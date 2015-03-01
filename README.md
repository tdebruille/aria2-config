# aria2-config
Instruction to configure aria2 and launch it as service with systemd.

## Create new user and switch

    # adduser aria2
    # su - aria2

## Create folders and config files

    $ mkdir -p ~/.config/aria2
    $ nano ~/.config/aria2/aria2.conf
      dir=/home/aria2/Downloads
      rpc-secret=SECRET
    $ touch ~/.config/aria2/session.lock
    $ mkdir Downloads
  
## Copy systemd unit file to units folder

    # cp aria2.service /etc/systemd/system/
    # systemctl enable aria2

