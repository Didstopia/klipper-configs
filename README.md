# Didstopia Klipper Configs

Our custom configuration files for Klipper.

## Installation / Usage

For the initial setup, you simply need to clone the repository to your home directory,
then symlink all the Klipper configuration files to your configuration directory.

Please note that you can also symlink only the config(s) you're interested in,
as the entire idea is to provide automatic updates for the configuration files.

```bash
cd ~
git clone https://github.com/Didstopia/klipper-configs.git
ln -sf ~/klipper-configs/*.cfg ~/printer_data/config/
```

Next, setup the automatic updates by adding the following to your `moonraker.conf` file.

```toml
[update_manager klipper-configs]
type: git_repo
primary_branch: master
path: ~/klipper-configs
origin: https://github.com/Didstopia/klipper-configs.git
managed_services: klipper
```

## License

See [LICENSE](LICENSE).
