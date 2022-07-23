sshppass scp 이용하여 원격 파일 전송================================================

sshpass
다른 컴퓨터에 바로 ssh 연결을 할 수 있고, 연결된 컴퓨터에서 명령어를 실행할 수 있는 기능

-p
패스워드

-o
옵션

StrictHostKeyChecking=no
로컬 인증키와 서버 인증키 비교 하지 않음

로컬 -> 원격
sshpass -p '패스워드' scp -o StrictHostKeyChecking=no 로컬파일 아이디@호스트주소:/폴더/파일명
sshpass -p 'test' scp -o StrictHostKeyChecking=no /local/tmp1 myid@10.10.10.1:/remote1/. 

원격 -> 로컬
sshpass -p '패스워드' scp -o StrictHostKeyChecking=no 아이디@호스트주소:/폴더/파일명 로컬파일
sshpass -p 'test' scp -o StrictHostKeyChecking=no myid@10.10.10.1:/remote1/. /local/tmp1

====================================================================================


cd [경로] : [] 안에 적힌 디렉토리로 이동
cd ~ : 기본 디렉토리로 이동
cd / : 기본 디렉토리 보다 위에 있는 디렉토리로 이동
cd . : 현재 디렉토리
cd .. : 상위 디렉토리 이동
cd - : 이전의 경로로 이동
ll : ls 명령어에 -l 옵션을 준 형태를 표시해주는 역활(권한, 소유자, 갱신일 확인)
ls : 해당 디렉토리에 존재하는 파일목록을 표시
ls -a : 숨겨진 파일 보기
pwd : 현재 경로 보기