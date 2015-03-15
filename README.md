# WeirdMeetup Server

## Vagrant 기본 설정
* Ruby : 2.2
* Gem : 2.2
* Rails : 4.2.0
* host only ip: 192.168.33.11

### rails 설정
* 현재 코드 기본 내용은 없음.
    * 작업시 `/vagrant`폴더 내용으로 해야되지 않을까함.
    * 이부분은 확인후 추가 및 작업에 대한 내용을 남겨야함.
* `rails new myapps`로 기본 내용 생성
* `rails server -b 0.0.0.0`로 실행시 외부에서 접근하려면
  `192.168.33.11:3000`으로 접근할 수 있음.

