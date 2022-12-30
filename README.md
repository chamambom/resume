# Martin Chamambo

_Cloud Operations Engineer (sometimes i wear my data analyst hat) based in Wellington, New Zealand_ <br>

[Email](mailto:chamambom@gmail.com.com) / [Website](https://cubem.co.zw/) / [LinkedIn](https://www.linkedin.com/in/chamambom/) / [GitHub](https://github.com/chamambom/) / [Twitter](https://twitter.com/chamambom/)

## 🏆 Projects | Accomplishments
_This section accounts for some of my high value (reducing cost and operational complexity) projects where i made an impact ._
<br>
<hr style="border:1px solid gray"> </hr>

**Organisation** - [Irvines Group | Sourthen Africa  ](https://www.irvinesafrica.com/)<br>
**Existing Environment** - Irvines Group has operations in SouthAfrica , Botswana ,Zambia ,Mozambique and Zimbabwe running various business applications 
(HR management software ,ERP automatica running on either HyperV or Physical servers. Various sites are running either a Sophos or a Mikrotik firewall). <br>
**Requirements. Planned Changes** - Develop a cloud adoption framework and migration roadmap. Consolidate (using azure migrate) existing applications while maintaining a hybrid environment 
using IPSec VPNs to facilitate a gradual migration using azure migrate to Azure. <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - We initially scoped the applications to be hosted on Azure SQL but we were faced with compatibility issues due to legacy code and 
 we settled for Azure SQL managed instance and SQL server (on a VM) which caters for an on-prem lift and shift.
 - Hybrid connectivity between Azure and irvines offices (with a mix of Mikrotiks and Sophos firewalls) - had overlapping subnets which needed to be changed. Additionally 
 because of teleworking , Irvines already had remote SSL VPNs configured for their users to connect to on-premise applications.Instead of configuring native azure P2S tunnels
  we extended traffic originating from the remote SSL vpn subnet into azure to reduce networking complexity .
 - Access requirements required that we centralise some applications didnt support AD authentication. <br>
 
 **References** - Dave Michie | [Email](mailto:davem@stratbt.co.za) <br>
 
 <hr style="border:1px solid gray"> </hr>
 
**Organisation** - [Liquid Intelligent Technologies | Zimbabwe](https://www.liquid.tech.co.zw/)<br>
**Existing Environment** - 2node VMware ESxi cluster designed for managed hosted services <br>
**Requirements. Planned Changes** To upgrade the VMware ESxi cluster by adding 10 more Dell M630 Blades/M1000e 
chassis serving ~ 6300 customers on a 1000 terabytes ISCSI SAN running 3x Dell Power Connect M6348 storage switches and 5x Dell PS 6610 EqualLogic arrays<br>
**Period** - Jan - Mar 2020 <br>
**Challenges Experienced** 
 - Maintenance and monitoring of storage and compute required dedicated resources. Most of the time active/standby controllers would fail affecting all VMs that have 
  their vmdks stored on that array. A power cycle of the VMs would be required as vms went into invalid or inconsistent states<br>
 
**References** - Lancelot Nyachoto |  [Email](mailto:LNyachoto@cassavasmartech.com) <br>

<hr style="border:1px solid gray"> </hr>

**Organisation** - [Cassava | Zimbabwe](https://www.cassavasmarttech.co.zw/)<br>
**Existing Environment** - With existing operations spanning econet and ecocash Zimbabwe , the data science department was formed to establish a unified analytics pla
tform using on-premises servers and 3rd party software. <br>
**Requirements. Planned Changes** To develop and implement a data strategy pipeline and provision a cloud based data analytic platform based on Azure databricks , Qliksense , Azure Data factory and Azure synapse<br>
**Period** - Jan - Mar 2020 <br>
**Challenges Experienced** 
 - Resources on azure had to connect to datasources located on-premise through IPSec VPNs. Some of the datasource endpoints keep going down. Resolved to implement a 
 data strategy where there are SLA agreements and boundaries of accountability for monitoring purposes.<br>
 
**References** - Lancelot Nyachoto |  [Email](mailto:LNyachoto@cassavasmartech.com) <br>

<hr style="border:1px solid gray"> </hr>

**Organisation** - [Zimbabwe Electricity Industry Pension Fund | Zimbabwe](https://www.zeipf.co.zw//)<br>
**Existing Environment** - Running business applications (SAP , Payroll app and Pension management software) on physical servers <br>
**Requirements. Planned Changes** - Develop and Implement a business continuity and disaster recover plan (BCDR) using Azure Site recovery. <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - Wrong scoping , Azure Site recovery supports Physical servers but some of the pre-requisites required for a successfull replication (Operating system disk count and Operating system disk size) 
  were overlooked only to be discovered when the project had started.We were forced to virtualize all the servers into HyperV and provided a temporary buffer server to
   aid the migration. 
 - Migration of the apps to the HyperV environment was manual and included engaging each vendor to verify if the application was compatible , which pushed the 
  project timelines even further.<br>
  
**References** - Simba Chavunduka [Email](mailto:simba@zesapf.co.zw ) <br>
 
 <hr style="border:1px solid gray"> </hr>
 
**Organisation** - [Econet Wireless |  Zimbabwe](https://www.econet.co.zw/)<br>
**Existing Environment** - Comprised of an environment running A cisco ASA at the edge , Intrusion Detection System, TMG , a proxy server, Ironport, Active Directory servers (4) and exchange 2013 servers (2 CAS and 6 Mailbox ) .The highly available setup comprised
 of 2385 mailboxes utilising a total of 10TB.  <br>
**Requirements. Planned Changes** - Migrate all mailboxes to O365 gradually using the hybrid move <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The datacenter network protecting the mail and AD servers was so complex , the existing team (which wasnt available when it was setup) , did not understand 
 all the network components involved. The network setup prevented the hybrid wizard to complete successfully. Microsoft documentation assumes that there are no 3rd party 
 components such as cisco spam filter in a successful hybrid scenario with exchange online - for email routing reasons.
 - Changes to the components of the network - allow exchange to communicate directly with exchange online required security experts (which we did not have) and a series of long 
 standing change requests. Tried to add O365 URLs and IPs on the firewall but there was a proxy and an IDS to also cater to. We ended up proposing doing a clean migration after 
 being advised by microsoft that the data was too much and would require breaking it down into chunks to move it.<br>
 
**References** - Adrin Muchatibaya | [Email](mailto:Adrin.Muchatibaya@econet.co.zw ), Tafadzwa Dzapasi [Email](mailto:tafadzwa.dzapasi@econet.co.zw )   <br>

 <hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Steward Bank |  Zimbabwe](https://www.stewardbank.co.zw/)<br>
**Existing Environment** On-premise environment comprised of 2 AD servers , 2 clustered 2016 exchange servers running all roles (CAS and Mailbox) ,Cisco iron port for 
 spam filtering<br>
**Requirements. Planned Changes** Migrate some users to exchange online and leave some users on-premise <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The exchange on-premise environment was unstable and kept corrupting the mailbox databases which affected the migration significantly.
 - After stabalising it , the assumption the customer had was that if the on-premise exchange servers are unreachable , it doesnt affect delivery.(email routing (mx) was 
 still pointing to their on-premise servers)<br>
 
**References** -Wellington Tsamasuo [Email](mailto:wellington.tsamasuo@stewardbank.co.zw) <br>
 <hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Edgars Pvt Ltd | Zimbabwe](https://www.edgars.co.zw/)<br>
**Existing Environment** - Environment comprised of exchange 2013 servers using mimecast for spam filtering <br>
**Requirements. Planned Changes** - Migrate all mailboxes to the cloud and still utilise mimecast for spam filtering. <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - My first hybrid setup , i never anticipated that having mimecast routing the emails (3rd party software) which is outside the perimeter network was going to complicate 
  my life. I was cautious but the email routing was confusing. The firewall was configured to block any spoofing attempts (mimecast trying to deliver same domain emails)
  originating outside the trusted IP block. We ended up configuring customer rules for different mail routing scenarios.<br>
  
**References** - Mbuso Ndlovu | [Email](mailto:M.Ndlovu@edgars.co.zw) <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Datlabs | Zimbabwe](https://www.datlabs.co.zw/)<br>
**Existing Environment**  Environment comprised of 2 Exchange 2013 servers and 2 Active Directory servers <br>
**Requirements. Planned Changes** - Configure a Hybrid setup for both AD and Exchange on-premise and migrate mailboxes for executives to the cloud and leave 
every other mailbox on-premise<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - After we were done testing all the email routing scenarios and moved a couple of test mailboxes  , the client had been sold a dummy. Account manager had told the client that even if the on-premise server
 goes down , email routing wont be affected. (MX records were not pointing to the cloud) <br>
 
**References** -  <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Zimre Holdings | Zimbabwe](https://www.zimre.co.zw/)<br>
**Existing Environment** - On-premise environment comprised of VMware servers running business applications. Some of the applications were intergrated to the on-premise AD
Sophos firewall for terminating Azure VPNs <br>
**Requirements. Planned Changes** -  Migrate all servers to the cloud and configure hybrid connnectivity using azure S2S and P2S <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The scoping did not cater for a robust identity solution , which forced us to migrate the AD to the cloud and keep seperate AD servers (On-premise and Clodu).Still feel
 like we could have done a better job.
 - Client had a lean team of I.T support personnel , which meant any changes required on the environment were sent to the service provider.<br>
 
**References** - Fadzanai E Mupandenyama [Email](mailto:FadzanaiMu@zimre.co.zw) <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Rainbow Tourism Group (RGT) | Zimbabwe](https://www.rtg.co.zw/)<br>
**Existing Environment** - https://gatewaystream.com/ hosted on AWS utilising cloudflare for traffic routing<br>
**Requirements. Planned Changes** - Application was hosted outside the country and was now required to be hosted in country for "whitelisting traffic" purposes.<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The environment (Azure Stack ) the app was migrated doesnt not have a resource that can support layer 7 loadbalancing capabilities (SSL offloading , Path redirection).
 We had to improvise the setup by terminating the SSL directly on the servers and utilising only a layer 4 loadbalancer. We could have proposed running a VM and running 
 a custom Nginx or HTTP proxy to offload the certificates but did not want to introduce uneccessary complexity into their already complex architecture. <br>
  
**References** - Taremeredzwa Chipepera [Email](mailto:taremeredzwa.ch@rtg.co.zw) <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Civil Aviation Authority Of Bostwana | Botswana](https://www.caab.co.bw/)<br>
**Existing Environment** - HyperV environment , ASA firewall , Physical servers<br>
**Requirements. Planned Changes** - Configured a disaster recovery (Azure Site Recovery (ASR)) and Azure Backup (MABS) setup to provide a remote BCDR plan as 
required by audit   <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - Felt like the setup was supposed to be a managed service - monitoring of server replication process , the coonfiguration server for physical servers and the on-premise microsoft backup server
 required someone with azure expertise. Client kept pushing requests to the vendor.<br>
 
**References** -  ontlametse tsumake | [Email](mailto:otsumake@caab.co.bw)  <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Morupule Coal Mine (MCM) | Botswana](https://www.mcm.co.bw/)<br>
**Existing On-premise Environment** - Enviroment comprised of business applications running on VMware <br>
**Requirements. Planned Changes** - Backup all servers to Azure<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - Client had other vendors (veeam and Solarwinds) also executing their backups which conflicted with Azure MABS software while trying to backup the same servers. Kept 
 getting stuck half way through. MABS was using the VMware vCenter API to connect to backup the server. We ended up backing up the servers by connecting directly to the
 server(s).<br>
 
**References** - Banachaba, Peter | [Email](mailto:pbanachaba@mcm.co.bw)   <br>
<hr style="border:1px solid gray"> </hr>
 
 **Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Enviroment comprised of decentralised bind servers where configurations were supposed to be done manually to all 4 servers 
for a single record<br>
**Requirements. Planned Changes** - Integrated 4 decentralised Bind DNS servers with facilemanager [http://www.facilemanager.com/]
 providing a single management interface for creating customer DNS records<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - We were running 4 bind servers and introducing facilemanager meant i had to recompile the bind servers replicating the same configuration. The process was too manual
  as our the existing zones contained errors.<br>
  
**References** - Abisai Matangira | [Email](mailto:matangiraa@afri-com.net)  | +263 8644004138 <br>
<hr style="border:1px solid gray"> </hr>
 
 
**Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Environment comprised operational and business support systems running on old commodity hardware (tower and rack servers). 
for a single record<br>
**Requirements. Planned Changes** - To consolidate applications and servers. Designed and implemented a 2 node KVM cluster on 2 Sun blades X6270/chassis 6000 
each with teamed interfaces connecting to 30 TBs of storage made from commodity hardware<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The initial setup lacked redundancy both from a compute and storage perspective <br>
 
**References** - Abisai Matangira | [Email](mailto:matangiraa@afri-com.net)  | +263 8644004138 <br>  <br>
<hr style="border:1px solid gray"> </hr>
 
## 📌 On The Side

🏳️‍🌈 **SentScore** - A sentiment analysis project utilising pandas , kafka , Twitter and MongoDB. [https://github.com/chamambom/SentScore]  _(Jan 2021 - Present)_<br>
🏳️‍🌈 Automated local .co.zw domain registrations [https://github.com/chamambom/regdns-txt] <br>
🏳️‍🌈 Automated subscriber network provisioning - [https://github.com/chamambom/python_to_text] <br>
🏳️‍🌈 Automated VMware instance deployment using puppet/foreman - [https://github.com/chamambom/mypuppet-lab]<br>
🏳️‍🌈 Standardised O365 and cloud services troubleshooting and deployment using ARM templates, PowerShell, GIT & terraform [https://github.com/chamambom/azure-terraform] 
<br>
  
<hr style="border:1px solid gray"> </hr>

## 🎤 Most Difficult customers (my testimonies)
🐻 Ever worked with a customer who has an I.T department which doesnt know how their applications ,network and servers are configured ? <br>
🐻 Customers with an I.T department reporting to the finance department ? where justification is required from the service provider on why we must do the project? <br>
🐻 Customers with that I.T Guy who will change stuff during project execution and when stuff stops working deny that he ever touched anything ? <br>
🐻 Customers with that I.T guy who doesnt pay attention during project execution - Only to take you back to square one during project handover? <br>
🐻 Customers who dont want to pay for a managed service support contract but will continue to bother you anyway and always get away with it ? <br>
🐻 Customers who always blame the service provider so as to get the service provider to do it for free ? <br>
🐻 Customers who are so deep in processes it takes months to get access to their environment to start a project ? <br>
🐻 Customers with a bureaucratic system where departments are so isolated - the service provider has to talk to each department to get stuff done ? <br>


🏳️‍🌈 **Well you are out of luck -  customer always wins - deal with it** 



<hr style="border:1px solid gray"> </hr>
  
## 💬 Languages

**English**: Proficient <br>
**Shona**: Native <br>
**Ndebele**: Native
<br><br>

## 👩🏼‍🎓 Education

**MSc In Data Analytics**  [Chinhoyi University Of Technology ](https://www.cut.co.zw/) - Chinhoyi, Zimbabwe _(Jan 2018 - Dec 2021)_ <br>

**BSc Honors In Computer Science** [University Of University](https://www.uz.ac.zw/) - Harare, Zimbabwe _(Aug 2006 - Jan 2010)_

**Redhat Certified Systems Enginer** | 140-045-378 | _(Feb 2014 - Feb 2017)_ <br>

**Redhat Certified Systems Administrator** | 140-045-378 |  _(Feb 2014 - Feb 2017)_ <br>

**Microsoft certified Azure Administrator** |MCID: 16595099 |  _(Nov 2020 - Nov 2022)_ <br>

**Microsoft certified Data Engineer**  | MCID: 16595099 | _(Sept 2020 - Sept 2022)_ <br>

**Microsoft certified Azure Security Engineer** | MCID: 16595099 | _(Jul 2021 - Jul 2023)_ <br>

**Microsoft certified Data Analyst** | MCID: 16595099 | _(Dec 2020 - Dec 2022)_ <br> 

**Microsoft certified Solutions Associate : O365**  | MCID: 16595099 | _(Dec 2018 - Present)_ <br>

**Cisco Certified Network Associate - CCNA**| CSCO12129589 | _(Mar 2012 - Mar 2015)_ <br>

**I.T.I.L Foundation certificate in IT Service management** | 4813045.1240312  | _(Aug 2013 - Present)_ <br>

**VMware Certified Associate Cloud** | VMW-01279212C-00417295 | _(Dec 2013 - Present)_ <br>

**VMware Certified Associate (Datacentre Virtualisation)** | VMW-01279212C-00417295| _(Nov 2013 - Present)_ <br> 

