rpm-etcd
========

An RPM spec file to build and install etcd.

To Install:
You will need go from http://repo.milford.io.

`sudo yum -y install rpmdevtools go && rpmdev-setuptree
`wget https://raw.github.com/nmilford/rpm-etcd/master/etcd.spec -O ~/rpmbuild/SPECS/etcd.spec`

`wget https://github.com/coreos/etcd/releases/download/v0.1.0/etcd-v0.1.0-Linux.tar.gz -O ~/rpmbuild/SOURCES/etcd-v0.1.0-Linux.tar.gz`

`wget https://raw.github.com/nmilford/rpm-etcd/master/etcd.initd -O ~/rpmbuild/SOURCES/etcd.initd`

`wget https://raw.github.com/nmilford/rpm-etcd/master/etcd.sysconfig -O ~/rpmbuild/SOURCES/etcd.sysconfig`

`wget https://raw.github.com/nmilford/rpm-etcd/master/etcd.nofiles.conf -O ~/rpmbuild/SOURCES/etcd.nofiles.conf`

`wget https://raw.github.com/nmilford/rpm-etcd/master/etcd.logrotate -O ~/rpmbuild/SOURCES/etcd.logrotate`

`rpmbuild -bb ~/rpmbuild/SPECS/etcd.spec`
