##Autom-Enroll already Azure AD Joined devices without any user interaction.

if((Test-Path -LiteralPath "HKLM:\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\MDM") -ne $true) {  New-Item "HKLM:\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\MDM" -force -ea SilentlyContinue };
New-ItemProperty -LiteralPath 'HKLM:\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\MDM' -Name 'AutoEnrollMDM' -Value 1 -PropertyType DWord -Force -ea SilentlyContinue;
New-ItemProperty -LiteralPath 'HKLM:\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\MDM' -Name 'UseAADCredentialType' -Value 1 -PropertyType DWord -Force -ea SilentlyContinue;

& $env:WINDIR\system32\deviceenroller.exe /c /AutoEnrollMDM
