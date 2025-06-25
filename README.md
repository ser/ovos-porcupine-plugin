## Picovoice Porcupine Wakeword plugin for OVOS

This plugins allows using [Porcupine](https://github.com/Picovoice/porcupine) wakewords together with OVOS/Hivemind.

## Configuration
To activate the plugin edit the hivemind config `~/.config/hivemind-core/server.json` command and add a hotword section if it doesn't already exist

```
[...]
  "hotwords": {

  }
```

Then insert a new hotword into the `hotwords` section

```
    "blueberry": {
      "module": "porcupine_wakeword_plug",
      "keyword_file_path": "~/blueberry_linux.ppn",
      "sensitivity": 0.5,
      "access_key": <your_access_key>
    }
```

Above is using the _blueberry_ model provided by picovoice stored in the location `~/blueberry_linux.ppn` and a sensitivity of 0.5.

## Models
Some models are available without charge from the [picovoice repo](https://github.com/Picovoice/porcupine/tree/master/resources/keyword_files), you can also generate models using the [Picovoice console](https://console.picovoice.ai/)

## Supported platforms

Porcupine ships precompiled binaries for several common platforms (x86 amd64, raspberry Pi, and several more) but may not work on your platform. Check their repo for more details.

## Credits

The original Mycroft bindings for Porcupine was written by @Tanel.Alumae, and thuis plugin is based upon their initial work with some updates for newer Porcupine releases and written by @forslund.

### Contributors

The following people are awesome and has helped with the development of this plugin:

- Tanel.Alumae
- forslund
- builderjer
- jarbasal
- NoiSek
