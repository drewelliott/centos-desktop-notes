### Initial Install ###
I chose to install the minimal iso from centos.org's download page:

  [https://www.centos.org/download](https://www.centos.org/download)

My first step is to install a DE - I chose to use gnome3 since it is the default:

To get a list of the various DE groups (among others), run the following:
```
  $ yum group list 
```
To install gnome3, I did the following:
```
  $ sudo yum -y groupinstall "GNOME Desktop"
```
By default, the system is not set to use Gnome Shell (the graphical login), you can change that through systemd:
```
  $ sudo systemctl set-default graphical.target
```
Now, just reboot to be presented with the graphical login.

### Extra Repository ###
I am adding the epel (extra packages for enterprise linux) with this command:
```
  sudo yum --enablerepo=extras install epel-release
```



