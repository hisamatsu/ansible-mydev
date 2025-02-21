# ansible-mydev

This playbook installs and configures most of the software I use for development on Ubuntu.
Whenever possible, the software is installed under $HOME. Some components are difficult to fully automate, so a few manual installation steps remain.
However, everything is documented here.

## Installation

  1. prepare ${HOME}/.netrc for github authentication
  2. sudo apt update
  3. sudo apt install pipx
  4. pipx ensurepath
  5. source .bashrc
  6. pipx install --include-deps ansible
  7. Clone or download this repository to your local drive.
  8. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your password when prompted for the 'BECOME' password.
  9. put secret keys in ${HOME}.ssh

## Included Applications / Configuration

Packages (installed with apt):
  - build-essential
  - tmux

Packages (installed with go install):
  - ghq

Packages (installed with cargo install):
  - bat
  - fd-find
  - eza
  - ripgrep
  - fd-find
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
