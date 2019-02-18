# 기본

## 기본 명령어
- 비밀번호 변경: passwd *password*
- 아이디 목록: cat /etc/passwd

## 권한 주기
- chown -R root:root ./folder

## 방화벽 처리
- 포트 확인
  - 모든 포트 조회: netstat -a
  - tcp 포트 확인: netstat -tnl
- 포트 열기
  - nc -kl 80 &

## 세션 종료시간 일시 변경
- 세션 종료시간 확인
  - echo $TMOUT
- 세션 종료시간 변경
  - export TMOUT=0

## sudo 권한 획득
- su -
- visudo f /etc/sudoers
- root ALL=(All) ALL 복사해서 root 대신 권한 부여할 아이디 입력
- usermod -aG wheel username
