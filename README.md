# Web Terminal
That simple websocket Web Terminal you've been searching everywhere for.

It consists of a single HTML file with just enough code and styling to
fire up an Xterm.js terminal on a webpage and connect to a websocket.

## Usage

### Local Access

Opening `https://new-wayland.com/terminal/` will connect to
`wss://localhost/ws` allowing you to test out your local websocket.

### Remote Access

Add a `host` query string to connect to a remote websocket

```
https://new-wayland.com/terminal?host=ipv6.srv-testy.gb1.brightbox.com
```

This will connect to `wss://ipv6.srv-testy.gb1.brightbox.com/ws`.

If your websocket sits on a different path, add a `path` query string.

### Self Serve

Download the file to your webroot

```
$ curl -L -o index.html https://new-wayland.com/terminal
```

When served the page will try to connect to a websocket on the path
`/ws` on the host that served the page. You can then just point your
browser at the server and you'll get a terminal.

```
$ firefox https://ipv6.srv-testy.gb1.brightbox.com
```

## Caveats

- Mobile use is less than ideal due to lack of control keys. Probably
needs some buttons.
- Allowing terminal access to anything is risky. Make
sure you know what you are doing.

## Contributing
Issues and Pull Requests welcome if you can think of ways to improve
the experience.
