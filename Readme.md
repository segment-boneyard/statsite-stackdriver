
# statsite-stackdriver

  Stackdriver sink for the [Statsite](https://github.com/armon/statsite) statsd implementation.

## Installation

```
$ npm install -g statsite-stackdriver
```

## Usage

```

  Usage: statsite-stackdriver [options]

  Options:

    -h, --help       output usage information
    -V, --version    output the version number
    -k, --key <key>  stackdriver api key
    -v, --verbose    verbose output

```

## Configuration

 Just add the command to your Statsite configuration, supplying the API key and you're good to go! Use `--verbose` to output the metrics being sent to stackdriver.

```
stream_cmd = statsite-stackdriver --key <stackdriver-api-key>
```

## Instance metrics

  Along with regular metrics you may also specify the origin instance id by wrapping the first segment in `[` `]` characters. For example where you might typically do `statsd.timer('request', delta)`, prefix with the id: `statsd.timer('[instance-id-here].request', delta)`.

## License

  MIT
