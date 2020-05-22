# app-get
> AppImages manager via command line

## Installation
```sh
git clone https://github.com/terroo/app-get up-app-get
cd up-app-get
./INSTALL && source ~/.bashrc
cd .. && rm -rf up-app-get/
```

## Using
```sh
usage: app-get [options] [package]
  
  Options:
    ---list            Lists all available packages
    --nocolor          Disable colors
    --update           Checks and updates this program
    --info [package]   Describes data for an available package
    --remove [package] Removes the informed package
    -h,--help          Show this content
    -v,--version       Show version

  Example, install qbittorrent: $ app-get qbittorrent  
```

## Contributing
If you want to add a new package to the project, follow these steps:
1. Fork the project
2. Clone your fork
```sh
git clone https://github.com/[YOUR_USER]/app-get up-app-get
```
3. Edit the `lib/apps.list` file
```sh
vim up-app-get/lib/apps.list
```
4. This file has data separated by spaces per line. And each field has a certain information:

| command | name | category | version | AppImage link | website | icon/.desktop automatic
|---|---|---|---|---|---|---|
| application command | name (usually with capital letters) | Category based on .desktop | Program version | AppImage link, use only the official project link, preferably from a Git repository | Inform the official website of the program | If when you run AppImage for the first time and it opens a box asking if you want to create the .desktop and the icon automatically, check `true`, but after testing it on your machine, it does not generate and is not automatically available from Dash your system, check `false` |

Example for the `FooBar` program:
```sh
foobar FooBar Utility;Graphics 1.0 https://github.com/foobar/FooBar.AppImage https://foobar.net false
```
> Add only those that you have tested on your machine.
5. Add a program icon in **PNG** format with **256x256** resolution to the directory: `data/icons/hicolor/256x256`
6. Submit a [Pull Request](https://bit.ly/prenlink)

## Report bugs
<https://github.com/terroo/app-get/issues>

## Uninstalation
```sh
git clone https://github.com/terroo/app-get up-app-get
cd up-app-get
./INSTALL remove
```
