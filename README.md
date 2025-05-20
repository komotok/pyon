Pyon [![Discord](https://img.shields.io/discord/1273043343445852161?style=social&logo=discord&label=Pyon)](https://discord.gg/d6gwJ5nquG)
A mod for Discord's mobile apps, a continuation of [Bunny]([https://github.com/pyoncord]).

# Installing

### Android

- **Root** with Xposed - [PyonXposedF](https://github.com/pyoncord/BunnyXposed/releases/latest)
- **Non-root** - [PyonManager](https://github.com/pyoncord/BunnyManager/releases/latest)

### iOS
- [**BunnyTweak**](https://github.com/pyoncord/BunnyTweak) - Get prebuilt rootful and rootless `.deb` files or the prepatched `.ipa ` - Pyon iOS builds have not yet been developed, and Android is a priority.

## Building
1. Install a Pyon loader with loader config support (any mentioned in the [Installing](#installing) section).
1. Go to Settings > General and enable Developer Settings.
1. Clone the repo:
    ```
    git clone https://github.com/komotok/pyon
    ```
1. Install dependencies:
    ```
    pnpm i
    ```
1. Build Pyon's code:
    ```
    pnpm build
    ```
1. In the newly created `dist` directory, run a HTTP server. I recommend [http-server](https://www.npmjs.com/package/http-server).
1. Go to Settings > Developer enabled earlier. Enable `Load from custom url` and input the IP address and port of the server (e.g. `http://192.168.1.236:4040/pyon.js`) in the new input box labelled `Pyon URL`.
1. Restart Discord. Upon reload, you should notice that your device will download Bunny's bundled code from your server, rather than GitHub.
1. Make your changes, rebuild, reload, go wild!

Alternatively, you can directly *serve* the bundled code by running `pnpm serve`. `pyon.js` will be served on your local address under the port 4040. You will then insert `http://<local ip address>:4040/pyon.js` as a custom url and reload. Whenever you restart your mobile client, the script will rebuild the bundle as your client fetches it.


## Contributing

Contributions to the project are both welcome and encouraged, but in absolutely no way mandatory. When contributing, please follow the Code of Conduct.
