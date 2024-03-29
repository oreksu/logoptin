# logi
Unofficial Logitech Options for Linux

!!! THIS SOFTWARE IS UNDER DEVELOPMENT, PLEASE DO NOT USE !!!


## Intro
I created this project to learn [`systemd`](https://wiki.archlinux.org/title/systemd), Rust, DBus, daemons, and Linux services in general.
As such I tried to document everything extensively, so others can learn from this repo as well.
I am also trying to have a good number of `good-first-issues`, so newcomers can join.
Please be welcome to give your thoughts and help with the project.
I hope this will be usefull for people.


## Alternatives
Main alterntive is [`logiops`](https://github.com/PixlOne/logiops),
which is great and did most of the work to establish a logitech support.
In out case, we trying to go beyond simple support and provide easy user experience,
with future GUI. Examples of simplifications are easier config file, more standart
location of the config, availabilty via linux package mangers.
Generally simpler design.


## Config
We adhere to [XDG Base Directory Spec](https://wiki.archlinux.org/title/XDG_Base_Directory).
Logi will look for config in such order of priority:
- `XDG_CONFIG_HOME/logi/logi.toml` env variable
- `$HOME/.config/logi/logi.toml`
- `$HOME/.logi.toml`
- `$HOME/.logi/logi.toml`

Simple config using TOML file located at `.config/logi/<DEVICE-NAME>.toml`
We use toml, cause it simple and readable, I dislike the 

### Format
```

```


## MacOS and Windows users
Please use the official driver and app from Logitech: [Logi Options+](https://www.logitech.com/en-us/software/logi-options-plus.html).


## How this works?

### Daemon

### systemd

### userspace

### driver

### HID++
- [Logitech Specification for HID++ 2.0](https://lekensteyn.nl/files/logitech/logitech_hidpp_2.0_specification_draft_2012-06-04.pdf)
- [Solaar on HID++](https://pwr-solaar.github.io/Solaar/features.html)
- [libratbag](https://github.com/libratbag/libratbag) - DBus daemon to configure imput devices
- [hidpp](https://github.com/cvuchener/hidpp) - Collection of HID++ tools 


## Libraries to use
- https://github.com/GuillaumeGomez/systemd-manager
- https://stackoverflow.com/questions/63093667/start-a-rust-binary-as-a-systemd-daemon
- https://crates.io/crates/daemonize
- https://www.freedesktop.org/software/systemd/man/daemon.html
- https://medium.com/all-about-rust/setup-rust-app-as-a-service-in-ubuntu-df788c1f1d41
- https://www.reddit.com/r/rust/comments/s1wejw/systemdclient_released/
- https://gitlab.freedesktop.org/dbus/zbus/
- https://github.com/51yu/systemd-client
- https://www.reddit.com/r/rust/comments/autf51/how_to_set_systemd_and_let_rust_run_in_background/
- https://www.reddit.com/r/rust/comments/e9o724/rustysd_a_systemdcompatible_service_manager/
- https://www.reddit.com/r/rust/comments/rqyb6z/how_do_i_run_my_rust_code_as_a_service_in_linux/
- https://github.com/vasilakisfil/hello.service
- https://lib.rs/crates/cargo-deb
- https://fabianlee.org/2017/05/21/golang-running-a-go-binary-as-a-systemd-service-on-ubuntu-16-04/
- https://github.com/brunoborges/toml-schema
- https://github.com/mehcode/config-rs
- https://12factor.net/
- https://docs.rs/config/0.1.3/config/
- https://danishshakeel.me/configure-logitech-mx-master-3-on-linux-logiops/
- https://github.com/PixlOne/logiops/wiki/Configuration
- [control id from linux](https://github.com/torvalds/linux/blob/master/include/uapi/linux/input-event-codes.h)


## Used Libraries
- [clap](https://crates.io/crates/clap) for cli
- [xdg](https://crates.io/crates/xdg) for config file
- [toml](https://crates.io/crates/toml)
- [cargo-deb](https://crates.io/crates/cargo-deb)
  
### Looking into 
- https://docs.rs/figment/latest/figment/index.html#metadata
- https://crates.io/crates/config


## Stadards Used
- [systemd](https://systemd.io/)
- [XDG Base Directory Specification](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html)


## Logi GUI
Make it work with logiops as well.
- https://www.egui.rs/#demo
- https://docs.rs/libconfig/latest/libconfig/
- https://hyperrealm.github.io/libconfig/libconfig_manual.html


## Other
- https://en.wikipedia.org/wiki/Daemon_(computing)
- https://stackoverflow.com/questions/61671013/how-to-make-rust-run-gracefully-in-the-background-and-daemonize
- https://stackoverflow.com/questions/61443052/rust-daemon-best-practices
- https://stackoverflow.com/questions/70676063/how-to-make-rust-log-into-journalctl-using-release-binary
- https://stackoverflow.com/questions/26354465/creating-a-simple-rust-daemon-that-listens-to-a-port
- https://medium.com/all-about-rust/setup-rust-app-as-a-service-in-ubuntu-df788c1f1d41
- https://github.com/vasilakisfil/hello.service
- https://stackoverflow.com/questions/63093667/start-a-rust-binary-as-a-systemd-daemon
- https://fabianlee.org/2017/05/21/golang-running-a-go-binary-as-a-systemd-service-on-ubuntu-16-04/
- https://www.linuxjournal.com/article/2476
- https://not-matthias.github.io/posts/kernel-driver-with-rust/
- 


## Credits
- [PixlOne](https://github.com/PixlOne) for amazing [logiops](https://github.com/PixlOne/logiops).
- [vasilakisfil](https://github.com/vasilakisfil) for simple [hello.service](https://github.com/vasilakisfil/hello.service) Rust example
