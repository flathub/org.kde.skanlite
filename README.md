# Skanlite Flatpak

## How to configure a SANE backend

Here are the steps to configure a SANE backend like [the `net`
one](http://www.sane-project.org/man/sane-net.5.html):

1. Create the `sane.d` folder in the `config` app dir:
   ```shell
   $ mkdir $HOME/.var/app/org.kde.skanlite/config/sane.d
   ```
2. Write the backend config:
   ```shell
   $ cat $HOME/.var/app/org.kde.skanlite/config/sane.d/net.conf
   # This is the net backend config file.
   
   ## saned hosts
   # Each line names a host to attach to.
   # If you list "localhost" then your backends can be accessed either
   # directly or through the net backend.  Going through the net backend
   # may be necessary to access devices that need special privileges.
   localhost
   ```
   
   The `sane.d` config folder should look like this:
   ```
   ~/.var/app/org.kde.skanlite/config/
   ├── sane.d
   │   └── net.conf
   └── skanliterc
   ```
