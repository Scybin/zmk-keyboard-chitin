# ZMK Module: chitin Keyboard

This repository provides shield files for the [chitin](https://github.com/Scybin/chitin) keyboard. It can be used to build the ZMK firmware for the keyboard.

## Usage

Edit your west.yaml file found in your zmk config's config directory to add the scyboard module.

Example:

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: scybin
      url-base: https://github.com/chitin
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboard-chitin
      remote: scybin
      revision: main
  self:
    path: config
```

My personal ZMK firmware configuration can be found [here](https://github.com/Scybin/zmk-config-chitin).

## More Info

For more info on modules, you can read through the [Zephyr modules page](https://docs.zephyrproject.org/3.5.0/develop/modules.html) and [ZMK's page on using modules](https://zmk.dev/docs/features/modules). [Zephyr's west manifest page](https://docs.zephyrproject.org/3.5.0/develop/west/manifest.html#west-manifests) may also be of use.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
