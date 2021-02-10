# Honeypot Assignment

**Time spent:** 12Hrs hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.? <br/>
Two GCP instances were created. The first is callend mhn-admin to run the MHN-server. The second is called mhn-honeypot-1 which holds the three sensors: p0f, dionaea, snort. To verify that the configuration of the MHN-server and the sensors are set up correctly, I run the command ```sudo supervisorctl status```. I used GCP.

<img src="mhn-admin.gif" width ="400" height ="400">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do? <br/>
Dionaea's intention is to trap malware exploiting vulnerabilities exposed by services offerd to a network, the ultimate goal is gaining a copy of the malware.

<img src="dionaea-honeypot.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record? <br/>
-> RDBMS which was used MySQL, Microsoft SQL Server. JSON file record export of the data. <br/>

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*



## Notes

Click on star if you like :)

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
