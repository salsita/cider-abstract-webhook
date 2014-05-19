# go-meeko-webhook-receiver #

go-meeko helper for implementing webhook collectors.

This package takes care of some boilerplate code while implementing webhook
collectors for Meeko. All that is necessary is to pass a `http.Handler` into
`ListenAndServe` and the rest will be taken care of.

## Environment ##

There are two variables that must be defined for `ListenAndServe` to work:

* `LISTEN_ADDRESS` - the network address to listen on, format `HOST:[PORT]`
* `ACCESS_TOKEN` - the access token that must be present in all the POST request
                   as a parameter, otherwise the request is rejected

These should be included in `.meeko/agent.json` as other variables.

## License ##

MIT, see the `LICENSE` file.
