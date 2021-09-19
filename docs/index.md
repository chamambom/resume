# Martin Chamambo

_Cloud Operations Engineer (Sometimes wear my data analyst hat) based in Harare, Zimbabwe_ <br>

[Email](mailto:chamambom@gmail.com.com) / [Website](https://cubem.co.zw/) / [LinkedIn](https://www.linkedin.com/in/chamambom/) / [GitHub](https://github.com/chamambom/) / [Twitter](https://twitter.com/chamambom/)

## 👩🏼‍💻 Technical Experience 


**Lead Cloud Operations Engineer - Southern Africa** @ [Liquid Intelligent Technologies](https://liquid.tech) _(Aug 2015 - Present)_ <br>

Hired to lead a remote team of 4 cloud engineers operating in Southern Africa (Zambia ,Botswana , Zimbabwe , DRC) to support customers in their cloud adoption journeys by developing end to end cloud migration roadmaps from planning ,implementation and support, doubling as a systems engineer in Zimbabwe (resident country) on the day-to-day support of business and operational support systems (BSS & OSS) running on-premise.
<br>

- - -

**Service Management Engineer** @ [Africom Pvt Ltd](https://africom.co.zw/) _(Jul 2013 - Jul 2015)_ <br>

Hired as part of a 10 member “24x7 on-call rotation team” to enhance service delivery using ITIL best practices by proactively monitoring and improving the reliability of network services and infrastructure.
<br>
- - -
**Network Operations Engineer** @ [Dandemutande Pvt Ltd](https://www.dandemutande.co.zw/) _(Jul 2012 - Jun 2013)_ <br>
Hired as part of a 5 member “24x7 on-call rotation team” to support onsite engineers , monitor and configure network services for customers. 
<br>
- - -

**Systems Administrator** @ [University Of Zimbabwe - Department of Community Medicine](https://www.uz.ac.zw/index.php?option=com_content&view=article&id=356&Itemid=961/) _(Apr 2009 - Feb 2012)_ <br>

Hired to work with Java and C# developers to support health management information systems for humanitarian programmes carried out under the Ministry of Health and Child Care (MoHCC) with support from various donors.
 <br>
 - - -   
## 🏆 Projects | Accomplishments
_This section accounts for some of my high value (reducing cost and operational complexity) projects where i made an impact ._
<br>

 **Organisation** - [Rainbow Tourism Group (RGT) | Zimbabwe](https://www.rtg.co.zw/)<br>
**Existing Environment** - https://gatewaystream.com/ hosted on AWS configured to use cloudflare for traffic routing<br>
**Requirements. Planned Changes** - Application was hosted outside the country and was now required to be hosted in country for GDPR and "whitelisting traffic" purposes.<br>
**Duration** - 1 month <br>
**Challenges Experienced** 
 - The environment (Azure Stack ) the app was migrated to did not have a resource that can support regional layer 7 loadbalancing capabilities (SSL offloading , Path redirection).
 We had to improvise the setup by terminating the SSL directly on the servers and utilising only a layer 4 loadbalancer. 
 - **Update** - after looking at azure front door , we realised it was able to support traffic routing to endpoints configured outside azure. We re-architected the solution
 to incorporate azure front door. 
  <br>
  
**References** -<br>

- - -
**Organisation** - [Irvines Group | Sourthen Africa  ](https://www.irvinesafrica.com/)<br>
**Existing Environment** - Irvines Group has operations in SouthAfrica , Botswana ,Zambia ,Mozambique and Zimbabwe. Their business applications 
(HR management software ,ERP automatica , Inventory management software etc) where decentralised around their regional sites running on-premise.SQL express was the main database backend. The underlying virtual infrastructurea was a mix of HyperV ,VMware and some physical servers here and there. Connectivity wise, all 5 sites either had a Sophos or a Mikrotik firewall that had Site to Site VPNs for office to office access and SSL VPNs for their employees while working from home. To streamline their servers and with most of their employees working remotely , irvines decided to centralise their operations by migrating to Azure<br>
**Requirements. Planned Changes** - Develop a cloud migration roadmap. Use the cloud rationalization framework to consolidate and migrate existing servers and applications while maintaining a hybrid environment using IPSec VPNs to facilitate a gradual migration to Azure. For user access , existing remote SSL vpns terminating on the sophos and mikrotiks were extended/routed to azure via the IPSec VPNs.  
<br>
**Duration** - 6 months <br>
**Challenges Experienced** 
 - We initially scoped the applications to be hosted on Azure SQL but most applications werent compatible when we ran azure migate due to legacy code and 
 we settled for Azure SQL managed instance and SQL server express (on a VM).
 - Hybrid connectivity between Azure and irvines offices (with a mix of Mikrotiks and Sophos firewalls) - had overlapping subnets which needed to be changed. Additionally 
 because of teleworking , Irvines already had remote SSL VPNs configured for their users to connect to on-premise applications.Instead of configuring native azure P2S tunnels
  we extended traffic originating from the remote SSL vpn subnet into azure to reduce networking complexity .
 - Identity access requirements required that we centralise application access. Some applications didnt support AD authentication until they were upgraded.<br>
 
 **References** - <br>
 
- - -
 
**Organisation** - [Liquid Intelligent Technologies | Zimbabwe](https://www.liquid.tech.co.zw/)<br>
**Existing Environment** - 2 VMware Esxi nodes configured independently of each other using direct attached storage designed for managed hosted services <br>
**Requirements. Planned Changes** To upgrade the VMware ESxi environment and convert the existing nodes into a cluster by adding 10 more Dell M630 Blades/M1000e 
chassis , a 1000 terabytes ISCSI SAN running 3x Dell Power Connect M6348 storage switches and 5x Dell PS 6610 EqualLogic arrays<br>
**Duration** - 4 months <br>
**Challenges Experienced** 
 - Maintenance and monitoring of storage and compute required dedicated resources. Most of the time active/standby storage controllers would fail affecting all VMs that have 
  their vmdks stored on that array. A power cycle of the VMs would be required as vms went into invalid or inconsistent states<br>
 
**References** - <br>

- - -

**Organisation** - [Cassava | Zimbabwe](https://www.cassavasmarttech.co.zw/)<br>
**Existing Environment** - With existing operations spanning econet and ecocash Zimbabwe , the data science team was formed to establish a unified analytics pla
tform using on-premises servers and 3rd party software. <br>
**Requirements. Planned Changes** To develop and implement strategies for data ingestion and intergration of existing ETL pipelines with azure based services - Azure databricks , Qliksense , Azure Data factory and Azure synapse<br>
**Duration** -2 months <br>
**Challenges Experienced** 
 - Resources on azure had to connect to datasources located on-premise through IPSec VPNs. Azure data factory was too expensive we ended up replacing it with SQL cron jobs. 
 Some of the datasource endpoints kept going down. Resolved to implement a data strategy that included SLA agreements and robust endpoint monitoring to establish boundaries of accountability.<br>
 **References** - <br>

- - -

**Organisation** - [Zimbabwe Electricity Industry Pension Fund | Zimbabwe](https://www.zeipf.co.zw//)<br>
**Existing Environment** - Running business applications (SAP , Payroll app and Pension management software) on physical servers <br>
**Requirements. Planned Changes** - Develop and Implement a business continuity and disaster recover plan (BCDR) using Azure Site recovery. <br>
**Duration** - 3 months <br>
**Challenges Experienced** 
 - Wrong scoping , Azure Site recovery supports Physical servers but some of the pre-requisites required for a successfull replication (Operating system disk count and Operating system disk size) 
  were overlooked only to be discovered when the project had started.We were forced to virtualize all the servers into HyperV and provided a temporary buffer server to
   aid the migration. 
 - Migration of the apps to the HyperV environment was manual and included engaging each vendor to verify if the application was compatible , which pushed the 
  project timelines even further.<br>
  
**References** - <br>

 - - -
**Organisation** - [Econet Wireless |  Zimbabwe](https://www.econet.co.zw/)<br>
**Existing Environment** - Comprised of an environment running A cisco ASA at the edge , Intrusion Detection System, TMG , a proxy server, Ironport, Active Directory servers (4) and exchange 2013 servers (2 CAS and 6 Mailbox ) .The highly available setup comprised of 2385 mailboxes with a total of 10TB.  <br>
**Requirements. Planned Changes** - Migrate all mailboxes to O365 gradually using the hybrid method <br>
**Duration** - 8 months  <br>
**Challenges Experienced** 
 - The datacenter network protecting the mail and AD servers was so complex , the existing team (which wasnt available when it was setup) , did not understand 
 all the network components involved. The network setup prevented the hybrid wizard to complete successfully. For a susccessful hybrid migration , Microsoft documentation states that no 3rd party components such as cisco spam filter should exist between exchange online and exchange on-premise - for email routing reasons.
 - Changes to the components of the network - allow exchange to communicate directly with exchange online required security experts (which we did not have) and a series of long 
 standing change requests. Tried to add O365 URLs and IPs on the firewall but there was a proxy and an IDS to also consider. In the end ,we did a clean migration after 
 being advised by microsoft that the data was too much and would require breaking it down into chunks to move it.<br>
 
 **References** - <br>
- - -
 
 **Organisation** - [Steward Bank |  Zimbabwe](https://www.stewardbank.co.zw/)<br>
**Existing Environment** On-premise environment comprised of 2 AD servers , 2 clustered 2016 exchange servers running all roles (CAS and Mailbox) ,Cisco iron port for 
 spam filtering<br>
**Requirements. Planned Changes** Implement a hybrid identity and email - Migrate some users to exchange online and leave some users on-premise <br>
**Duration** - 2 months <br>
**Challenges Experienced** 
 - The exchange on-premise environment was unstable and kept corrupting the mailbox databases which affected the migration significantly.
 - After stabalising it , the assumption the customer had was that if the on-premise exchange servers are unreachable , it doesnt affect delivery.(email routing (mx) was 
 still pointing to their on-premise servers)<br>
 
**References** - <br>
- - -
 
 **Organisation** - [Edgars Pvt Ltd | Zimbabwe](https://www.edgars.co.zw/)<br>
**Existing Environment** - Environment comprised of exchange 2013 servers using mimecast for spam filtering <br>
**Requirements. Planned Changes** - Implement hybrid identity and migrate all mailboxes to the cloud and still utilise mimecast for spam filtering. <br>
**Duration** - 1 month<br>
**Challenges Experienced** 
 - This was the first hybrid project that i executed.I failed to anticipate the following 
   - Mimecast for spam filtering and routing of emails - was outside the perimeter network
   - 3rd party software for spam filtering and routing of emails   
   
 - Because of the complicated email routing rules that were required,  i made sure i tested all email routing scenarios by migrating test accounts only to 
   satisfy all email routing scenarios before doing the final migration. The firewall was configured to block any spoofing attempts (mimecast trying to deliver same domain emails)  originating outside the 
   trusted IP block. We ended up configuring custom rules for different mail routing scenarios.<br>
  
**References** - <br>
- - -
 
 **Organisation** - [Datlabs | Zimbabwe](https://www.datlabs.co.zw/)<br>
**Existing Environment**  Environment comprised of 2 Exchange 2013 servers and 2 Active Directory servers <br>
**Requirements. Planned Changes** - Configure a Hybrid setup for both AD and Exchange on-premise and migrate mailboxes for executives to the cloud and leave 
every other mailbox on-premise<br>
**Duration** - 1 month <br>
**Challenges Experienced** 
 - After we had tested all email routing scenarios and moved a couple of test mailboxes  , all this time the client believed that hybrid email and identity
 will work even if one end is down. MX records were still pointing to exchange on-premise ,a decision we made based on the number of users left on-premise.
 - We tried to explain to the client why it wasnt possible , but we lost the client eventually.
 <br>
 
**References** -  <br>
- - -
 
 **Organisation** - [Zimre Holdings | Zimbabwe](https://www.zimre.co.zw/)<br>
**Existing Environment** - Has operations in SouthAfrica , Botswana ,Zambia ,Mozambique and Zimbabwe. All core applications 
where centralised in their Zimbabwe HQ. Zimbabwe On-premise environment comprised of VMware servers running these business applications. Some of the applications were intergrated 
to the on-premise AD. All their 5 sites were using Sophos firewall at the edge<br>
**Requirements. Planned Changes** -  Migrate all core applications to the cloud and configure hybrid connectivity using azure S2S and P2S <br>
**Duration** - 2 months  <br>
**Challenges Experienced** 
 - The scoping done by the solution architect did not cater for a robust identity solution , which forced us to migrate the AD to the cloud and keep separate 
 AD servers (On-premise and Cloud). Upon project completion client was happy with the setup but still felt like we could have done a better job around centralising 
 their identity.
 - Client had a lean team of I.T support personnel , which meant any changes required on the environment were sent to the service provider.<br>
 
**References** - <br>
- - - 

 
 **Organisation** - [Civil Aviation Authority Of Bostwana | Botswana](https://www.caab.co.bw/)<br>
**Existing Environment** - HyperV environment , ASA firewall , Physical servers<br>
**Requirements. Planned Changes** - Configured a disaster recovery (Azure Site Recovery (ASR)) and Azure Backup (MABS) setup to provide a remote BCDR plan as 
required by audit   <br>
**Duration** - 3 months <br>
**Challenges Experienced** 
 - Monitoring of the server replication process , the configuration server for physical servers and the on-premise microsoft backup server
 required someone with azure expertise. Client kept pushing requests to the vendor. Felt like this was supposed to be a managed service but client was 
 having non of it<br>
 
**References** -  <br>

- - -
 
 **Organisation** - [Morupule Coal Mine (MCM) | Botswana](https://www.mcm.co.bw/)<br>
**Existing On-premise Environment** - Environment comprised of business applications running on VMware <br>
**Requirements. Planned Changes** - Backup all 24 servers to Azure<br>
**Duration** - 3 months <br>
**Challenges Experienced** 
 - Client had other vendors (veeam and Solarwinds) also executing their backups which conflicted with Azure MABS software while trying to backup the same servers. Backups 
 kept getting stuck half way through. MABS was using the VMware vCenter API to connect to backup the server. We ended up backing up the servers by connecting directly to the
 server(s).<br>
 
**References** - <br>
- - - 
 **Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Environment comprised of decentralised bind servers where configurations were supposed to be done manually to all 4 servers 
for a single record<br>
**Requirements. Planned Changes** - Integrated 4 decentralised Bind DNS servers with facilemanager [http://www.facilemanager.com/]
 providing a single management interface for creating customer DNS records<br>
**Duration** - 1 month <br>
**Challenges Experienced** 
 - We were running 4 bind servers and introducing facilemanager meant i had to recompile the bind servers replicating the same configuration. The process was too manual
  as most of our existing zones contained errors.<br>
  
**References** - <br>

- - - 
 
**Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Environment was comprised of operational and business support systems running on old commodity hardware (tower and rack servers). 
<br>
**Requirements. Planned Changes** - To consolidate applications and servers. Designed and implemented a 2 node KVM cluster on 2 Sun blades X6270/chassis 6000 
each with teamed interfaces connecting to 30 TBs of storage (managed by openfiler) made from commodity hardware<br>
**Duration** - 2 month <br>
**Challenges Experienced** 
 - The initial setup lacked redundancy both from a compute and storage perspective so we made use of a robust backup strategy
 - There was no firewall protecting the VMs , all rules were managed directly on the server. 
<br>
 
**References** - <br>

- - -
 
## 📌 On The Side

- **SentScore** - A sentiment analysis project utilising pandas , kafka , Twitter and MongoDB. [https://github.com/chamambom/SentScore]  _(Jan 2021 - Present)_<br>
- Automated local .co.zw domain registrations [https://github.com/chamambom/regdns-txt] <br>
- Automated subscriber network provisioning - [https://github.com/chamambom/python_to_text] <br>
- ‍Automated VMware instance deployment using puppet/foreman - [https://github.com/chamambom/mypuppet-lab]<br>
- Standardised O365 and cloud services troubleshooting and deployment using ARM templates, PowerShell, GIT & terraform [https://github.com/chamambom/azure-terraform] 
<br>
  


## 🎤 Types of difficult customers
- A customer who has an I.T department which which isnt familiar with how their applications ,network and servers are configured ? <br>
- Customers with an I.T department reporting to the finance department ? everything is about cost ? <br>
- Customers with that I.T Guy who will change configurations during project execution and when it stops working deny that he ever touched anything ? <br>
- Customers with that I.T guy who doesnt pay attention during project execution - Only to take you back to square one during project handover? <br>
- Customers who dont want to pay for a managed service support contract but will continue to bother you anyway and always get away with it ? <br>
- Customers who always blame the service provider so as to get the service provider to do it for free ? <br>
- Customers who are so deep in processes it takes months to get access to their environment to start a project ? <br>
- Customers with a bureaucratic system where departments are so isolated - you have to initiate communications to each department to get anything done ? <br>

💖 **Well you are out of luck -  customer always wins - deal with it** 

- - -
## 💬 Languages

**English**: Proficient <br>
**Shona**: Native <br>
**Ndebele**: Native
<br><br>
- - -
## 👩🏼‍🎓 Education

**MSc In Data Analytics**  [Chinhoyi University Of Technology ](https://www.cut.co.zw/) - Chinhoyi, Zimbabwe _(Jan 2018 - Dec 2021)_
- - -
**BSc Honors In Computer Science** [University Of University](https://www.uz.ac.zw/) - Harare, Zimbabwe _(Aug 2006 - Jan 2010)_
- - -
**Redhat Certified Systems Engineer** | 140-045-378 | _(Feb 2014 - Feb 2017)_
- - -
**Redhat Certified Systems Administrator** | 140-045-378 |  _(Feb 2014 - Feb 2017)_
- - -
**Microsoft certified Azure Solutions Expert** |MCID: 16595099 |  _(Sept 2021 - Sept 2022)_
- - -
**Microsoft certified Azure Administrator** |MCID: 16595099 |  _(Nov 2020 - Nov 2022)_
- - -
**Microsoft certified Data Engineer**  | MCID: 16595099 | _(Sept 2020 - Sept 2022)_
- - -
**Microsoft certified Azure Security Engineer** | MCID: 16595099 | _(Jul 2021 - Jul 2023)_
- - -
**Microsoft certified Data Analyst** | MCID: 16595099 | _(Dec 2020 - Dec 2022)_
- - -
**Microsoft certified Solutions Associate : O365**  | MCID: 16595099 | _(Dec 2018 - Present)_
- - -
**Cisco Certified Network Associate - CCNA**| CSCO12129589 | _(Mar 2012 - Mar 2015)_ 
- - -
**I.T.I.L Foundation certificate in IT Service management** | 4813045.1240312  | _(Aug 2013 - Present)_
- - -
**VMware Certified Associate Cloud** | VMW-01279212C-00417295 | _(Dec 2013 - Present)_
- - -
**VMware Certified Associate (Datacentre Virtualisation)** | VMW-01279212C-00417295| _(Nov 2013 - Present)_
- - -
