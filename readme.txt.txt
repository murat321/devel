netstat -a ile t�m TCP ve UDP ba�lant�lar�n� getirdi
netstat -r ile IP y�nlendirme tablosunun i�eri�ini getirdi

Get-WmiObject -Class Win32_Desktop -ComputerName .
ile Masa�st� ayarlar�n� getirdi

Get-WmiObject -Class Win32_BIOS -ComputerName . ile Bios bilgilerini getirdi
 
Get-WmiObject -Class Win32_Processor -ComputerName . | Select-Object -Property [a-z]* ile  ��lemci bilgisini getirdi


Get-WmiObject -Class Win32_OperatingSystem -ComputerName . | Select-Object -Property 		 				BuildNumber,BuildType,OSType,ServicePackMajorVersion,ServicePackMinorVersion   ile  ��letim sistemi s�r�m bilgisini getirdi 

Get-WmiObject -Class Win32_OperatingSystem -ComputerName . | Select-Object -Property 						NumberOfLicensedUsers,NumberOfUsers,RegisteredUser  ile kullan�c� bilgilerini getirdi

Get-WmiObject �Class win32_computersystem ile domain ,ram ve �retici firma hakk�ndaki bilgileri getirdi  

schtasks | Where-Object { $_ -Match "Ready*" -or $_ -Match "Running*"} ile schedule tasklar�n� getirdi

Get-WmiObject -Class Win32_LogonSession -ComputerName . -- ile oturum a�m�� kullan�c�lar�n listesini getirdi

get-wmiobject win32_group  ile  Grup hakk�nda bilgileri getirdi

Get-ADDomainController  ile dc hakk�ndaki bilgileri getirdi
