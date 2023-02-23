# Didstopia Klipper Configs

This repository contains our custom configuration files for Klipper, as well as other Klipper related files.

All configuration files are stored under the `/extra` directory, with emphasis on each config being as modular as possible.

## Installation / Usage

For the initial setup, you simply need to clone the repository to your home directory,
then symlink all the Klipper configuration files to your configuration directory.

Please note that you can also symlink only the config(s) you're interested in,
as the entire idea is to provide an easy way to handle configuration updates.

```bash
cd ~
git clone https://github.com/Didstopia/klipper-configs.git
ln -sf ~/klipper-configs/extra ~/printer_data/config/extra
ln -sf ~/klipper-configs/moonraker-klipper-configs.cfg ~/printer_data/config/moonraker-klipper-configs.cfg
```

Next, setup configuration updates by adding the following to your `moonraker.conf` file.

```ini
# ~/printer_data/config/moonraker.conf

# Klipper Configs update_manager entry
[include moonraker-klipper-configs.cfg]
```

Finally, include what you need in your config files, for example in your `printer.cfg` file:

```ini
# ~/printer_data/config/printer.cfg

# Include the base Creality Ender-3 V2 config
[include extra/creality-ender-3-v2.cfg]

# Now you can customize and override
# any configuration options you want.
```

## License

See [LICENSE](LICENSE).
