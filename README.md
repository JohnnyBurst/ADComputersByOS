To be run on DC hosting AD. Open elevated via a "right-click > Run As Administrator" on the powershell icon in the taskbar. Copy/paste script into window. Results should populate a 4 column table. Results are listed from Active Directory on host machine.

Display List: Returns all Windows Servers
Get-ADComputer -Filter {OperatingSystem -Like "Windows Server*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate

Saves "filename.csv" to c:\windows\System32
Get-ADComputer -Filter {OperatingSystem -Like "Windows 10*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | Export-csv AllWinServers.csv -NoTypeInformation -Encoding UTF8



Displays List: Returns all Windows 10
Get-ADComputer -Filter {OperatingSystem -Like "Windows 10*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate

Saves "filename.csv" to c:\windows\System32
Get-ADComputer -Filter {OperatingSystem -Like "Windows 10*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | Export-csv AllWin10.csv -NoTypeInformation -Encoding UTF8



Displays List: Returns all Windows 8 versions
Get-ADComputer -Filter {OperatingSystem -Like "Windows 8*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate

Saves "filename.csv" to c:\windows\System32
Get-ADComputer -Filter {OperatingSystem -Like "Windows 8*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | Export-csv AllWin8.csv -NoTypeInformation -Encoding UTF8



Displays List: Returns all Windows 7
Get-ADComputer -Filter {OperatingSystem -Like "Windows 7*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | 

Saves "filename.csv" to c:\windows\System32
Get-ADComputer -Filter {OperatingSystem -Like "Windows 7*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | Export-csv AllWin7.csv -NoTypeInformation -Encoding UTF8



Displays List: Returns all Windows XP
Get-ADComputer -Filter {OperatingSystem -Like "Windows XP*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate

Saves "filename.csv" to c:\windows\System32
Get-ADComputer -Filter {OperatingSystem -Like "Windows XP*"} -Property * | select-object Name,OperatingSystem,OperatingSystemServicePack,LastLogonDate | Export-csv AllWinXP.csv -NoTypeInformation -Encoding UTF8
