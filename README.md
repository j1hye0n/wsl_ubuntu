# VM_Ubuntu
based on vlsisys


## Vim 단축키
ctrl + u / ctrl + d 이동키

c 잘라내기

y 복사하기

p 붙여넣기

shift + insert 붙여넣기

Ctrl + v 비쥬얼블락 진입

Shift + v 비쥬얼라인 진입

각각 블락을 잡고 y로 복사같은 걸 한 다음에 블락단위별 수정을 진행하면 된다. 이때 노멀모드에서 해당 입력을 블락단위별 변경하고 싶으면 shift + i 를 눌러 한 줄을 우선 변경한다음 모드에서 나오면 된다.

:%s /” “/” “/g 문자 대체작성

rm 파일 삭제

rmdir 디렉토리 삭제

-rf 안에 든 파일 관계없이 삭제

:e ~/file_path 다른파일로 이동

들여쓰기 수정 : shift v로 전체 단락 잡고 "<" or ">"로 조절


## Setting of Ubuntu


1. gvim 등 gui 기능 지원 안될때
> export DISPLAY=:0.0
> echo $DISPLAY
> echo $DISPLAY 값이 120.0.0.1:* 로 나오면 gui 기능 x

=> :0.0 되는지 확인


2. new user authority

//powershell

> wsl -d <DistroName> -u root
> su -
> usermod -aG sudo <username>


3. 사용자가 등록되어있지만 root가 메인 디렉토리로 인식될때
//powershell
> ubuntu2204(.exe) config --default-user hyeon(username)
> C:\Users\username\AppData\Local\Microsoft\WindowsApps\  // wsl .exe path


또는
//bash
> sudo vim /etc/wsl.conf
//vim
> [user]
> default=user



4. 드라이브 이동
//powershell
> wsl --export Ubuntu-22.04 D:\wsl_backup.tar // 현재 wsl 압축해서 내보내기
> wsl --unregister Ubuntu-22.04 // D폴더(기존 wsl) 삭제
> wsl --import Ubuntu-22.04 C:\WSL D:\wsl_backup.tar // c드라이브에 재설치 , 설정 유지

### to check DistroName
> wsl -list -all

### to verify
> groups <username>
