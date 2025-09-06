## 문제1. 가상머신 구축

# 현재 쉘 확인
grep testuser /etc/passwd

# 쉘 변경
exit
sudo chsh -s /bin/dash testuser

# 쉘 변경 확인
grep testuser /etc/passwd

# 쉘 목록 확인
cat /etc/shells
chsh -l

## 문제2. 리눅스 명령어 실습
man pwd
man cd        
man ls
man mkdir
man rm
man cp
man mv
man touch

cd는 셸 내장 명령(built-in)이므로 man이 아닌 다음 명령으로 확인 가능

help cd

# 디렉토리 생성
cd ~
mkdir tmp1 tmp2

# 파일 생성
cd tmp1
touch tmpfile1 tmpfile2

# 파일 복사 및 삭제
cp tmpfile2 ~/tmp2/
rm tmpfile2

# 디렉토리 이동
mv ~/tmp1 ~/tmp2/

# 결과 확인
tree ~/tmp2
ls -R ~/tmp2

* /etc/passwd 파일에서 계정 목록 확인
cat /etc/passwd

* 현재 사용하는 쉘 확인
grep testuser /etc/passwd

## 문제3. 리눅스 계정 관리

# 계정 목록 확인
cat /etc/passwd

# 사용자 전환
su testuser
cd ~
ls -la


## 문제4. Git 설치 및 설정

명령어
  
# 설정 확인
git config --global --list
git config --global -e


## 문제 5. Python 및 Flask 웹 서버 실행

명령어

# Python 버전 확인
python3 --version

# 서버 실행
python3 ~/app.py

# UFW 방화벽 설정 중일 경우 포트 8080 허용
sudo ufw allow 8080