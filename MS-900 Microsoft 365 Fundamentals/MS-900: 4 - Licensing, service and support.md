
# MS-900: Licensing, service and support

These notes are made from the official MS learning path available at: [Microsoft 365 Fundamentals: Demonstrate knowledge of Microsoft 365 licensing, service and support - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/paths/m365-licensing-service-support/)

:exclamation:		Important
:anger: 				Be careful, confusing
:scroll:					Reoccurring exam topic
:star: 					Interesting 
:bulb:					Ideas to work on later


## What is Microsoft 365?
### Explore the productivity benefits of Microsoft 365
- Personal productivity
	- Enable teamwork and simplify workflow (ex. with **Teams**)
	- Stay productive on the go (**mobile** apps)
	- Get more done with **AI**-enabled tools
- Organizational productivity
	- Harness organizational knowledge (:anger: ~~Workplace Analytics~~ is now **Viva Insights**)
	- Manage all your endpoints (Microsoft Endpoint Manager)
	- Protect your business (security, risk management, compliance standards)

### Explore the Microsoft 365 subscription options
:exclamation:	for a non-US organizations, prices and plans might vary.
#### Microsoft 365 Enterprise
These subs includes robust threat protection, security, compliance, and analytics features. To compare the plans: [Microsoft 365 Enterprise](https://www.microsoft.com/en-us/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- Microsoft 365 E3 
- Microsoft 365 E5 = E3 + advanced threat protection, security, and collaboration tools
- Microsoft 365 F3 (~~formerly F1~~) = for Firstline Workers

#### Microsoft 365 for business
For small- and medium-sized organizations. To compare the plans: [Microsoft 365 for Business](https://www.microsoft.com/en-us/microsoft-365/business?rtc=1#compareProductsRegion)
:exclamation: Up to 300 licenses
- Microsoft 365 Basic
- Microsoft 365 Standard
- Microsoft 365 Premium

#### Microsoft 365 Education
For educational organizations. [Free Microsoft 365 Education](https://www.microsoft.com/en-us/education/products/microsoft-365)
- Microsoft 365 A1
- Microsoft 365 A3
- Microsoft 365 A5

#### Microsoft 365 Home
- Microsoft 365 Family
- Microsoft 365 Personal
:star: Office Home and Student 2019 are available as a one-time purchase, but do not include any of the cloud benefits of Microsoft 36

### Explore Microsoft 365 tenant
- Configure company branding
	- Azure Portal > Azure AD > Company Branding > Configure :
		- Language
		- Background image
		- Banner logo image
		- Hints
		- and other options :bulb:	
- Teams admin center 
	- Configure **Policies**:
		-   A  **policy package**  is a collection of predefined policies and settings.
		-   **Meeting policies**  control the features that are available to participants in meetings.
		-   **Messaging policies**  control which chat and channel messaging features are available to users.
	- Configure **Org-wide settings**:
		-   **External access**, formerly known as federation :anger: , lets Teams and Skype for Business users communicate with users who are outside of your organization.
		-   **Guest access**  lets individuals outside your organization access teams and channels.
	- Other options: 
		- :star: **Call quality dashboard**, **Analytics & reports** 


## Identify licensing options available in Microsoft 365
### Compare home, business, and enterprise options
#### Business:


|   			|  **Basic** | **Standard**  |  **Premium** | **M365 Apps for business**  |
|---------------|------------|---------------|--------------|-----------------------------|
| M365 apps 	|   		 |:full_moon:|:full_moon:| :full_moon:  |
| Exchange  	|:full_moon: |:full_moon:|:full_moon:|   |
| OneDrive		|:full_moon: |:full_moon:|:full_moon:| :full_moon:  |
| SharePoint	|:full_moon: |:full_moon:|:full_moon:|   |
| Teams			|:full_moon: |:full_moon:|:full_moon:|   |
| Intune		|   		 |   		|:full_moon::exclamation:|   |
| Azure IP		|   		 |   		|:full_moon::exclamation:|   |

#### Enterprise:

Complete > :full_moon:
Partial > :moon:

| Capability group               | F3  | E3 | E5 |
|--------------------------------|------------------------------------------------|------------------|------------------|
| Microsoft 365 Apps             | Office mobile/web only | :full_moon:| :full_moon:|
| Email and calendar             | :full_moon:| :full_moon:| :full_moon:|
| Meetings and voice             | :moon::anger: | :moon::anger: | :full_moon:|
| Social and intranet            | :full_moon:| :full_moon:| :full_moon:|
| Files and content              | :full_moon:| :full_moon:| :full_moon:|
| Task management                | :full_moon:| :full_moon:| :full_moon:|
| Advanced analytics             |  | :moon::anger: | :full_moon:|
| Device and app management      | :full_moon:| :full_moon:| :full_moon:|
| Identity and access management | :moon::anger: | :moon::anger: | :full_moon:         |
| Threat protection              | :moon::anger: | :moon::anger: | :full_moon:         |
| Information protection         | :moon::anger: | :moon::anger: | :full_moon:|
| Security management            | :full_moon:| :full_moon:| :full_moon:|
| Advanced compliance            |                                                |                  | :full_moon:|

- capability groups:

| Capability group               | Description                                                                                                                                                                                                                                                                 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft 365 apps             | Install Office desktop apps (Word, Excel, PowerPoint, OneNote, Access) on up to 5 PCs/Macs + 5 tablets + 5 smartphones per user with Microsoft 365 Apps for enterprise. Microsoft 365 F3 includes Office mobile apps and Office for the web.                                |
| Email and calendar             | Includes Outlook and Exchange.                                                                                                                                                                                                                                              |
| Meetings and voice             | Microsoft 365 E5 includes Microsoft Teams, audio calls and phone system. E3 and F3 subscriptions include Microsoft Teams.                                                                                                                                                   |
| Social and intranet            | Includes SharePoint and Yammer.                                                                                                                                                                                                                                             |
| Files and content              | Includes OneDrive, Stream, and Sway.                                                                                                                                                                                                                                        |
| Task management                | Includes Planner, Power Apps, Power Automate, and To Do.                                                                                                                                                                                                                    |
| Advanced analytics             | Microsoft 365 E5 includes MyAnalytics and Power BI Pro. E3 subscriptions include MyAnalytics.                                                                                                                                                                               |
| Device and app management      | Includes Windows Enterprise, Microsoft 365 Admin Center, Microsoft Intune, Windows Autopilot, Windows Analytics Device Health, and Microsoft Endpoint Configuration Manager.                                                                                                |
| Identity and access management | Includes Windows Hello, Credential Guard, and Direct Access, and Azure Active Directory Premium plan 1. Microsoft 365 E5 also includes Azure Active Directory Premium plan 2.                                                                                               |
| Threat protection              | Includes Microsoft Advanced Threat Analytics and Windows Defender Antivirus and Device Guard. Microsoft 365 E5 also includes Microsoft Defender Advanced Threat Protection, Microsoft 365 Advanced Threat Protection, and Azure Advanced Threat Protection.                 |
| Information protection         | Includes Windows Information Protection and BitLocker and Azure Information Protection P1. Microsoft 365 E5 and E3 subscriptions also include Microsoft 365 data loss prevention. Microsoft 365 E5 further includes Azure Information Protection P2 and Cloud App Security. |
| Security management            | Includes Microsoft Secure Score and Microsoft Security and Compliance Center.                                                                                                                                                                                               |
| Advanced compliance            | Microsoft 365 E5 includes Advanced eDiscovery, Customer Lockbox, Advanced Data Governance, Service Encryption with Customer Key, and Privileged Access Management.                                                                                                          |

### Describe additional capabilities available with Azure
- MS365 for Business:
	- Microsoft Azure Active Directory P1
- MS365 for Enterprise:
	- F1
		- Microsoft Azure Active Directory Premium P1
		- with additional identity protection features from Azure Active Directory Premium P2, to detect and remediate identity-based risks. 
	- E3
		- Microsoft Azure Active Directory Premium P1
		- to create and manage user and group accounts. 
	- E5
		- Microsoft Azure Active Directory Premium P1 and P2
		- to create, manage, and protect user and group accounts.

:anger: P2 can be purchased additionally and includes identity protection and identity governance functionality.

### Describe the cloud solution provider model
- CSP: 
	- 3rd party to manage Microsoft 365 subscription, licenses and settings, and provide tier 1 support.
	- provides additional consultancy and advice to ensure security and productivity targets are met.
	- pay-as-you-go subscription model for Windows 10 with per-user, per-month pricing
	- CSP catalogue: https://www.microsoft.com/solution-providers/home

:bulb:	Microsoft’s New Commerce Experience (NCE) for CSP

### Explore bill management options
- **Billing** is accessible via M365 admin center, you can review and modify:
	- Number of licenses and allocations
	- Any charges due
	- Payment method and frequency (monthly or annual).
	- Additional services or features
	- Billing notifications

### Explain ways that Microsoft 365 helps optimize costs
- cost consolidation (using multiple services/products from a single provider)
- MS takes care of the underlying hardware and Ops
- reduce security breaches, protect privacy, and simplify remediation
- reduce on-site costs, enabling remote work, less travel expenses
- streamline, automate, AI = more productivity
- CapEx vs. OpEx

### License and manage users
[License and manage users](https://docs.microsoft.com/en-us/learn/modules/identify-licensing-options-available-microsoft-365/7-license-management-options), this is an interactive guide on how to: 
- Review a list of active users, 
- Assign or revoke user licenses, 
- Manage multiple users at once.

## Describe support offerings for Microsoft 365 services
### Explore support options for Microsoft 365 services

| Support type                        | Description                                                                                                                                                                                                             |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Community-based support             | Microsoft 365 Tech Community = collaborative forum to solve problems.                                                                                                                                                   |
| Microsoft 365 Support Assistant     | A bot in the M365 admin center = find answers to support related questions.                                                                                                                                             |
| Web, email, and telephone support   | Submit issues to MS support to receive around the clock technical, billing, and accounts support via email, online chat, or telephone support.                                                                          |
| FastTrack                           | Dedicated Microsoft engineers, project managers, and resources to help deploy Microsoft 365 services and resolve issues along the way                                                                                   |
| Premier Support for Microsoft 365   | On-site support, a dedicated technical account manager, and access to advisory services.                                                                                                                                |
| Support through a Microsoft Partner | A certified MS365 Partner. For example, a 1 Cloud Services Provider direct support. The CSP will act as the first line support for all issues and will escalate issues to Microsoft if they are unable to resolve them. |

The support option chosen depends on:
 - The tool or service where the issue has arisen. 
 - The type of subscription your organization uses. 
 - The kind of support your organization needs.

### Explain service level agreements
- **Microsoft Online Services Level Agreement**
	- Found here [Service Level Agreement - Service Descriptions | Microsoft Docs](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/service-level-agreement#microsoft-online-services-level-agreement)
	- and here [Licensing Documents (microsoft.com)](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services)
- Service Level Agreements with a Cloud Service Provider
	- Varies according to the CSP choosen 
- SLA Concepts:

| Concept        | Description                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Incident       | A set of events or single event that results in downtime.                                                                                                                                                                    |
| Downtime       | Reduces the total time your services are functional (your uptime).                                                                                                                                                           |
| Claim          | Submitted to Microsoft customer support = information about an incident, the downtime, affected users, how you attempted to resolve an incident. Microsoft is then responsible for processing your claim.                    |
| Service Credit | :anger: If your claim has been successfully approved by Microsoft, your organization will receive Service Credits as a percentage of the total monthly fees your organization has paid for the month where you experienced downtime. |

- The percentage of Service Credit an organization can receive, is linked to their monthly uptime percentage:

| Monthly uptime percentage | Service Credit |
|---------------------------|----------------|
| < 99.9%                   | 25%            |
| < 99%                     | 50%            |
| <95%                      | 100%           |

### Describe how to track service health status
- health status of a M365 service = when a specific service will undergo maintenance
#### View the health status of services
- MS365 Admin Center > Health > **Service Health**
	- view the current health status of your Microsoft 365 services and tenant, 
	- information about outages or disruptions to services
	- report an issue if the organization is experiencing service issues
	- view specific details about service issues

(:anger: An advisory is a service issue that is typically limited in scope or impact.)

#### Keep track of incidents

- Service incident = event that has an effect on a service
	- Might occur because of hardware or software failures or issues
	- Notifications can be set for:
		- New incidents
		- Updates to any active incidents that might affect your organization. 
	- Microsoft provides two types of notifications:
		- **Unplanned downtime**: Incident has caused a service to become unresponsive or unavailable.
		- **Planned maintenance**: Service updates to the software and infrastructure that runs services.
	- :exclamation: :anger: :scroll: **Post-Incident Reviews**, analysis of  **unplanned service incidents** by Microsoft: 
		- :moon: Preliminary review within the first :exclamation: two days of incident resolution
		- :full_moon: Final review within :exclamation: five business days. 
			- Final Post-Incident Reviews will details:
				- Company/User impact
				- A date and time breakdown detailing resolution
				- RCA, and what actions are to be carried out to prevent the incident in the future.

- Your organization can keep track of the health status of services in different ways:

| Tool                    | Description                                                                                                                                                                                             |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Admin App               | View and stay up to date with the health status of the services on the go.                                                                                                                              |
| Microsoft System Center | View all service communications from within System Center if your organization has the Office 365 Management Pack (SCOM - Microsoft System Center Operations Manager Management Pack for Microsoft 365) :bulb::exclamation::anger:|
| API                     | Microsoft/Office 365 Service Communications API to create or use tools that can connect and monitor the service status for you in real-time.                                                            |
#### Continuity and availability
- Microsoft is able to recover services from unexpected issues 
	- hardware related issues, 
	- software related issues, 
	- catastrophic issues like natural disasters.

- To protect and keep client's data using:
	- Data storage redundancy: 
		- Storing data on multiple levels of redundancy using data replication and secure data protection capabilities = rapid availability and recovery of data.
	- Monitoring data: 
		- Packet loss, latencies in queries, and more.
	- Preventative measures:
		- Checks for database consistency, reviews of error logs, and more.

### Communicate and share ideas with UserVoice
- UserVoice Feedback collects and prioritizes suggestions from customers as they list ideas and vote on them.
- Microsoft has partnered with UserVoice to enable Microsoft 365 services customers to share ideas and feedback:
	-   [Microsoft Stream](https://techcommunity.microsoft.com/t5/microsoft-stream-ideas/idb-p/StreamIdeas)
	-   [SharePoint](https://sharepoint.uservoice.com/)
	-   [Microsoft Teams](https://microsoftteams.uservoice.com/)
	-   [Yammer](https://yammer.uservoice.com/)
	-   [Word](https://word.uservoice.com/)
	-   [Microsoft Planner](https://planner.uservoice.com/forums/330525-microsoft-planner-feedback-forum)

## Describe the service life cycle in Microsoft 365
### Describe private, public preview, and general availability releases
A product, or services, lifecycle typically has three phases:
 - Private preview 
	 - Released to a limited number of users 
	 - To test new features or functionality. 
	 - Needs to sign up to be members of a private preview
 - Public preview 
	 - Released to get feedback from a broader range of users
	 - Include beta or pre-release features and services
	 - Aren't supported and should only be used to test upcoming functionality.
 - General Availability (GA)
	 - :exclamation:**Release version** and is fully supported.
	 - Have been through a full development and test lifecycle to ensure stability and reliability. 

- :anger: End of support
	- Older products can no longer be supported and these products will reach the end of support. 
	- Will no longer receive updates.
	- For details, see  [Overview - Product end of support](https://docs.microsoft.com/en-us/lifecycle/overview/product-end-of-support-overview).



### Explain support models for private, public preview, and general availability releases
- Microsoft 365 is covered by the Modern Lifecycle Policy.
	- Supported as long as customers stay current as per the servicing and licensing requirements published for the product or service and have the rights to use the product or service. 
	- Microsoft gives :exclamation: :scroll: **a minimum of 12 months'** prior notification before ending support for products governed by the Modern Lifecycle Policy. These notifications don't include any free services, or preview releases.

- **Stay current**  means that customers accept and apply all servicing updates for their products and services.

- For Microsoft 365, customers have the right to use the products or services as long as they have an active subscription.

- For more information on the Modern Lifecycle Policy, see  [Modern Lifecycle Policy](https://docs.microsoft.com/en-us/lifecycle/policies/modern).

### Use the Microsoft 365 roadmap portal to learn about upcoming features
Roadmaps include the status of a feature, whether it is in development, rolling out, or has launched, and the expected release date of that feature.
The Microsoft 365 Roadmap:

-   Allows you to download the current features in development as a CSV file
-   Allows you to search by product, cloud instance, or platform
-   Allows you to view additional information about each update
-   Allows you to leverage RSS to be notified of feature updates in real time
-   Includes Windows and Azure Active Directory

For more information, see  [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

## Select a cloud deployment model
How the cloud-only and hybrid deployments require different approaches and how an organization approaches migrating systems with older versions of Office, Windows, and Office Server to Microsoft 365.
### The hybrid cloud model
- Hybrid is a combination of cloud services with on-premises services to support your IT needs
	- keep critical resources on-premises
	- working with cloud services
	- connects on-premises resources to the cloud
	- cloud services an extension of on-premises infrastructure
	- added mobility and productivity


### Which cloud model should organizations choose?
When organizations consider cloud solutions, they focus on three areas:
- Cost
- Security/reliability and compliance
- Functionality

### Migration vs co-existence - planning your move to Microsoft 365
- Migration = moving old system > new system + intent of removing the old system
	- data and applications from local resources > the cloud
- Coexistence = two systems = on-premises + the cloud
	- Example: link Windows Server Active Directory to Azure Active Directory.
#### Migration considerations
- Office 2013 or older to Microsoft 365 Apps	
	- April 2023, accessing Office 365 services (like Exchange Online, SharePoint) won't be supported with Office 2013.
	- Office 2010 is only supported until 2020
	- Office 2007 isn’t supported at all.

- Office Server versions to equivalent Office 365 services
	- Office Server 2013/2016 (Exchange Server / SharePoint Server) don’t take advantage of the cloud-based services and enhancements.
	- Some Office Server 2010 products have a specified end-of-support date.
	- Office Server 2007 products are no longer supported. 
		- To help with migration from this version, :bulb: hire a Microsoft partner. 
- Windows 7 and Windows 8.1 on your devices to Windows 10 Enterprise	
	- Perform an in-place upgrade to Windows 10 Enterprise.
