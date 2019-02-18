# 시작하기

## 용어 정리
- epel: Extra Packages for Enterprise Linux
- npm: Node Package Manager
- rpm: Redhat Package Manager
- yum: Yellodog Updater Modified

## epel 저장소 추가
- 패키지 설치여부 확인
  - rpm -q epel-release
- 패키지 설치가능여부 확인
  - yum list epel-release
- 패키지 설치
  - yum -y install epel-release

## nodejs 설치
- nodejs 설치여부 확인
  - rpm -q nodejs 또는 node -v
- nodejs, npm 설치
  - yum -y install nodejs npm
- n(; nodejs 버전 관리 패키지) 설치
  - yum -y update openssl
  - npm cache clean -f
  - npm install n -g
- nodejs 지정 버전 설치
  - 상세 매뉴얼은 npm의 n 패키지 저장소 참고
  - n lts
- 재부팅 후 버전 확인
  - reboot
  - node -v
