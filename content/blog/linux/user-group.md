---
title: 'Linux 에서 사용자의 그룹확인 및 특정 그룹에 추가'
date: 2020-01-15 12:00:00
category: 'linux'
---

### 현재 로그인한 사용자가 속한 그룹 확인

```shell script
$ groups
ubuntu adm dialout cdrom floppy sudo audio dip video plugdev lxd netdev
```

### 특정 사용자 그룹 확인(예 : tomcat)

```shell script
$ groups tomcat
tomcat : tomcat sudo
```

### leonkim 사용자를 wheel 그룹에 추가할 때

대부분 sudo권한이 있는 user가 입력 가능함.

```shell script
$ sudo gpasswd -a leonkim wheel
Adding user leonkim to group wheel
```
### leonkim 사용자를 wheel 그룹에 뺄때

```shell script
$ sudo gpasswd -d leonkim wheel
Removing user leonkim from group wheel
```
