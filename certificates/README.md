# Certificates

How to generate self-signed CA and SSL certificates.

## Requirements:

* [Windows 10 SDK](https://developer.microsoft.com/pl-pl/windows/downloads/windows-10-sdk/)
  * makecert.exe
  * pvk2pfx.exe

## Usage

* CA Certificate - [see CreateCARoot.bat](/certificates/CreateCARoot.bat)

   ```shell
   CreateCARoot.bat [ca]
   # ca - your ca name
   ```

* SSL Certificate - [see CreateSSLCertificate.bat](/certificates/CreateSSLCertificate.bat)

   ```shell
   CreateSSLCertificate.bat [filename] [password] [cn]
   # filename - name under which files will be saved
   # password - certificate password
   # cn - certificate comma separated common names e.g. CN=computername.domain.com, CN=localhost, CN=computername
   ```

## Install Certificates (Windows)

* Open a Snap-in window
  * _Start_ -> _Run_ -> Type _mmc_
  * _Add/Remove Snap-in..._ (Ctrl-M)
  * Add a Certificates snap-in for _My user account_
* Expand the _Trusted Root Certification Authorities_ -> _Certificates_ node
* Right click the Certificates folder and choose _All Tasks_ –> _Import_
* Browse folders to find certificate you want to install.
* Import the certificate and click through the remaining windows and finish.
