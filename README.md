<p align="center">
  <a href="https://avwo.github.io/whistle/">
    <img alt="whistle logo" src="https://raw.githubusercontent.com/avwo/whistle/master/biz/webui/htdocs/img/whistle.png">
  </a>
</p>

# About whistle

It is an HTTP, HTTPS, Websocket debugging proxy. https://github.com/avwo/whistle

Here is the docs in English of whistle. Other language versions followed:

[中文文档](https://avwo.github.io/whistle/)

### Any contribution to this doc is warmly welcomed. Whistle need your help, so that not just Chinese developers enjoy such a wonderful tool.

If you still wonder what can whistle do, take a look  at [Fiddler](https://www.telerik.com/fiddler). Though they are not the same thing, but quite similar to many web developers.

It can be used to view or modify the request and the reponse contents through http/https/websocket, even just as an HTTP proxy server. Whistle's rule configuration is much alike with the hosts file, but more powerful by supporting matching hostname, path, regular expression, wildcards and so on.

# Setup whistle

Four steps:

1. Install Node(>= v0.10.0) https://nodejs.org/en/download/

2. Install whistle

```
    npm install -g whistle
```
once installed, run `whistle help` or `w2 help` to checkout more helpful information, seeing below means successful installation:

```
$ w2 help

Usage: w2 <command> [options]

  Commands:

    run       Start a front service
    start     Start a background service
    stop      Stop current background service
    restart   Restart current background service
    help      Display help information

  Options:

    -h, --help                                      output usage information
    -d, --debug                                     debug mode
    -l, --localUIHost [hostname]                    local ui host(local.whistlejs.com by default)
    -n, --username [username]                       login username
    -w, --password [password]                       login password
    -S, --storage [newStorageDir]                   the new local storage directory
    -C, --copy [storageDir]                         copy storageDir to newStorageDir
    -p, --port [port]                               whistle port(8899 by default)
    -m, --middlewares [script path or module name]  express middlewares path(as: xx,yy/zz.js)
    -u, --uipath [script path]                      web ui plugin path
    -t, --timeout [ms]                              request timeout(36000 ms by default)
    -s, --sockets [number]                          max sockets(12 by default)
    -V, --version                                   output the version number
    -c, --command <command>                         command parameters ("node --harmony")
```

3. Start up whistle

    `whistle`, `w2` and `wproxy` act the same if you installed the latest whistle.

```shell
# start
w2 start

# restart
w2 restart

# stop
w2 stop

# debugging mode(useful investigating exceptions or plugins development)
w2 run
```

4. Configuration

You should modify your browser of system's proxy setting, so that HTTP proxy 127.0.0.1:8899 be set. And then visit http://127.0.0.1:8899, you can see all your http traffic in the `Network` pannel. Like this:

![Network](https://raw.githubusercontent.com/avwo/whistleui/master/img/network.gif)

done!



