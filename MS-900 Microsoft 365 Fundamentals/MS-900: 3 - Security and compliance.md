
# MS-900: Security and compliance
Study guide based on the following learning path: [Microsoft 365 Fundamentals: Demonstrate fundamental knowledge of Microsoft 365 security and compliance capabilities - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/paths/m365-security-compliance-capabilities/)


## Describe security and compliance concepts and methodologies

### Describe the zero-trust methodology
- 0-Trust:
	- Everything is on an open and untrusted network
	- “**trust no one, verify everything.**”

#### Zero Trust guiding principles
- Verify explicitly = use data points (user ID, location, device, service, workload...) to authenticate and authorize
- Least privileged access = Just-in-time and Just-enough-access (JIT/JEA)
- Assume breach = Segment network, encryption, analytics to detect threats
 
##### Six foundational pillars:
- Identities = users, services, or devices
- Devices = monitoring devices for health and compliance
- Applications = discovering all applications that are being used
- Data = classified, labeled, and encrypted
- Infrastructure = monitor on-premises or cloud based infra
- Networks = net segmentation, RT protection, End2End Encryption, monitoring

### Describe the shared responsibility model
- Used so that organizations are clear about their responsibilities, and those of the cloud provider.
![The Shared responsibility model responsibilities by type](https://docs.microsoft.com/en-us/learn/wwl-sci/describe-security-concepts-methodologies/media/3-shared-responsibility-model-responsibilites-type.png)

-  On-premises
	- Client: Responsibility for everything
- IaaS
	- Client: OSs, network controls, applications, and protecting data.
	- MS: Physical Infra
- PaaS
	- Client: applications, and protecting data.
	- MS: OSs, network controls, Physical Infra
- SaaS
	- MS: everything except data, devices, accounts, and identities.

In summary, responsibilities always retained by the customer organization include:
-   Information and data
-   Devices (mobile and PCs)
-   Accounts and identities

### Describe defense in depth
- Layered approach to security =  Each layer provides protection. If one layer is breached, a subsequent layer will prevent an attacker getting unauthorized access to data.

![Defense in depth uses multiple layers of security to protect sensitive data](https://docs.microsoft.com/en-us/learn/wwl-sci/describe-security-concepts-methodologies/media/4-defense-depth.png)

#### Confidentiality, Integrity, Availability (CIA)
![Confidentiality, Integrity, Availability (CIA)](https://docs.microsoft.com/en-us/learn/wwl-sci/describe-security-concepts-methodologies/media/4-confidentiality-integrity-availability.png)
- **Confidentiality**  = keep confidential sensitive data. encrypt data to keep it confidential
- **Integrity**  = keeping data or messages correct. data hasn't been tampered with or altered.
- **Availability**  = making data available to those who need it. 

### Describe common threats
- Data breach
	- Because of: phishing, spear phishing, tech support scams, SQL injection, and malware designed to steal passwords or bank details.
- Dictionary attack
	- aka; brute force attacks.
- Ransomware
	- encrypts files and folders
- Disruptive attacks = 
	- DDoS, exhausts an application's resources
	- coin miners, mines crypto on the devices
	- rootkits, intercept and change standard operating system processes.
	- trojans, uses common files to spread
	- worms, can copy itself and often spreads through a network
	- exploits/exploit kits, a weakness in your software that malware uses to get onto your device

### Describe ways encryption and hashing can secure your data
There are two top-level types of encryption:
- **Symmetric** = 1 key to encrypt and decrypt the data. 
- **Asymmetric** = a public key and private key pair. 
	- One encrypts, the other decrypts. 
	- Used in Transport Layer Security (TLS): :bulb:
		- HTTPS protocol, 
		- data signing. :star:

Encryption may protect data at rest, or in transit: 
- **At rest**
	- Data stored in a physical device, storage account, database...
	- Data is unreadable without the encryption key.
- **In transit**
	- Data is moving from one location to another. (internet, private network...)
	- Secure transfer, encryption at the application layer (ex: HTTPS) :star: :bulb:

**Hashing** uses an algorithm to convert the original text to a _unique_ fixed-length hash value.
- Used as a unique identifier of its associated data.
- You can't get the data from its hash. 
- Used to store passwords, verify files... :bulb:
- **Salted** Hashes: 
	- Hackers know most hashing algos
	- Adding a fixed-length random value to the input of hash functions to create unique hashes for every input. :bulb:

### Describe the Cloud Adoption Framework
= Documentation, implementation guidance, best practices, and tools designed to help businesses to implement strategies necessary to succeed in the cloud.
  ![The Cloud Adoption Lifecycle diagram.](https://docs.microsoft.com/en-us/learn/wwl-sci/describe-security-concepts-methodologies/media/6a-cloud-adoption-lifecycle-inline.png)
1.  **Strategy**: define business justification and expected outcomes of adoption.
2.  **Plan**: align actionable adoption plans to business outcomes.
3.  **Ready**: Prepare the cloud environment for the planned changes.
4.  **Adopt**
    -   **Migrate**: Migrate and modernize existing workloads.
    -   **Innovate**: Develop new cloud-native or hybrid solutions.
5.  **Govern**: Govern the environment and workloads.
6.  **Manage**: Operations management for cloud and hybrid solutions.


## Describe the identity and access management capabilities of Microsoft 365

### Describe Microsoft's Zero Trust model and the concepts of Identity and access management

 - Identity and access management (IAM)
	 - Verify **Identity** = credentials + **authentication** methods (like MFA) 
	 - **Access** Management = with tools like Conditional Access
		 - Assess the user and verify geographical location, the device they are connecting from, the app they used to make the connection, time of day
		 - Decide if the user is **authorized** to access. 
 - Hybrid identity
	 - Account created on AD DS **transferred/copied to Azure AD** tenant
	 - AD DS = authoritative source for account information
	 - Azure AD Connect synchronizes user accounts in Azure AD
 - Cloud identity
	 - accounts that exist **only in Azure AD**

 - Zero Trust security model
	 - “never trust, always verify.”
	 - Micro-segmentation = create secure zones to separate workloads, each of which can be secured.
- A Zero Trust model has three aspects.
	-   It requires  _**signals**_  to inform decisions.  = telemetry.
	-   Policies to make access  _**decisions**_. = finely tuned access policies.
	-   _**Enforcement**_  capabilities to implement those decisions.

### Manage identities and access in Microsoft 365 with Azure Active Directory
![Diagram showing the Conditional Access model](https://docs.microsoft.com/en-us/learn/wwl/describe-identity-access-management-capabilities-of-microsoft-365/media/3-conditional-access-overview-how-it-works.png)
- Conditional Access:
	- Evaluating users, devices, apps, location, and assessing the risk before granting access.
	- if-then statements and policies. 
#### 1. Conditional Access signal assessment
Common **signals** that Conditional Access can take into account when making a policy **decision** include:
- User or group membership
- IP Location information
- Device
- Application
- Real-time and calculated risk detection
	- With **Azure AD Identity Protection**
- Microsoft Cloud App Security (MCAS) :bulb:

#### 2. Conditional Access decision
To apply a **policy** to the request based on the organization’s security posture, the decision outcome from Conditional Access will be:

-   **Block Access**  –  most restrictive decision.
    
-   **Grant Access**  – least restrictive decision. Might require one or more of the following checks:
    -   Require **MFA**
    -   Require device to be marked as **compliant**
    -   Require **Hybrid Azure AD joined device**
    -   Require approved client app
    -   Require app protection policy (preview)

#### 3. Enforcement through applied policies
Many organizations have  [common access concerns that Conditional Access policies can help with](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policy-common)  such as:

-   Requiring **MFA for users with administrative roles**
-   Requiring **MFA for Azure management tasks**
-   Blocking sign-ins for users attempting to use legacy authentication protocols
-   Requiring **trusted locations for Azure MFA registration**
-   Blocking or granting access from **specific locations**
-   Blocking risky sign-in behaviors
-   Requiring **organization-managed devices** for specific applications

#### 4. Licensing for identity and Conditional Access
Azure AD tiers: 
-   Free 
	- SSO, self-service password change :anger:, MFA, basic security/usage reports, and business-to business collaboration
-   Microsoft 365 Apps 
	- Free + identity, self-service password reset :anger:, and device write-back (two-way synchronization between on-premises directories and Azure)
- Azure AD Premium P1
	- Microsoft 365 E5, E3, and F3 plans. 
	- Free features, 
	- Office 365, 
	- premium features = **Conditional Access** based on group, location, and device status, 
	- Microsoft Cloud App Discovery, 
	- Advanced security and usage reports, 
	- advanced group access management, 
	- hybrid identities
- Azure AD Premium P2 
	- Microsoft 365 E5
	- all the above
	- **Azure Identity protection** = risk based Conditional Access policies, risky accounts detection, risk event investigations and Identity governance capabilities, including **Privileged Identity Management (PIM)** :bulb:

:exclamation: :anger: :bulb: Note: copy and edit the table in this page: [Manage identities and access in Microsoft 365 with Azure Active Directory - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/describe-identity-access-management-capabilities-of-microsoft-365/3-manage-identities-access-with-azure-active-directory)

### Reduce risk of security breaches with secure authentication
#### Use MFA to improve authentication security
- Azure Multi-Factor Authentication uses two  or more of these: 
	- **Something you know**  – typically a password
	-  **Something you have**  – such as a trusted device that is not easily duplicated, like a phone or hardware key
	-  **Something you are**  - biometrics like a fingerprint or face scan
- Users can add methods here: https://myprofile.microsoft.com/
- Additional supported methods are: 
	- Microsoft Authenticator app
	-  SMS
	-  Voice call
	-  OATH Hardware token :bulb: :star: 
  
#### Passwordless authentication
-   **Removes passwords** that can be stolen.
-   Uses **facial recognition and biometrics** authentication to help ensure the right person has the right access.
-   **Ties PIN to device** so that a hacker would need to steal both.
- Passwordless authentication with Azure AD
	- Fast Identity Online 2 (**FIDO2**) :bulb: :star:
		- open standard for passwordless authentication
		- AuthN using an external security key or a platform key built into a device.
		- Using PINs, biometrics, devices, USB security keys and NFC-enabled smartcards, keys, or wearables
		- Details @ [FIDO2 security keys](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-passwordless#fido2-security-keys)

#### Windows Hello
- On Windows 10 
- Tied to a device and uses a biometric or PIN.
- Windows Hello lets users authenticate to:
-   A Microsoft, AD,  or Azure AD account.
-   An Identity Provider Services :star: or Relying Party Services :star: that support FIDO2
- biometric data doesn't roam and is never sent to external devices or servers

#### Microsoft Authenticator
- You can use the Microsoft Authenticator app in multiple ways, including:
	- MFA method
	-  Passwordless sign in with a fingerprint, face, or PIN.
	-  As a code generator for any other accounts that support authenticator apps.

- :bulb: Passwordless sign-in with Microsoft Authenticator requires:
	- Their accounts are enabled for Azure MFA
	-  They enroll their devices by using **Microsoft Intune** or a third-party endpoint management solution



## Describe the threat protection capabilities of Microsoft 365

### Identify common security threats
Common **network security threats** include:
-   **Eavesdropping** (aka. sniffing) = capturing network packets in transit.
-   **Denial of service** (DoS) = limit/render an app/network resource unavailable.
-   **Port scanning** = ID the apps running on servers.
-   **Man-in-the-middle** (MITMs) = impersonate a legitimate host on the network.

Common **data security threats** include:
-   Unauthorized access 
	- to information on a **server/host**.
	- to data from a **lost or stolen** removable drive.
-   Data leakage
	- lost/stolen **device** with company information.
	- **emails** with sensitive content inadvertently being sent to unintended recipient(s).

Other attacks:
- :bulb: Commodity-driven threats 
	- Automated ransomware operations and large-scale phishing campaigns
- :bulb: Advanced human-operated attacks.
	- More complex, typically begin with exploits, brute-force (password guessing) attacks, or tailored phishing emails.

### Discover how enterprises can prevent, detect, and respond to threats
~~Microsoft Threat Protection~~ (now **Microsoft 365 Defender Suite**)
![Integrate Microsoft Threat Protection experience](https://docs.microsoft.com/en-us/learn/wwl/describe-threat-protection-capabilities-of-microsoft-365/media/3-threat-protection-v3.png)
- Microsoft 365 Defender suite protects/using:
	-   **Identities** 
		- **Microsoft Defender for Identity** (MSDI) 
			- Old name: ~~Azure Advanced Threat Protection~~
			- MSDI uses :star: Active Directory signals to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions directed at your organization.
	-   **Endpoints** 
		- **Microsoft Defender for Endpoint** (MSDE) - 
			- Old name: ~~Microsoft Defender Advanced Threat Protection~~
			- MSDE is a unified endpoint platform for preventative protection, post-breach detection, automated investigation, and response.
	-   **Email and collaboration** 
		- **Microsoft Defender for Office 365** (MSDO) - 
			- Old name: ~~Office 365 Advanced Threat Protection~~
			- MSDO safeguards your organization against malicious threats by detecting, investigating, and responding to attacks across email and other collaboration vectors like Microsoft Teams, SharePoint Online, and OneDrive for Business and Office clients.
			- [Office 365 Security including Microsoft Defender for Office 365 and Exchange Online Protection - Office 365 | Microsoft Docs](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/overview?view=o365-worldwide)
			- ![EOP and Microsoft Defender for Office 365 and their relationships to one another with service emphasis, including a note for email authentication.](https://docs.microsoft.com/en-us/microsoft-365/media/tp_graphiceopatpp1p2_2.png?view=o365-worldwide)
				- Plan 1
					- Microsoft 365 Business Premium
					- Protects email and collaboration from zero-day malware, phish, and business email compromise.	
				- Plan 2 
					- Office 365 E5, Office 365 A5, and Microsoft 365 E5.
					- Adds post-breach investigation, hunting, and response, as well as automation, and simulation (for training).
				- Exchange Online Protection (EOP) :star: :bulb: 
					- Prevents broad, volume-based, known attacks.	
	-   **Applications** 
		- **Microsoft Cloud App security (MCAS)** 
			- MCAS is a comprehensive cross-SaaS solution bringing deep visibility, strong data controls, and enhanced threat protection to your cloud apps.
			- An intermediary between a cloud user and the cloud provider

### Define your security posture with Microsoft Security Center and Secure Score

Microsoft 365 **Security Center** (:bulb: Microsoft 365 Defender Portal?)
- https://security.microsoft.com/homepage
- Monitoring and managing security across Microsoft identities, data, devices, apps, and infrastructure.
- Intended for security admins and SOC teams to manage and better protect the organization.

Microsoft **Secure Score**
- Report on the current state of the organization's security posture.
	- Points are split between the various categories (identity, data, device, apps, and infrastructure
- Improve their security posture by providing discoverability, visibility, guidance, and control. (using MS Secure Score **recommendations**)
- Compare with benchmarks and establish key performance indicators (KPIs).


### Describe Microsoft's Intelligent Security Graph and Azure Sentinel
- The Intelligent Security Graph 
	- Uses **advanced analytics** to link a massive amount of **threat intelligence** and security data **from Microsoft and partners** to combat cyberthreats. 
	- Insights power the Microsoft Graph Security API

- Microsoft Graph Security API
	- Used by developers to build intelligent security services.
	- Integrates security alerts and threat intelligence from multiple sources
	- Automates security operations

- Azure Sentinel
	- A scalable, cloud-native solution for: 
		- **security information event management (SIEM)** 
		- **security orchestration automated response (SOAR)** .
	- Integrates with Microsoft 365 Defender (~~Microsoft Threat Protection.~~) solutions
	- Provides:
		- Collect data at cloud scale across all users, devices, applications, and infrastructure, both on-premises and in multiple clouds.
		-  Detect previously undetected threats, and minimize false positives using Microsoft's analytics and unparalleled threat intelligence.
		-  Investigate threats with artificial intelligence, and hunt for suspicious activities at scale, tapping into years of cyber security work at Microsoft.
		-  Respond to incidents rapidly with built-in orchestration and automation of common tasks.




  

## Describe the cloud security capabilities of Microsoft 365

-   Explore the Cloud App Security Framework.
-   Discover the capabilities of Microsoft Cloud Application Security (MCAS).
-   Explore how Microsoft Cloud App Security integrates with Microsoft security and threat protection capabilities.

### Take control of your cloud environment with Microsoft Cloud App Security
- MCAS = User-based subscription service 
	- provides rich visibility and control over data travel 
	- analytics to identify and combat cyberthreats across all your cloud services. 
	- powered by native integrations with industry-leading security and identity solutions, (Azure D, Intune, and Azure Information Protection) 
	- identifies and combats these threats by operating as an intermediary, or broker, between a cloud user and the cloud provider.
	- a **Cloud Access Security Broker** (CASB)
		- cloud-based security solutions that provide a layer of security to enable oversight and control of activities and information across public and custom cloud SaaS apps and IaaS services.
		- CASBs are broken down into four key capability areas (:anger: **Cloud App Security framework**)
			- Shadow IT Discovery, 
			- Information Protection, 
			- Threat Protection, 
			- Compliance

### Explore the integration capabilities of Microsoft Cloud App Security
Integration with **Microsoft Defender for Endpoint**
- Allow discovery of cloud apps (shadow IT) used outside your network. 
- Discover Apps, IPs, Machines, Behaviors...

Integration with **Azure AD** and **Azure Information Protection**
![Azure Active Directory Conditional Access](https://docs.microsoft.com/en-us/learn/wwl/describe-cloud-security-capabilities-of-microsoft-365/media/3-azure-active-directory-conditional-access-v2.png)
- Allows the business to prevent confidential information from leaking outside of the organization.

MCAS and **Advanced threat intelligence**
-   MCAS leverages the **Intelligent Security Graph**, with its billions of security signals, to power its Threat Detection.
-   MCAS integrates with **Secure Score** to provide visibility into your security position and provides an overview of which security features are available to reduce risk. 

MCAS integration with **Power Automate**
- Power Automate = a service to create automated workflow between apps and services to synchronize files, get notices, collect data, and more.
- Microsoft Cloud App Security integrates with Power Automate = automation and orchestration **playbooks** = a response when specific alerts are triggered.



## Describe the information protection and governance capabilities of Microsoft 365

### Discover and identify important information across your environment
- Sensitivity labels
	- Sensitivity labels use **Azure Information Protection**.
	- They need to be created and published to users/services in the organization.
	- Once published, sensitivity labels will appear in Office apps...
	- Sensitivity label is:
		- Customizable = example: Personal, Public, General, Confidential, and Highly Confidential.
		- Clear text = stored in plaintext in document metadata.
		- Persistent = label roams with the content, document, email and policies are enforced. 
	- What can you do with these labels?
		- **Encrypt** = [Restrict access to content by using encryption sensitivity](https://docs.microsoft.com/en-us/microsoft-365/compliance/encryption-sensitivity-labels).
		- **Mark the content** = adding watermarks, headers, or footers to email or documents that have the label applied. See [When Office apps apply content marking and encryption](https://docs.microsoft.com/en-us/microsoft-365/compliance/sensitivity-labels-office-apps#when-office-apps-apply-content-marking-and-encryption).
		- **Apply the label automatically** = can be applied automatically, or you can prompt users to apply the label that you recommend.
		- **Protect content in containers such as sites and groups** (Preview) =  [use sensitivity labels with Microsoft Teams, Microsoft 365 groups, and SharePoint sites](https://docs.microsoft.com/en-us/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).

- Azure Information Protection. 
	- Anywhere 
	- helps an organization classify and optionally, protect its documents and emails by applying **labels**.
	- For example, an email message has been classified as "General". The label has added a footer of "Sensitivity: General" to the email message.
	- The label is embedded in the email headers so that email services can inspect this value and create an audit entry or prevent it from being sent outside the organization.

- Data classification
	- How to see the applied retention labels and sensitivity labels?
		- Microsoft 365 Compliance center > data classification portal (https://compliance.microsoft.com/dataclassification)

### Protect your data throughout its lifecycle

- Protect your data with sensitivity labels
	- By: Automatically apply a sensitivity label to content
		- the protection associated with that label is automatically applied.
	- By: Use sensitivity labels to apply encryption.
		- restrict access to content to which a sensitivity label is applied.
		- can be decrypted only by users authorized by the label's encryption settings.
		- Encrypted at rest and in transit. 
		- The encryption settings are available when you create a sensitivity label in the Microsoft 365 compliance center or the Microsoft 365 security center.

- Office 365 Message Encryption (OME)
	- Email message encryption
	- Works with Outlook, Yahoo!, Gmail, and other email services.
	- Ensure that only intended recipients can view the message content.
	- An online service that's built on Microsoft Azure Rights Management (Azure RMS),
	- Used by Azure Information Protection (AIP)

- Data loss prevention (DLP)
	- protect sensitive information and prevent its inadvertent disclosure and is **implemented through policies**.
	- Can use sensitivity labels and [Sensitive information types ](https://docs.microsoft.com/en-us/microsoft-365/compliance/sensitive-information-type-entity-definitions?view=o365-worldwide) to identify sensitive information. 
	- using deep content analysis
		- uses keyword matches, dictionary matches, the evaluation of regular expressions, internal functions, and other methods
	- What can you do with DLP?
		- Identify sensitive information (Sharepoint, OneDrive, Exchange, Teams)
			- ex: you can identify any document containing a credit card number that's stored in any OneDrive for Business site
		- Prevent the accidental sharing of sensitive information (Sharepoint, OneDrive, Exchange, Teams)
			- Ex: identify any document or email containing a health record that's shared with people outside your organization
		- Monitor and protect sensitive information in Office
			- DLP provides continuous monitoring when people share content in Office programs.
		- Help users learn how to stay compliant
			- Ex: user tries to share a document containing sensitive information, a DLP policy can both send them an email notification and show them a policy tip.
		- View DLP reports 
			- Ex:  see how many matches each policy and rule has over time.

- Windows Information Protection
	- Set of technologies that protect your organization from accidental or malicious data leaks
	- On both enterprise-owned devices and BYOD devices


### Govern your data using Microsoft 365
Capabilities in Microsoft 365 include:  
- Manage data
	- Bulk import PST files to Exchange Online mailboxes
	- Unlimited Archiving > more mailbox storage to users
	- Retention policies
- Monitor data
	- Security & Compliance Center >  Label Activity Explorer
		- Label usage and ensure data labels are being applied appropriately.
- Manage inactive mailboxes
	- Create inactive mailboxes to retain the mailbox of former employees.
- Records management
	- Meet regulatory and legal obligations
	- Disposing of documents and data that are no longer required.
	- Includes:
		- Labeling content as a record.
		-   Migrating and managing your retention plans with file plan manager.
		-   Establishing retention and deletion policies within the record label.
		-   Triggering event-based retention.
		-   Reviewing and validating disposition.
		-   Proof of records deletion.
		-   Exporting information about disposed items.
		-   Setting specific permissions for records manager functions in your organization


## Describe the compliance management capabilities in Microsoft
-   Find compliance documentation.
-   Describe Microsoft’s privacy principles.
-   Explore the Microsoft 365 compliance center.
-   Describe the benefits of Compliance Manager.

### Describe common compliance needs
- Govs regulations = protect people' data through:
	-   Personal right to access their data at any time.
	-   Personal right to correct or delete data about them if needed.
	-   Retention periods = minimum/maximum time data storage.
	-   Enabling governments and regulatory agencies the right to access/examine data when necessary.
	-   What/how data can be processed.
	- Regulations geographic data movement:
		- Destination country provides adequate protections for the data?
		- Organizations contracts should includes clauses that regulate data with contractors. 
- Common compliance regulations and standards
	-   **Health Insurance Portability and Accountability Act (HIPAA)**  – a regulation that introduces rules on how health-related information should be protected.
	-   **The Family Educational Rights and Privacy Act (FERPA)**  – a regulation that introduces rules to protect student information.
	-   **ISO 27701**  – a standard that specifies rules and guidance to manage personal information, and demonstrate compliance.


### Describe the offerings of the Service Trust Portal
- https://servicetrust.microsoft.com/
	- Information, tools, and other resources about Microsoft security, privacy, and compliance practices
		-   **Service Trust Portal**  – home page.
		-   **Compliance Manager**  
			- https://servicetrust.microsoft.com/ComplianceManager/V3
			- https://compliance.microsoft.com/compliancemanager
			-  helps simplify the way to manage compliance by recommending actions to take to comply with industry regulations and standards that matter to the business.
		-   **Trust Documents**  
			- links to a security implementation and design information.
			- [Audit Reports (microsoft.com)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
				- Resources to help information security and compliance professionals understand cloud features, and to verify technical compliance and control requirements
			- [Data Protection (microsoft.com)](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3)
				- Whitepapers, FAQs, Security Reports, Penetration Tests, Risk Assessment Tools and Other Resources
			- [Azure Stack (microsoft.com)](https://servicetrust.microsoft.com/ViewPage/AzureStack)
				- Provides security and compliance solutions and support, tailored to the needs of Azure Stack customers.
		-   **Industries & Regions**  – contains compliance information about Microsoft Cloud services organized by industry and region. 
			- Industry Solutions > [Financial Services](https://servicetrust.microsoft.com/ViewPage/FinancialServicesOverview). 
				- :bulb: :star:[Microsoft Cloud for Financial Services](https://www.microsoft.com/en-us/industry/financial-services/microsoft-cloud-for-financial-services?rtc=1) 
			- Regional Solutions > Australia, Canada, Czech Republic, Denmark, Germany, Poland, Romania, Spain, and the United Kingdom.
		-   Microsoft **Trust Center**
			- information about security, compliance, and privacy in the Microsoft Cloud.
			- [Microsoft Trust Center](https://www.microsoft.com/en-us/trust-center)
				- https://www.microsoft.com/en-us/trust-center/privacy
				- https://www.microsoft.com/en-us/security
				- https://www.microsoft.com/en-us/trust-center/compliance/compliance-overview
		-   **Resources** 
			- Information about the features and tools available for data governance and protection in Office 365, 
			- Microsoft Global Datacenters, 
			- Frequently Asked Questions.
		-   **My Library**  – 
			- https://servicetrust.microsoft.com/Library
			- Save reports, whitepapers and other resources relevant to your organization. 

### Microsoft's 6 privacy principles
-   **Control**: easy-to-use tools + clear choices for client to control their data. 
-   **Transparency**: about data collection and use.
-   **Security**: Protecting the data by using strong security and encryption.
-   **Strong legal protections**: Respecting local privacy laws and fighting for legal protection of privacy as a fundamental human right.
-   **No content-based targeting**: Not using email, chat, files, or other personal content to target advertising.
-   **Benefits to you**: All data collection benefits the clients, make their experiences better.

### Describe the Compliance Center
- https://compliance.microsoft.com/
	- available to customers with a Microsoft 365 **SKU** :bulb: with one of the following roles:
		-   Global administrator
		-   Compliance administrator
		-   Compliance data administrator
	- Default cards in the home page: 
		- Compliance Score  = the progress in completing recommended improvement **actions** within **controls**.
			- Forwards admins to the **Compliance Manager** - https://compliance.microsoft.com/compliancemanager
		- Solution catalog = Discover new and improved compliance and risk management solutions available to your org (https://compliance.microsoft.com/solutioncatalog)
			-  The  **Information protection & governance**  
				- Data loss prevention
				- Information governance
				- Information protection
				- Records management
			-   The  **Insider risk management**  
				- Communication compliance
				- Information barriers
				- Insider risk management
			-   The  **Discovery & respond section**  
				- Audit
				- Data subject requests
				- eDiscovery
		- Active alerts = Summary of the most active alerts and a link where admins can view more detailed information, such as alert severity, status, category, and more.
			- https://compliance.microsoft.com/compliancealerts

### Describe Compliance Manager
A tool that provides:
-  **Prebuilt assessments** based on common regional and industry regulations and standards. 
- Admins can also use **custom assessment** to help with compliance needs unique to the organization.
-   Workflow capabilities that enable admins to efficiently complete risk assessments for the organization.
-   Step-by-step improvement **actions** that admins can take to help meet regulations and standards relevant to the organization. Some actions will also be managed for the organization by Microsoft. Admins will get implementation details and audit results for those actions.
-   **Compliance score**, which is a calculation that helps an organization understand its overall compliance posture by measuring how it's progressing with improvement actions.


The **key elements**: 

 - Controls = requirement of a regulation, standard, or policy.
	 - defines how to assess and manage system configuration, organizational process, and people responsible for meeting a specific requirement of a regulation, standard, or policy.
	 - Types:
		 -  **Microsoft-managed controls**: controls for Microsoft cloud services, Microsoft is responsible for implementing.
		-   **Your controls**: customer-managed controls, these are implemented and managed by the organization.
		-   **Shared controls**: responsibility for implementing these controls is shared by the organization and Microsoft.
 - Assessments 
 - Templates 
 - Improvement actions

Compliance Manager provides many **benefits**, including:
-   Translating complicated regulations, standards, company policies, or other control frameworks into a simple language.
-   Providing access to a large variety of out-of-the-box assessments and custom assessments to help organizations with their unique compliance needs.
-   Mapping regulatory controls against recommended improvement actions.
-   Providing step-by-step guidance on how to implement the solutions to meet regulatory requirements.
-   Helping admins and users to prioritize actions that will have the highest impact on their organizational compliance by associating a score with each action.


### Describe use and benefits of compliance score
- Measures progress in completing recommended improvement actions within **controls**.
- Compliance Manager vs. compliance score?
	- The compliance score is available through Compliance Manager.
	- Compliance Manager gives admins the capabilities to understand and increase their compliance score
- How to understand the compliance score?
	- The overall compliance score is calculated using scores that are assigned to **actions**. 
	- Actions come in two types:
		- Org improved actions: actions that the organization is expected to manage.
		- Microsoft actions: actions that Microsoft manages for the organization.
	- Actions can be technical or nontechnical.
	- Actions are categorized as:
		-  **Mandatory**  – these actions shouldn’t be bypassed. For example, creating a policy to set requirements for password length or expiration.
		-   **Discretionary**  – these actions depend on the users understanding and adhering to a policy. For example, a policy where users are required to ensure their devices are locked before they leave them.
	- Subcategories: 
		-   **Preventative**  actions are designed to handle specific risks, like using encryption to protect data at rest if there were breaches or attacks.
		-   **Detective**  actions actively monitor systems to identify irregularities that could represent risks, or that can be used to detect breaches or intrusions. Examples of these types of actions are system access audits, or regulatory compliance audits.
		-   **Corrective**  actions help admins to minimize the adverse effects of security incidents, by undertaking corrective measures to reduce their immediate effect or possibly even reverse damage.
	- Actions that are mandatory and preventative, with 27 points, provide the highest points value towards your compliance score.
  

## Reduce risk and simplify the discovery and audit process
-   Explore the Microsoft 365 capabilities to manage insider risk.
-   Describe the tools available to help organizations find relevant data quickly and cost effectively.

### Insider risk management
- https://compliance.microsoft.com/insiderriskmgmt
* A Microsoft 365 solution that helps minimize internal risks = detect, investigate, and take action on risky activities.
* Insider Risks:
	-   Leaks of sensitive data and data spillage
	-   Confidentiality violations
	-   Intellectual property (IP) theft
	-   Fraud
	-   Insider trading
	-   Regulatory compliance violations

#### Insider risk management workflow
Identifying and resolving internal risk activities and compliance issues with insider risk management in Microsoft 365 uses the following workflow:
![Diagram showing the risk management workflow](https://docs.microsoft.com/en-us/learn/wwl/reduce-risk-simplify-discovery-audit-process/media/2-diagram-insider-risk-management.png)

-   **Policies** - created using pre-defined templates and policy conditions that define what **risk indicators** are examined in Microsoft 365 feature areas. =  [Insider risk management policies](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-policies?view=o365-worldwide).
-   **Alerts** - Automatically generated by **risk indicators** that match policy conditions and are displayed in the  **Alerts dashboard** =  [Insider risk management alerts](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-alerts?view=o365-worldwide). 
	- Alerts are resolved by opening a new case, assigning the alert to an existing case, or dismissing the alert.Alerts are resolved by opening a new case, assigning the alert to an existing case, or dismissing the alert.
-   **Triage** - New activities that need investigation automatically generate alerts that are assigned a  _Needs review_  status. Reviewers can quickly identify these alerts and scroll through each to evaluate and triage. 
-   **Investigate** - **Cases** are created for alerts that require deeper review and investigation of the details and circumstances around the policy match. 
	- The  **Case dashboard**  provides an all-up view of all active cases, open cases over time, and case statistics for your organization. =  [Insider risk management cases](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-cases?view=o365-worldwide).
-   **Action** - After cases are investigated, reviewers can quickly take action to resolve the case or collaborate with other risk stakeholders in your organization.
    -   Actions can be as simple as sending a notification when employees accidentally or inadvertently violate policy conditions. For more information, see  [Insider risk management notice templates](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-notices?view=o365-worldwide).
    -  If a case is more serious, **escalating a case for investigation** allows you to transfer data and management of the case to :anger: **Advanced eDiscovery in Microsoft 365**. =  [Overview of Advanced eDiscovery in Microsoft 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/overview-ediscovery-20?view=o365-worldwide).

#### Scenarios
-   **Data theft by employees** 
	- When employees leave an organization, either voluntarily or as the result of termination, there is often legitimate concerns that company, customer, and employee data are at risk =  [Departing employee data theft](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-policies?view=o365-worldwide#policy-templates) 
-   **Intentional or unintentional leak of sensitive or confidential information** 
	- Policies created using the  [Data leaks](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-policies?view=o365-worldwide#policy-templates) policy template automatically detect activities typically associated with sharing sensitive or confidential information.
-   **Actions and behaviors that violate corporate policies** 
	- Employee-to-employee communications are often a source of inadvertent or malicious violations of corporate policies.
	- These violations can include offensive language, threats, and cyber-bullying between employees. 
	- This type of activity contributes to a hostile work environment and can result in legal actions against both employees and the larger organization.
	- [Offensive language in email](https://docs.microsoft.com/en-us/microsoft-365/compliance/insider-risk-management-policies?view=o365-worldwide#policy-templates)  policy template.

### Manage communications compliance
- Detect, capture, and take remediation actions for inappropriate messages in your organization.
- Reviewers can investigate scanned emails, Microsoft Teams, Yammer, or third-party communications in your organization and take appropriate remediation actions to make sure they're compliant with your organization's message standards.
- Microsoft Communication Compliance.
	- isn’t enabled by default, and can be found in the **Solutions Catalog**, under **Insider Risk Management**.
		- :bulb: https://compliance.microsoft.com/supervisoryreview
	- monitor and detect aberrant and undesirable communications

### Restrict communications with information barriers
- Information barriers (IB)
	- policies that an admin can configure to prevent individuals or groups from communicating with each other.
	- users won't be able to find, select, chat, or call those users.
#### Scenarios
Some common scenarios include:

-   **Financial services**: Financial Industry Regulatory Authority (FINRA) reviews information barriers and conflicts of interest within member firms and provides guidance as to how to manage such conflicts
-   **Education**: Students in one school aren't able to look up contact details for students of other schools.
-   **Legal**: Maintaining confidentiality of data obtained by the lawyer of one client from being accessed by a lawyer for the same firm representing a different client.
-   **Government**: Information access and control is limited across departments and groups
-   **Professional services**: A group of people in a company is only able to chat with a client or specific customer via federation or guest access during a customer engagement.


#### :bulb: Information barriers in Teams
In Microsoft Teams, information barrier policies determine and prevent the following kinds of unauthorized communications:

-   Searching for a user
-   Adding a member to a team
-   Starting a chat session with someone
-   Starting a group chat
-   Inviting someone to join a meeting
-   Sharing a screen
-   Placing a call

Details: [Information barriers in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/information-barriers-in-teams).


### Control privileged admin access
- Enabling privileged access management in Microsoft 365 allows your organization to operate with **zero standing access** = 
	- users who need privileged access, must request permissions for access, and once received it's just-in-time and just-enough access to perform the job at hand.
	- The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.
- :anger: :bulb: [Control privileged admin access - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/reduce-risk-simplify-discovery-audit-process/5-control-privileged-admin-access)
	- Try to do a lab on this. 


### Increase control with Customer Lockbox
- Customer Lockbox
	- Gives organizations the option to approve or deny these requests and provide direct-access control to the customer.
	- Ensures that Microsoft can't access your content to perform a service operation without your explicit approval.
	- Requests to access data in Exchange Online, SharePoint Online, and OneDrive for Business.

#### Customer Lockbox workflow
1.  Support request with Microsoft Support.
2.  A Microsoft support engineer = need to access the organization's tenant to repair the issue.
3.  The Microsoft support engineer logs into the Customer Lockbox request tool and makes a data access request that includes the organization's tenant name, service request number, and the estimated time the engineer needs access to the data.
4.  After a Microsoft Support manager approves the request, Customer Lockbox sends the designated approver at the organization an email notification about the pending access request from Microsoft.
5.  The approver signs-in to the Microsoft 365 admin center and approves the request. This step triggers the creation of an audit record available by searching the audit log. 
	- If the customer rejects the request or doesn't approve the request within 12 hours, the request expires, and no access is granted to the Microsoft engineer.
6.  After the approver from the organization approves the request, the Microsoft engineer receives the approval message, logs into the tenant, and fixes the customer's issue. 

### Investigate with Advanced Audit
* new auditing capabilities that can help your organization with forensic and compliance investigations.
* **Microsoft 365 Enterprise E5** 
	* or **Microsoft 365 E5 Compliance add-on license** can be assigned to user when needed. 


- Advanced Audit includes these capabilities:
	- **Long-term retention** of audit logs 
		- Default audit log retention policy that retains all Exchange, SharePoint, and Azure Active Directory audit records for **1 year**.
	-   Audit log retention policies 
		- All audit records generated in other services that aren't covered by the default audit log retention policy are retained for **90 days**. 
		- Customized audit log retention policies to retain other audit records for up to one year.
	-   Access to crucial events for investigations 
		- Ex  _MailItemsAccessed_  mailbox auditing action. 
			- This action is triggered when mail data is accessed by mail protocols and mail clients. 
			- This action can help investigators identify data breaches and determine the scope of messages that may have been compromised.
	-   High-bandwidth access to the Office 365 Management Activity API 
		- Each organization will get their own fully allocated bandwidth quota to access their auditing data.

### Manage compliance and legal investigations with Advanced eDiscovery
- Advanced eDiscovery  
	- An end-to-end **workflow** to preserve, collect, review, analyze, and export content that's responsive to your organization's internal and external investigations.
	- Aligns with the eDiscovery process outlined by the **Electronic Discovery Reference Model (EDRM)** :bulb:	 [EDRM](https://edrm.net/wp-content/uploads/2020/04/EDRM-clean-poster-24x36-1.pdf)

At a high level, here's how Advanced eDiscovery supports the EDRM workflow:

-   **Identification**. 
	- After you identify potential persons of interest in an investigation, you can add them as custodians (also called  _data custodians_, because they may possess information that's relevant to the investigation) to an Advanced eDiscovery case. After users are added as custodians, it's easy to preserve, collect, and review custodian documents.
-   **Preservation**. 
	- To preserve and protect data that's relevant to an investigation, Advanced eDiscovery lets you place a legal hold on the data sources associated with the custodians in a case. You can also place non-custodial data on hold. Advanced eDiscovery also has a built-in communications workflow so you can send legal hold notifications to custodians and track their acknowledgments.
-   **Collection**. 
	- After you identified (and preserved) the data sources relevant to the investigation, you can use the built-in search tool in Advanced eDiscovery search for and collect live data from the custodial data sources (and non-custodial data sources, if applicable) that may be relevant to the case.
-   **Processing**. 
	- After you've collected all data relevant to the case, the next step is process it for further review and analysis. In Advanced eDiscovery, the in-place data that you identified in the collection phase is copied to an Azure Storage location (called a  _review set_), which provides you with a static view of the case data.
-   **Review**. 
	- After data has been added to a review set, you can view specific documents and run another queries to reduce the data to what is most relevant to the case. Also, can annotate and tag specific documents.
-   **Analysis**. 
	- Advanced eDiscovery provides integrated analytics tool that helps you further cull data from the review set that you determine isn't relevant to the investigation. In addition to reducing the volume of relevant data, Advance eDiscovery also helps you save legal review costs by letting you organize content to make the review process easier and more efficient.
-   **Production**  and  **Presentation**. 
	- When you're ready, you can export documents from a review set for legal review. You can export documents in their native format or in an EDRM-specified format so they can be imported into third-party review applications.
