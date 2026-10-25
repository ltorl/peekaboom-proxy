# Peekaboom-Proxy
Extremely compatible proxy that serves any public website so it can be embedded in an iframe. Includes rewriter.

uses wss://anura.pro/ by default. Pass `?wisp=` to use another Wisp relay:

```
https://peekaboom-proxy.github.io/?wisp=wss://example.com/wisp/&url=https://example.com/
https://peekaboom-proxy.github.io/__px/https://example.com/?wisp=ws://localhost:5001/
```

The relay is remembered until another `?wisp=` is given (or the home page is opened without one, which goes back to the default).

A relay on your own machine or network (`ws://localhost:5001/`, `ws://192.168.…`) needs Chrome's local network permission: allow it when the page asks. When the proxy is in an iframe, the embedding page has to delegate it:

```html
<iframe allow="loopback-network; local-network; local-network-access" src="https://peekaboom-proxy.github.io/__px/https://example.com/?wisp=ws://localhost:5001/"></iframe>
```

# Link: https://peekaboom-proxy.github.io/
