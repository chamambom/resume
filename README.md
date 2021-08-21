# Martin Chamambo

_Cloud Operations Engineer (sometimes i wear my data analyst hat) based in Harare, Zimbabwe_ <br>

[Email](mailto:chamambom@gmail.com.com) / [Website](https://cubem.co.zw/) / [LinkedIn](https://www.linkedin.com/in/chamambom/) / [GitHub](https://github.com/chamambom/) / [Twitter](https://twitter.com/chamambom/)

## 👩🏼‍💻 Technical Experience 

**Lead Cloud Operations Engineer - Southern Africa** @ [Liquid Intelligent Technologies](https://liquid.tech) _(Aug 2015 - Present)_ <br>
Provides Network, Cloud and Cyber Security offerings through strategic partnerships with leading global players to the African continent.

Hired to lead a remote team of 4 cloud engineers operating in Southern Africa (Zambia ,Botswana , Zimbabwe , DRC) to support customers in their cloud adoption 
journeys by developing end to end cloud migration roadmaps from planning ,implementation and support, doubling as an on-premise 
systems engineer in the resident country on the day-to-day support of business and operational support systems (BSS & OSS).
<br><br>

**Service Management Engineer** @ [Africom Pvt Ltd](https://africom.co.zw/) _(Mar 2012 - July 2015)_ <br>
Telecommunications service provider that provides converged communication and hosting solutions.

Hired as part of a 6 member “24x7 on-call rotation team” within the Network Operations Centre (NOC) to ensure the reliability of network services 
through automated monitoring systems & ITIL compliant service delivery processes.
<br><br>

**Systems Administrator** @ [University Of Zimbabwe | Department of Community Medicine](https://www.uz.ac.zw/index.php?option=com_content&view=article&id=356&Itemid=961) _(Apr 2009 - Feb 2012)_ <br>
Part of a team hired to be part of a humanitarian project operating within the boundaries of the department of the community medicine.

Hired to support web based database systems and mobile data collection for humanitarian programmes carried out under 
  the Ministry of Health and Child Care (MoHCC) with support from various donors.
 <br>
    
## 🏆 Projects | Accomplishments
_This section accounts for all high value projects where i made an impact._
<br><br>
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
 **Reference** - Dave Michie | [Email](mailto:davem@stratbt.co.za) <br>

**Organisation** - [Cassava | Zimbabwe](https://www.cassavasmarttech.co.zw/)<br>
**Existing Environment** - With existing operations spanning econet and ecocash Zimbabwe , the data science department was formed to establish a unified analytics pla
tform using on-premises servers and 3rd party software. <br>
**Requirements. Planned Changes** To develop and implement a data strategy pipeline and provision a cloud based data analytic platform based on Azure databricks , Qliksense , Azure Data factory and Azure synapse<br>
**Period** - Jan - Mar 2020 <br>
**Challenges Experienced** 
 - Resources on azure had to connect to datasources located on-premise through IPSec VPNs. Some of the datasource endpoints keep going down. We have resolved to implement a 
 data strategy where there are SLA agreements and boundaries of accountability for monitoring purposes.<br>
 **Reference** - Lancelot Nyachoto |  [Email](mailto:LNyachoto@cassavasmartech.com) <br>

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
 **Reference** - Simba Chavunduka [Email](mailto:simba@zesapf.co.zw ) <br>
 
**Organisation** - [Econet Wireless |  Zimbabwe](https://www.econet.co.zw/)<br>
**Existing Environment** - Comprised of an environment running A cisco ASA at the edge , Intrusion Detection System, TMG , a proxy server, Ironport, Active Directory servers (4) and exchange 2013 servers (2 CAS and 6 Mailbox ) .The highly available setup comprised
 of 2385 mailboxes utilising a total of 10TB.  <br>
**Requirements. Planned Changes** - Migrate all mailboxes to O365 gradually using the hybrid move <br> <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The datacenter network protecting the mail and AD servers was so complex , the existing team (which wasnt available when it was setup) , did not understand 
 all the network components involved. The network setup prevented the hybrid wizard to complete successfully. Microsoft documentation assumes that there are no 3rd party 
 components such as cisco spam filter in a successful hybrid scenario with exchange online - for email routing reasons.
 - Changes to the components of the network - allow exchange to communicate directly with exchange online required security experts (which we did not have) and a series of long 
 standing change requests. Tried to add O365 URLs and IPs on the firewall but there was a proxy and an IDS to also cater to. We ended up proposing doing a clean migration after 
 being advised by microsoft that the data was too much and would require breaking it down into chunks to move it.<br>
 **References** - Adrin Muchatibaya | [Email](mailto:Adrin.Muchatibaya@econet.co.zw ), Tafadzwa Dzapasi [Email](mailto:tafadzwa.dzapasi@econet.co.zw )   <br>
 
 **Organisation** - [Steward Bank |  Zimbabwe](https://www.stewardbank.co.zw/)<br>
**Existing Environment** On-premise environment comprised of 2 AD servers , 2 clustered 2016 exchange servers running all roles (CAS and Mailbox) ,Cisco iron port for 
 spam filtering<br>
**Requirements. Planned Changes** Migrate some users to exchange online and leave some users on-premise <br> <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The exchange on-premise environment was unstable and kept corrupting the mailbox databases which affected the migration significantly.
 - After stabalising it , the assumption the customer had was that if the on-premise exchange servers are unreachable , it doesnt affect delivery.(email routing (mx) was 
 still pointing to their on-premise servers)<br>
 -
 **Reference** -Wellington Tsamasuo [Email](mailto:wellington.tsamasuo@stewardbank.co.zw) <br>
 
 **Organisation** - [Edgars Pvt Ltd | Zimbabwe](https://www.edgars.co.zw/)<br>
**Existing Environment** - Environment comprised of exchange 2013 servers using mimecast for spam filtering <br>
**Requirements. Planned Changes** - Migrate all mailboxes to the cloud and still utilise mimecast for spam filtering. <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - My first hybrid setup , i never anticipated that having mimecast routing the emails (3rd party software) which is outside the perimeter network was going to complicate 
  my life. I was cautious but the email routing was confusing. The firewall was configured to block any spoofing attempts (mimecast trying to deliver same domain emails)
  originating outside the trusted IP block. We ended up configuring customer rules for different mail routing scenarios.<br>
 
 **Reference** - Mbuso Ndlovu | [Email](mailto:M.Ndlovu@edgars.co.zw) <br>
 
 **Organisation** - [Datlabs | Zimbabwe](https://www.datlabs.co.zw/)<br>
**Existing Environment**  Environment comprised of 2 Exchange 2013 servers and 2 Active Directory servers <br>
**Requirements. Planned Changes** - Configure a Hybrid setup for both AD and Exchange on-premise and migrate mailboxes for executives to the cloud and leave 
every other mailbox on-premise<br> <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - After we were done testing all the email routing scenarios and moved a couple of test mailboxes  , the client had been sold a dummy. Account manager had told the client that even if the on-premise server
 goes down , email routing wont be affected. (MX records were not pointing to the cloud) <br>
 **Reference** -  <br>
 
 **Organisation** - [Zimre Holdings | Zimbabwe](https://www.zimre.co.zw/)<br>
**Existing Environment** - On-premise environment comprised of VMware servers running business applications. Some of the applications were intergrated to the on-premise AD
Sophos firewall for terminating Azure VPNs <br>
**Requirements. Planned Changes** -  Migrate all servers to the cloud and configure hybrid connnectivity using azure S2S and P2S <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The scoping did not cater for a robust identity solution , which forced us to migrate the AD to the cloud and keep seperate AD servers (On-premise and Clodu).Still feel
 like we could have done a better job.
 - Client had a lean team of I.T support personnel , which meant any changes required on the environment were sent to the service provider.<br>
 **Reference** - Fadzanai E Mupandenyama [Email](mailto:FadzanaiMu@zimre.co.zw) <br>
 
 **Organisation** - [Rainbow Tourism Group (RGT)](https://www.rtg.co.zw/)<br>
**Existing Environment** - https://gatewaystream.com/ hosted on AWS utilising cloudflare for traffic routing<br>
**Requirements. Planned Changes** - Application was hosted outside the country and was now required to be hosted in country for "whitelisting traffic" purposes.<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The environment (Azure Stack ) the app was migrated doesnt not have a resource that can support layer 7 loadbalancing capabilities (SSL offloading , Path redirection).
 We had to improvise the setup by terminating the SSL directly on the servers and utilising only a layer 4 loadbalancer. We could have proposed running a VM and running 
 a custom Nginx or HTTP proxy to offload the certificates but did not want to introduce uneccessary complexity into their already complex architecture. <br>
  
 **Reference** - Taremeredzwa Chipepera [Email](mailto:taremeredzwa.ch@rtg.co.zw) <br>
 
 **Organisation** - [Civil Aviation Authority Of Bostwana | BOSTWANA](https://www.caab.co.bw/)<br>
**Existing Environment** - HyperV environment , ASA firewall , Physical servers<br>
**Requirements. Planned Changes** - Configured a disaster recovery (Azure Site Recovery (ASR)) and Azure Backup (MABS) setup to provide a remote BCDR plan as required by audit   <br> <br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - Felt like the setup was supposed to be a managed service - monitoring of server replication process , the coonfiguration server for physical servers and the on-premise microsoft backup server
 required someone with azure expertise. Client kept pushing requests to the vendor.<br>
 **Reference** -  ontlametse tsumake | [Email](mailto:otsumake@caab.co.bw)  <br>
 
 **Organisation** - [Morupule Coal Mine (MCM) | BOTSWANA](https://www.mcm.co.bw/)<br>
**Existing On-premise Environment** - Enviroment comprised of business applications running on VMware <br>
**Requirements. Planned Changes** - Backup all servers to Azure<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - Client had other vendors (veeam and Solarwinds) also executing their backups which conflicted with Azure MABS software while trying to backup the same servers. Kept 
 getting stuck half way through. MABS was using the VMware vCenter API to connect to backup the server. We ended up backing up the servers by connecting directly to the
 server(s).<br>
 **Reference** - Banachaba, Peter | [Email](mailto:pbanachaba@mcm.co.bw)   <br>
 
 **Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Enviroment comprised of decentralised bind servers where configurations were supposed to be done manually to all 4 servers 
for a single record<br>
**Requirements. Planned Changes** - Integrated 4 decentralised Bind DNS servers with facilemanager [http://www.facilemanager.com/]
 providing a single management interface for creating customer DNS records<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - We were running 4 bind servers and introducing facilemanager meant i had to recompile the bind servers replicating the same configuration. The process was too manual
  as our the existing zones contained errors.<br>
**Reference** - Abisai Matangira | [Email](mailto:matangiraa@afri-com.net)  | +263 8644004138 <br>
 
 
**Organisation** - [Africom | Zimbabwe](https://www.africom.co.bw/)<br>
**Existing On-premise Environment** - Environment comprised operational and business support systems running on old commodity hardware (tower and rack servers). 
for a single record<br>
**Requirements. Planned Changes** - To consolidate applications and servers. Designed and implemented a 2 node KVM cluster on 2 Sun blades X6270/chassis 6000 
each with teamed interfaces connecting to 30 TBs of storage made from commodity hardware<br>
**Period** - Mar - Jul 2020 <br>
**Challenges Experienced** 
 - The initial setup lacked redundancy both from a compute and storage perspective <br>
**Reference** - Abisai Matangira | [Email](mailto:matangiraa@afri-com.net)  | +263 8644004138 <br>  <br>
 
## 📌 On The Side

**SentScore** _(Jan 2021 - Present)_<br>
🏳️‍🌈 A sentiment analysis project utilising pandas , kafka , Twitter and MongoDB.
  <br><br>


## 🎤 Most Difficult customers 
🐻 Customers who dont understand their own application , network and server configurations and the contribution to the complexity of the project especially in 
hybrid deployment scenarios <br>
🐻 customers with an I.T department reporting to the finance department - Most of the time , the I.T team is not technical <br>

  
## 💬 Languages

**English**: Proficient <br>
**Shona**: Native <br>
**Ndebele**: Native
<br><br>

## 👩🏼‍🎓 Education

**MSc In Data Analytics** Focused on Big Data Analytics and Machine Learning<br>
[Chinhoyi University Of Technology ](https://www.cut.co.zw/) - Chinhoyi, Zimbabwe _(Jan 2019 - Dec 2021)_ <br>

**BSc Honors In Computer Science** <br>
[University Of University](https://www.uz.ac.zw/) - Harare, Zimbabwe _(Aug 2006 - Jan 2010)_

**Redhat Certified Systems Enginer** | _(Jan 2019 - Dec 2021)_ <br>

**Redhat Certified Systems Administrator** | _(Jan 2019 - Dec 2021)_ <br>

**Microsoft certified Azure Administrator** | _(Jan 2019 - Dec 2021)_ <br>

**Microsoft certified Data Engineer**  | _(Jan 2019 - Dec 2021)_ <br>

**Microsoft certified Azure Security Engineer** | _(Jan 2019 - Dec 2021)_ <br>

**Microsoft certified Data Analyst** | _(Jan 2019 - Dec 2021)_ <br> 

**Microsoft certified Solutions Associate : O365**  | _(Jan 2019 - Dec 2021)_ <br>

**CCNA**| _(Jan 2019 - Dec 2021)_ <br>

**I.T.I.L Foundation certificate in IT Service management** | _(Jan 2019 - Dec 2021)_ <br>

**VMware Certified Associate Cloud** | _(Jan 2019 - Dec 2021)_ <br>

**VMware Certified Associate (Datacentre Virtualisation)**| _(Jan 2019 - Dec 2021)_ <br> 

