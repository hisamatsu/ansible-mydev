# ansible-mydev

This playbook installs and configures most of the software I use for development on Ubuntu.
Whenever possible, the software is installed under $HOME. Some components are difficult to fully automate, so a few manual installation steps remain.
However, everything is documented here.

## Installation

  1. Prepare `${HOME}/.netrc` for GitHub authentication (the `.netrc` file must have `0600` permissions).
  2. Run `sudo apt update`
  3. Install pipx: `sudo apt install pipx`
  4. Ensure `pipx` is added to your path: `pipx ensurepath`
  5. Source your .bashrc: `source .bashrc`
  6. Install ansible `pipx install --include-deps ansible`
  7. Clone or download this repository to your local drive.
  8. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your password when prompted for the 'BECOME' password.
  9. Place your secret keys in `${HOME}.ssh`

## Included Applications / Configuration

Packages (installed with apt):
  - build-essential
  - tmux

Packages (installed with go install):
  - ghq

Packages (installed with cargo install):
  - bat
  - git-delta
  - eza
  - fd-find
  - ripgrep
  - starship
  - zoxide

Packages (installed with git)
  - fzf
  - oh_my_tmux
  - bash_it

Packages (installed with others):
  - neovim
  - go
  - rust

My [dotfiles](https://github.com/hisamatsu/dotfiles) are installed via ghq.


## Author

This project was created by [Hiroyuki Hisamatsu](https://sotome.org/).
