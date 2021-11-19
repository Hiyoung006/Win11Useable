##### 0x01 请使用管理员运行批处理脚本：

setwin10right.bat 			    >>切换到旧版右键菜单：

setwin10explorer.bat		  >>恢复回Win11右键菜单

returnwin11explorer.bat	>>切换到旧版explorer：

returnwin11right.bat    	   >>恢复新版explorer:

<u>切换explorer后需要重启系统方可生效！</u>

##### 0x02 管理员运行cmd,执行相关命令：

切换到旧版右键菜单：

`reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve`
`taskkill /f /im explorer.exe & start explorer.exe`

恢复回Win11右键菜单：

`reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f`
`taskkill /f /im explorer.exe & start explorer.exe`



切换到旧版explorer：

`reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Shell Extensions\Blocked" /f /v {e2bf9676-5f8f-435c-97eb-11607a5bedf7} /t REG_SZ`

恢复新版explorer:
`reg delete "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Shell Extensions\Blocked" /f`