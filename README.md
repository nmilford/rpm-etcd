rpm-etcd
========

An RPM spec file to build and install etcd.

To Install:

`etcd_version='2.0.9'`

`etcd_rpm_github_repo='nmilford/rpm-etcd'`

`sudo yum -y install rpmdevtools && rpmdev-setuptree`

`wget https://raw.github.com/${etcd_rpm_github_repo}/master/etcd.spec -O ~/rpmbuild/SPECS/etcd.spec`

`wget https://github.com/coreos/etcd/releases/download/v${etcd_version}/etcd-v${etcd_version}-linux-amd64.tar.gz -O ~/rpmbuild/SOURCES/etcd-v${etcd_version}-linux-amd64.tar.gz`

`wget https://raw.github.com/${etcd_rpm_github_repo}/master/etcd.initd -O ~/rpmbuild/SOURCES/etcd.initd`

`wget https://raw.github.com/${etcd_rpm_github_repo}/master/etcd.sysconfig -O ~/rpmbuild/SOURCES/etcd.sysconfig`

`wget https://raw.github.com/${etcd_rpm_github_repo}/master/etcd.nofiles.conf -O ~/rpmbuild/SOURCES/etcd.nofiles.conf`

`wget https://raw.github.com/${etcd_rpm_github_repo}/master/etcd.logrotate -O ~/rpmbuild/SOURCES/etcd.logrotate`

`rpmbuild -bb ~/rpmbuild/SPECS/etcd.spec`
