# iptables

## 기본 정책 설정
- `iptables -P INPUT ACCEPT`
- `iptables -P OUTPUT ACCEPT`
- `iptables -P FORWARD ACCEPT`

## 현재 규칙 확인
- `iptables -L`
- `iptables --list`

## 수정 규칙 저장
- `service iptables save`

## 규칙 초기화
- `iptables -F`
