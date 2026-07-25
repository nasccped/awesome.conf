# AwesomeWM config

Here's my personal config for [`Awesome window manager`](https://awesomewm.org/).

## Requirements

This config requires:
- **git** for cloning
- **lua** runtime for awesome script run
- **awesome** (can be installed through package manager)
- **xorg** and **xorg-server**
- **xrandr** for xorg resolution
- **setxkbmap** for keyboard layout
- **dbus-run-session** cmd for brave working

## Set up

1. Clone the repository to the conf's path:
```sh
git clone https://github.com/nasccped/awesome.conf "$HOME/.config/awesome"
```

2. Start xorg server:
```sh
startx
```

> [!NOTE]
>
> The instruction above only works if prepared `.xinitrc`.
>
> My current config is:
> ```sh
> xrandr --output Virtual-1 --mode 1920x1080 --rate 60
> setxkbmap -layout br -variant abnt2
> 
> exec dbus-run-session awesome
> exec awesome
> ```
>
> - `xrandr` to set the prefered resolution
> - `setxkbmap` (change keyboard layout from default to my actual layout)
> - `dbus-run-session` to allow brave connecting
