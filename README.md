# Project 7 - WordPress Pentesting

Time spent: 5 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. Username Enumeration
  - [ ] Summary: I used wpscan to find all the users for the wp website.
    - Vulnerability types: Username Enumeration
    - Tested in version: 4.1.00
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="UsernameEnumeration.gif" alt="Username Enumeration">
  - [ ] Steps to recreate: Run wpscan --url http://127.0.0.1:8080 --api-token ar6NfqrODSEXyb7JA3X8elecFcEumX2VTd6YSs4DE9k -e u vp in terminal.

### 2. Password Enumeration
  - [ ] Summary: I used wpscan to find all correct username and passoword combinations.
    - Vulnerability types: Password Enumeration
    - Tested in version: 4.1.00
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="PasswordEnumeration.gif" alt="Password Enumeration">
  - [ ] Steps to recreate: Populate passoword.txt and username.txt with username and passowrd combination. Then run wpscan --url http://127.0.0.1:8080 --         api-token ar6NfqrODSEXyb7JA3X8elecFcEumX2VTd6YSs4DE9k --usernames username.txt --passwords password.txt to find any matches.
  
### 3. Comment Cross-Site Scripting 
  - [ ] Summary: I created a post that manipulated HTML so that everytime someone visted a specific page alert was shown on the webpage. 
    - Vulnerability types: Comment Cross-Site Scripting 
    - Tested in version: 4.1.00
    - Fixed in version: 4.1.26
  - [ ] GIF Walkthrough: <img src="xss.gif" alt="Xss">
  - [ ] Steps to recreate: Add <svg onload=alert(1)> in text box to manipulate HTML.

## Assets

List any additional assets, such as scripts or files
  <img src="webscan.gif" alt="scan">


## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2022] [DeJa Barclay]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
