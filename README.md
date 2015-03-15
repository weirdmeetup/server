# WeirdMeetup Server
## Introduction

## Requirements
* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant 1.7.2](https://www.vagrantup.com/)

## How To Build The Virtual Machine

```
$ git clone https://github.com/weirdmeetup/server.git
$ cd server
$ vagrant up		// 시간이 오래 걸립니다
```
설치가 완료되면, Virtual Machine에 다음과 같은 방법으로 접속 가능합니다.
```
$ vagrant ssh
Welcome to Ubuntu 14.04.2 LTS (GNU/Linux 3.13.0-46-generic x86_64)
...
vagrant@weirdmeetup:~$
```
Host 컴퓨터의 3000번 포트는 Virtual machine 의 3000번 포트로 포워딩 됩니다. 따라서, VM에서 동작하는 어플리케이션은 host컴퓨터에서 localhost:3000으로 접근 가능합니다.  

## Vagrant 기본 설정
* Ruby : 2.2
* Gem : 2.2
* Rails : 4.2.0
* OS : ubuntu 64bit
* host only ip: 192.168.33.11

### rails 설정
* 현재 코드 기본 내용은 없음.
    * 작업시 `/vagrant`폴더 내용으로 해야되지 않을까함.
    * 이부분은 확인후 추가 및 작업에 대한 내용을 남겨야함.
* `rails new myapps`로 기본 내용 생성
* `rails server -b 0.0.0.0`로 실행시 외부에서 접근하려면
  `192.168.33.11:3000`으로 접근할 수 있음.

## Vritual Machine Management
간단하게 VM을 로그아웃하려면 `^D`로 가능하고, suspend모드는
```
$ vagrant suspend
```
로 가능합니다. 다시 resume 하기 위해서는
```
$ vagrant resume
```
으로 가능합니다. VM을 종료하기 시키기해서는
```
$ vagrant halt
```
를 입력하면 되고, 다시 부팅하기 위해서는

```
$ vagrant up
```
을 입력하면 됩니다.

```
$ vagrant status
```
를 호출함으로써 언제든 가상머신의 상태를 확인 할 수도있습니다.

VM을 완벽하게 삭제하려면 다음 명령어로 모든 컨텐츠를 삭제할 수 있습니다.
```
$ vagrant destroy # DANGER: all is gone
```
