; autoit 스크립트 편집기를 사용하십시오.


RUN("control /name microsoft.networkandsharingcenter /page advanced")


Sleep(2000)
WINWAITACTIVE("고급 공유 설정")
Send("#{UP}")
Send("{UP}")
Send("{SPACE}")

Sleep(1000)
$hWnd = WinWaitActive("고급 공유 설정")
; 암호보호공유 인터페이스 136 켜기 138 끄기
ControlClick( $hWnd, "", "[CLASS:Button; INSTANCE:138]")
Sleep(500)
$hWnd = WinWaitActive("고급 공유 설정")
ControlClick( $hWnd, "", "[CLASS:Button; INSTANCE:141]")

;종료
$hWnd = WinWaitActive("고급 공유 설정")
Send("{esc}")
