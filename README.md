# pros-application-browser

This project produces an electron application that provides a flashplayer plugin.
A config file is used to restrict navigation to specific start pages as well as setup of the flashplayer plugin.

## Quick start

Clone and run this repo

```sh
npm install
npm start
```

Then follow the on-screen instructions on how to configure the application environments.

## config.json

Below is a sample configuration for the application

```javascript {
  "flash":
  {
    "path":"C:\\Windows\\System32\\Macromed\\Flash\\pepflashplayer64_28_0_0_137.dll"
  },

 "environments":
  [
    {
      "id": "test",
      "url": "https://www.google.it",
      "label": "Test"
    }, {
      "id": "sandbox",
      "url": "https://us.yahoo.com/",
      "label": "Sandbox"
    }, {
      "id": "production",
      "url": "https://www.facebook.com",
      "label": "Production"
    }
  ]
}
```

* flash - path - The path to the installed flashplayer - version - <i>(optional)</i> version number of the flashplayer
* environments - An array of environments that will be available on the launch page - id - unique id for the environment - url - fully qualified path to a website - label - The name of the link when shown in the UI
* develop - <i>(optional)</i> boolean value used to turn on development mode
* locale - <i>(optional)</i> forced override for the locale value. System locale will be used if not specified.

## How to Build

To build the installer, run the make command.

```sh
npm install
npm run make
```

Once complete the setup file will be in the `\out` folder.

## Contributors

[List of Contributors](CONTRIBUTORS)

## License

[GNU General Public License v3.0](LICENSE)
