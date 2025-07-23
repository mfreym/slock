# Patched slock

This repository contains a customized version of `slock`, a simple X display locker, with several patches applied to enhance its functionality and usability.

## Description

`slock` is a simple screen locker for X. It is designed to be lightweight and stable, providing a straightforward way to lock your screen when you step away from your computer. This version of `slock` includes several patches that add new features and improve user interaction.

## Features

- **Squares**: Instead of changing the color of the entire screen, this patch draws centered squares on each monitor to indicate the current lock state. The size of the squares can be configured using `squaresize` in `config.h`. This feature requires `xrandr` to be active.

- **Squares Password**: Enhances the squares patch by ensuring the number of squares matches the length of your current input for responsive behavior.

- **User**: Uses the `$USER` environment variable to determine which user and group to use for the password, making it more flexible and easier to configure.

## Installation

### Prerequisites

- A C compiler (e.g., `gcc`)
- `make`
- Xlib header files

### Building and Installing

1. Clone the Repository:
   ```sh
   git clone https://github.com/mfreym/slock.git
   cd slock
   ```

2. Build:
    ```sh
    make
    ```

3. Install:
    ```sh
    sudo make install
    ```

## Usage

Once installed, you can launch slock by simply running the slock command. This will lock your screen immediately. To get out of it, enter your password.

## Credits

This project is based on [slock](https://tools.suckless.org/slock/), a simple screen locker for X developed by the [Suckless community](https://suckless.org/).
