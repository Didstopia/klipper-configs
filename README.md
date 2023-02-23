# Didstopia Klipper Configs

This repository contains our custom configuration files for Klipper, as well as other Klipper related files.

All configuration files are stored under the `/extra` directory, with emphasis on each config being as modular as possible.

## Installation / Usage

For the initial setup, you simply need to clone the repository to your home directory,
then symlink all the Klipper configuration files to your configuration directory.

Please note that you can also symlink only the config(s) you're interested in,
as the entire idea is to provide automatic updates for the configuration files.

```bash
cd ~
git clone https://github.com/Didstopia/klipper-configs.git
ln -sf ~/klipper-configs/extra ~/printer_data/config/extra
```

Next, setup the automatic updates by adding the following to your `moonraker.conf` file.

```ini
[update_manager klipper-configs]
type: git_repo
primary_branch: master
path: ~/klipper-configs
origin: https://github.com/Didstopia/klipper-configs.git
managed_services: klipper
```

Finally, include what you need in your config files, for example in your `printer.cfg` file:

```ini
# ~/printer_data/config/printer.cfg
[include extra/creality-ender-3-v2.cfg]

# Now you can customize and override
# any configuration options you want.
```

## License

See [LICENSE](LICENSE).
