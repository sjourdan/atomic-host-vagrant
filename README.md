# Atomic Host Vagrant

This does nothing more than launch an Atomic Host on Vagrant from [CentOS Atomic on Atlas] (https://atlas.hashicorp.com/centos/boxes/atomic-host).

This does not currently use the [Fedora Atomic image](https://getfedora.org/cloud/download/atomic.html). An index of files from Fedora Atomic can be found [here](https://download.fedoraproject.org/pub/alt/atomic/stable/Cloud-Images/x86_64/Images/).

The image weighs around 420MB un compressed.

* [CentOS Atomic SIG](https://wiki.centos.org/SpecialInterestGroup/Atomic/Download/)
* [Fedora Atomic](https://getfedora.org/cloud/download/atomic.html)
* [Project Atomic](http://www.projectatomic.io/)
* [Atomic Host on Atlas](https://atlas.hashicorp.com/centos/boxes/atomic-host)

## Usage

Launch on virtualbox:

    vagrant up --provider virtualbox

Note: there's no VMware support currently.

You can test basic functionality:

```
$ sudo atomic host status
  TIMESTAMP (UTC)         VERSION        ID             OSNAME                 REFSPEC
* 2015-11-18 10:59:15     7.20151118     4916c22d5c     centos-atomic-host     centos-atomic-host:centos-atomic-host/7/x86_64/standard
```

Or upgrade your host if needed:

```
$ sudo atomic host upgrade
Updating from: centos-atomic-host:centos-atomic-host/7/x86_64/standard


No upgrade available.
```
