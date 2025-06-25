# 🔓 Wargame hacking report

![Wargame Report Demo](https://github.com/whathekim/hacking_report/blob/main/Wargame_report_main.gif?raw=true)


본 프로젝트는 실전 웹 환경을 가정하여, 숨겨진 페이지 탐색부터 파일 업로드 우회 및 리버스 셸 확보, 내부 DB 접근까지의 침투 흐름을 실습한 사례입니다.  
업로드 필터링을 우회해 리버스 셸을 성공적으로 실행하였고, 웹 서버 내부의 설정 파일을 통해 데이터베이스 접속 정보까지 확인할 수 있었습니다.

---

## 🛠️ 사용 도구 및 환경

Date: 2025년 6월 8일 ~ 6월 24일

Victim OS : Rocky Linux 9.5
Victim IP: 192.168.5.160 / TeamESG Wargame website

Attacker OS: Kali Linux
Attacker IP: 192.168.5.~ / 192.168.56.~

Tool: Kali Linux, wfuzz, gobuster, reverseshell 

---

## ✅ 주요 내용

- `wfuzz`와 `gobuster`를 이용해 숨겨진 디렉토리 및 페이지 탐색
- 업로드 필터링을 우회 (.php.kr 확장자 사용)하여 리버스 셸 업로드
- `nc`를 통한 셸 연결, bash 환경으로 전환 (`pty.spawn`)
- `db.php` 내부 설정 확인을 통해 MySQL 접속
- 워게임 플래그 및 유저 정보 획득

---

## ⚠️ 목적

- 웹 취약점 기반 침투 흐름 이해
- 파일 업로드 우회 기법 실습
- 셸 제어 및 내부 시스템 분석 역량 강화
- 보안 장비(Wazuh) 로그 탐지 결과 확인

---

## 📝 모의해킹 보고서 pdf
[► 모의해킹 보고서 PDF 보기](https://github.com/whathekim/hacking_report/blob/main/%EC%A1%B0%EB%B2%94%EA%B7%BC%20%EB%AA%A8%EC%9D%98%ED%95%B4%ED%82%B9%EB%B3%B4%EA%B3%A0%EC%84%9C.pdf)

[► 모의해킹 보고서 PDF 다운로드](https://github.com/whathekim/hacking_report/raw/main/%EC%A1%B0%EB%B2%94%EA%B7%BC%20%EB%AA%A8%EC%9D%98%ED%95%B4%ED%82%B9%EB%B3%B4%EA%B3%A0%EC%84%9C.pdf)

