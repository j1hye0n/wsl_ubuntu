# VM_Ubuntu
based on vlsisys

# Vim 단축키

# visual mode
ctrl + u / ctrl + d 이동키
c 잘라내기
y 복사하기
p 붙여넣기
shift + insert 붙여넣기
Ctrl + v 비쥬얼블락 진입
Shift + v 비쥬얼라인 진입
각각 블락을 잡고 y로 복사같은 걸 한 다음에 블락단위별 수정을 진행하면 된다. 이때 노멀모드에서 해당 입력을 블락단위별 변경하고 싶으면 shift + i 를 눌러 한 줄을 우선 변경한다음 모드에서 나오면 된다.
:%s /” “/” “/g 문자 대체작성

# Setting of Ubuntu

1. gvim 안열릴때
> export DISPLAY=:0.0
> echo $DISPLAY

=> :0.0 되는지 확인

2. new user authority
//powershell
> wsl -d <DistroName> -u root
> su -
> usermod -aG sudo <username>

# to check DistroName
> wsl -list -all

# to verify
> groups <username>
