# vagrant-ubuntu

A single instance of Ubuntu using Vagrant and VirtualBox

## Requirements

* VirtualBox
* Vagrant

### Installing Requirements

#### macOS

Using `homebrew`

```bash
brew cask install virtualbox virtualbox-extension-pack

brew cask install vagrant
```

## Using

Start the instance and connect via SSH.

```bash
vagrant up

vagrant ssh ubuntu
```

