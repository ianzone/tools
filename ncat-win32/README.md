CMD RUN AS ADMIN
```
C:\"Program Files (x86)"\"Microsoft Visual Studio"\2019\Community\VC\Auxiliary\Build\vcvars32.bat
choco install svn
choco install nasm
powershell -nop
[environment]::SetEnvironmentvariable("PATH", "$([environment]::GetEnvironmentvariable("Path", "Machine"));C:\Program Files\NASM\", "Machine")
exit
nasm --version
choco install strawberryperl
perl --version
cpan -i Text::Template
cd C:\
mkdir ncat
cd ncat
svn checkout https://svn.nmap.org/nmap-mswin32-aux
curl https://www.openssl.org/source/openssl-1.1.1k.tar.gz -o openssl.tgz
tar -xf openssl.tgz
mkdir OpenSSL
cd openssl-OpenSSL*
perl Configure --prefix=C:\OpenSSL enable-weak-ssl-ciphers enable-ssl3 enable-ssl3-method VC-WIN32 no-shared
perl -pi -e "s|/debug|/NXCOMPAT /DYNAMICBASE /SAFESEH| if /^LDFLAGS/" makefile
nmake -f makefile install_dev
copy .\ms\applink.c ..\OpenSSL\include\openssl
cd ..
rmdir /s /q .\nmap-mswin32-aux\OpenSSL
move OpenSSL nmap-mswin32-aux
curl https://nmap.org/dist/nmap-7.91.tgz -o nmap.tgz
tar -xf nmap.tgz
nmap-7.91\mswin32\nmap.sln
```
START FROM https://secwiki.org/w/Nmap/Ncat_Portable "Build Ncat Statically 4."
