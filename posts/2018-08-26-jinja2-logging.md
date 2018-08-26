# jinja2 print to console or logging

As explained on this [stackoverflow A](https://stackoverflow.com/a/42888467/3130926)

In python / flask:

    @app.context_processor
    def utility_functions():
        def print_in_console(message):
            print str(message)

        return dict(mdebug=print_in_console)

In jinja2, Use it anywhere as follows:

    {{ mdebug("any text or variable") }}
