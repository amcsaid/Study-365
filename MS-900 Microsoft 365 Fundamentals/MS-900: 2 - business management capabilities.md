# MS-900: business management capabilities

## Manage your business with Microsoft 365
-   Describe how Microsoft 365 empowers organizations with tools to improve organizational productivity.
-   Identify the business management solutions and how they correlate to specific products.

### Organizational productivity
- The ability to streamline the business and meet its goals though the use of tools like:
	-  Workplace Analytics.
	- **Microsoft Endpoint Manager** (MEM) = Simplified management – Simplify the management of all devices. 
	-   **Business process automation** - automate time-intensive tasks, optimizing operations, and bringing a new level of efficiency.
	-   **Extensibility** - Custom applications or customize Office applications, SharePoint, and Microsoft Teams.
	-   **Forms and workflow management** - Capture, track, and act on data and requests with built-in apps and tools designed to simplify and manage workflow processes
	-   **Business intelligence** - Transform your data to create meaningful, actionable insights for your organization.
	-   **Work management** – Manage your projects more efficiently, and share project information with your team and the project stakeholders through Microsoft Planner and Microsoft 365 Groups.

#### Workplace Analytics
* Identify collaboration patterns that impact productivity, workforce effectiveness, and employee engagement.
* AI-based insights that create actionable behaviors you can apply to the way your organization behaves and reacts to change.
* Benefits:
	-   Address wasteful collaboration and meeting cultures.
	-   Enhance process efficiency and effectiveness
	-   Drive cultural transformations.
	-   Inform leadership excellence and development.
	-   Visualize data with dashboards and reports from Power BI and other reporting tools.
	-   Inform leadership initiatives and development.
	-   Develop executive dashboards and reporting systems.


#### Microsoft Secure Score
- Security posture, with a higher number indicating more improvement actions taken. 
- Found in Microsoft 365 security center
- Secure Score helps organizations:
	- Report organization's security posture.
	- Improve security posture by providing discoverability, visibility, guidance, and control.
	- Compare with benchmarks and establish key performance indicators (KPIs).

### Simplified management
* Microsoft Endpoint Manager (MEM)
	- A secure and intelligent management solution that improves productivity and collaboration with the familiar experiences users expect and gives IT the flexibility to support diverse scenarios for both BYOD and corporate-owned devices.

- Endpoint Manager combines services: 
	- Microsoft Intune: 
		- 100% cloud-based MDM & MAM
		- Control features and settings on Android, iOS/iPadOS, macOS, and Windows.
	- Configuration Manager:
		- On-premises management solution to manage desktops, servers, and laptops that are on your network or internet-based.
		- Cloud-enabled version integrates with Intune, Azure Active Directory (AD), Microsoft Defender ATP, and other cloud services.
		- Allow you to customize the following areas:
			-   Application management
			-   OS deployment
			-   Software update management
			-   Device compliance
	- Co-management, 
		- Choose whether ConfigManager (on-premises) or Intune (Cloud) is the management authority for your workloads.
	- Desktop Analytics:
		- A cloud-based service that integrates with Configuration Manager. 
		- Insights and intelligence about the update readiness of Windows clients.
	- Windows Autopilot;
		- Simplify the lifecycle of Windows devices
		- preconfigure devices, and automatically enroll devices in Intune.
	- Azure Active Directory (AD):
		- Identity of devices, users, groups, and multi-factor authentication (MFA)
	- Endpoint Manager admin center:
		- https://endpoint.microsoft.com/ :bulb: :star:
		- Create policies and manage your devices
	- Microsoft Defender:
		- Anti-virus solution provided with Windows.

### Business process automation
Microsoft 365 provides several tools, services, or applications to enable automation:

 - SharePoint 
 - Power Automate 
 - Power Apps

#### Use SharePoint to provide business process automation
- SharePoint workflows are pre-programmed mini-applications that streamline and automate a wide variety of business processes. 
- Workflows can include collecting signatures, feedback, or approvals for a plan or document to track the current status of a routine procedure.
- SharePoint built-in workflows:
	- Approval, Collect Feedback, Collect Signatures, Publishing Approval, Three-state


#### Use Power Automate
 - An online workflow service that automates actions across the most common apps and services.
 - Automate workflows between your favorite applications and services, sync files, get notifications, collect data, and much more.
- **Flow types**
	 - [Automated flows](https://docs.microsoft.com/en-us/power-automate/get-started-logic-flow)
	- [Button flows](https://docs.microsoft.com/en-us/power-automate/introduction-to-button-flows)
	- [Scheduled flows](https://docs.microsoft.com/en-us/power-automate/run-scheduled-tasks)
	- [Business process flows](https://docs.microsoft.com/en-us/power-automate/business-process-flows-overview)
	- [UI flows](https://docs.microsoft.com/en-us/power-automate/ui-flows/overview)

#### Create Power Apps
- A suite of apps, services, connectors, and data platforms that provide a rapid application development environment to build custom apps for your business needs. 


### Extensibility
- Teams
	- A set of extensibility points, UI constructs, and APIs to build your app. 
- Office add-ins
	- Office add-ins provide several options for how your solution can interact with an Office application:
		- Task pane add-ins
		- Content add-ins
- SharePoint Framework
	- SharePoint is an extensible platform you can customize and extend with the SharePoint Framework and the multiple APIs available to developers. 
- Microsoft Graph 
	- Microsoft Graph REST API
	- Microsoft Graph Native SDKs

### Forms and workflow management
#### Microsoft Dynamics 365 Customer Voice
- An enterprise survey capability that helps businesses obtain the feedback they need to make smarter decisions.
- Send Pro Forms

#### Microsoft Bookings
- A web-based appointment scheduling system that integrates with Outlook to provide your customers with the means to book an appointment with members of your staff.

### Business intelligence
- Transforming the data to create meaningful, actionable insights with Excel and Power BI.	
#### Excel's Get & Transform features
![Connecting to and transforming data in Excel](https://docs.microsoft.com/en-us/learn/wwl/manage-your-business-with-microsoft-365/media/7-connect-excel-c43114e8.png)
Looking at those steps in order, they often occur like this:
-   Connect – make connections to data sitting in the cloud, in service, or locally
-   Transform – shape the data to meet your needs; the original source remains unchanged
-   Combine – create a data model from multiple data sources, and get a unique view into the data
-   Share – once your query is complete you can save it, copy it, or use it for reports

#### Power BI
-  A collection of software services, apps, and connectors that work together to turn your independent sources of data into coherent, visually immersive, and interactive insights.
- There are three distinct Apps of Power BI:
	-   A Windows desktop application called Power BI Desktop
	-   An online SaaS (Software as a Service) service called the Power BI service
	-   Power BI mobile apps for Windows, iOS, and Android devices
	- **Power BI Report Server** :bulb: :anger: , which allows you to publish Power BI reports to an on-premises report server, after creating them in Power BI Desktop.
- Power BI licenses = [Details](https://docs.microsoft.com/en-us/learn/modules/manage-your-business-with-microsoft-365/7-business-intelligence)
	- Free (Not in Premium capacity)
	- Free (Premium capacity)
	- Pro (Not in Premium capacity)
	- Pro (Premium capacity)

#### Analyze in Excel
- Bring Power BI datasets into Excel, and then view and interact with them using PivotTables, charts, slicers, and other Excel features.
- Download the feature from Power BI, install it, and then select one or more datasets to use in Excel.


### Work management
#### Microsoft Planner
-  A project management tool to help you manage your projects and the teams working on them.
- Organize the activities in your project, starting with the overall plan, then assigning tasks to groups, known as buckets.
- Uses Microsoft 365 Groups to give project team members access to the plan and be assigned tasks.
- Integrates into Teams and Outlook to ensure that all your team members are fully updated.

#### Microsoft 365 Groups
- A service that works with the Microsoft 365 tools to collaborate with teammates when writing documents, creating spreadsheets, working on project plans, scheduling meetings, or sending emails.
- Resources include a **shared Outlook inbox**, a **shared calendar**, or a document library for collaborating on files.
- Group permissions = adding members to the group automatically gives them the permissions.
- You can create Microsoft 365 Groups from various tools;
	- Which tool you choose to start from depends a bit on what kind of group you're working with. :anger:

## Simplify device management with Microsoft Endpoint Manager

###  Modern management
- Modern management is a novel approach of managing Windows 10 similar to how mobile devices are managed by :bulb: **Enterprise Mobility Management (EMM)** solutions.
####  Benefits of modern management
- Easy to deploy and manage
	- Windows Autopilot, which is deeply integrated with Azure Active Directory (Azure AD) and Intune, simplifies and personalizes out-of-the-box (OOBE) experience for users, joins the device to Azure AD, and enrolls it in Intune.
- Always up-to-date
	-  Aligned updates, powerful insights driven by cloud intelligence, and a modern management approach with EMS.
- Intelligent security, built in
	- Windows Hello, Windows Defender Advanced Threat Protection (ATP), Windows Information Protection, Azure AD Identity Protection, Conditional Access...
- Proactive insights
	- Telemetry and cloud intelligence

####  Deployment and enrollment options
- Microsoft Autopilot for Windows 10 +  Microsoft Intune 
	- Avoid reimaging with cloud-based device management services 
	-  Dynamic provisioning of subscriptions, applications, devices, and user profiles.
- Windows Configuration Designer
	- Create self-contained provisioning packages
- System Center Configuration Manager
	- Use traditional imaging techniques (deploying custom images)

####  Updates and maintenance
- Windows-as-a-Service
	- Devices on **Windows 10 semi-annual channel (SAC)** versions receive the latest feature and quality updates through simple -- often automatic -- patching processes.
- Mobile Device Management (MDM) with Intune
	- Provide tools for applying Windows updates to client computers in your organization.
	- Configuration Manager allows rich management and tracking capabilities of these updates, including maintenance windows and automatic deployment rules.

####  Identity and authentication
- Azure Active Directory 	
	- Cloud-based identity, authentication, and management. 

You can envision user and device management as falling into these two categories:
- Corporate (CYOD) or personal (BYOD) devices: 
	- Mobile users for SaaS apps
- Domain joined Devices:
	- Traditional applications and access to secure resources.


###  Integrated solutions in Microsoft Endpoint Manager
:bulb: TO DO 

###  Intune
With Intune, you can:

-   Choose to be 100% cloud with Intune, or be co-managed with Configuration Manager and Intune.
-   Set rules and configure settings on personal and organization-owned devices to access data and networks.
-   Deploy and authenticate apps on devices -- on-premises and mobile.
-   Protect your company information by controlling the way users access and share information.
-   Be sure devices and apps are compliant with your security requirements.

When devices are enrolled and managed in Intune, administrators can:

-   See the devices enrolled, and get an inventory of devices accessing organization resources.
-   Configure devices so they meet your security and health standards. For example, you probably want to block jailbroken devices.
-   Push certificates to devices so users can easily access your Wi-Fi network, or use a VPN to connect to your network.
-   See reports on users and devices that are compliant, and not compliant.
-   Remove organization data if a device is lost, stolen, or not used anymore.

### Configuration Manager
![Larger Group of Devices](https://docs.microsoft.com/en-us/learn/wwl/simplify-device-management-with-microsoft-endpoint-manager/media/5-co-management-overview-666c6462.png)

:bulb: TO DO 

### AutoPilot and zero-touch deployment

Windows Autopilot enables you to:

-   Automatically join devices to Azure Active Directory (Azure AD) or Active Directory (via Hybrid Azure AD Join).
-   Auto-enroll devices into MDM services, such as Microsoft Intune (Requires an Azure AD Premium subscription for configuration).
-   Restrict the Administrator account creation.
-   Create and auto-assign devices to configuration groups based on a device's profile.
-   Customize out of box experience (OOBE) content specific to the organization.

:bulb: TO DO 


## Get more done and stay secure with Windows 10

-   Describe the options for deploying and supporting Windows.
-   Describe the deployment and release models for Windows-as-a-Service (WaaS), including deployment rings.
-   Describe the capabilities of Azure Virtual Desktop (AVD), and when it makes sense to implement it.

### Describe Windows-as-a-Service
- New features are released twice a year. By releasing new features in bite sized chunks, rather than major new versions, the work required by IT people is reduced.
- designed to make life simpler for both users and IT professionals. 
- There are two types of updates: 
	- Features (twice a year)
	- Quality fixes (once a month)
		- A cumulative update is released that includes all previous updates. 
- Servicing channels:
	- A method of controlling the frequency at which organizations deploy Windows 10 features.
	- Control how and when updates are applies.
	- MS offers three servicing channels:
		-   **Insider preview**. 
			- Windows features before general release, often during development. 
			- Allows to test and evaluate new features and provide feedback to Microsoft.
		-   **Semi-annual channel**. 
			- Feature updates are released to the semi-annual channel twice a year.
		-   **Long-term servicing channel**. 
			- For Specialist devices: medical equipment, IoT, ATMs. 
			- New features every two or three years.
- Deployment rings
	- Groups of devices that are used to pilot new features, before they are deployed to the rest of the organization.
- Manage Windows-as-a-Service
	- In Configuration Manager, you can view the state of Windows-as-a-Service (WaaS) in your environment. 
		- To create servicing plans to form deployment rings 
		- Ensure Windows 10 systems are kept up to date when new builds are released.
		- View alerts when Windows 10 clients are near end of support for their Semi-Annual Channel build.


### Explore deployment methods for Windows 
Deployment factors:
-   Business requirements.
-   Environment considerations.
-   Amount of administrative control needed.
-   Network capacity.
-   Current deployment capabilities.

Deployment tools:
- Windows Autopilot
- Microsoft Deployment Toolkit for Windows, 
- Intune 
- Configuration Manager for Windows

Deployment sources:
- Windows from the cloud
- from a local source on your network.

Windows 10 includes the following new deployment tools and methods:
-   **Windows Autopilot**. 
	- Customize the out-of-box experience (OOBE) to deploy apps and settings that are pre-configured for your organization. 
	- Use with Configuration Manager to upgrade Windows 7 or Windows 8.1 to Windows 10.
-   **In-place upgrade**. 
	- Upgrade a device’s operating system without reinstalling. 
	- You can migrate apps, user data, and settings from one version of Windows to another 
-   **Dynamic provisioning**. 
	- Create a provisioning package to quickly configure one or more devices, even those without network connectivity. 
	- You create provisioning packages with the **Windows Configuration Designer** and can install them over a network, from removable media, or in near field communication (NFC) tags or barcodes.
-   **Subscription activation**. 
	- Use a subscription to switch from one edition of Windows 10 to another. 
	- Ex: When a licensed user signs into a device (and they have Windows 10 E3 or E5 license), the OS changes from Windows 10 Pro to Windows 10 Enterprise, and all the appropriate Windows 10 Enterprise features are unlocked. 
	- :anger: If the subscription expires (or is transferred to another user), the device reverts seamlessly to Windows 10 Pro edition, after a grace period of up to 90 days.


### Explain how Windows stays secure and up-to-date
- To reduce bandwidth consumption, you can enable peer-to-peer content sharing:
	- Delivery Optimization
		- Source content from other devices on their local network that have already downloaded the updates, or from peers over the internet.
	- BranchCache
		- A bandwidth optimization technology
		- Files are cached on each individual client, and other clients can retrieve them as needed.
### Describe servicing options for Windows
- :bulb: How to deploy Windows 10 upgrades using task sequences, and automated servicing plans in System Center Configuration Manager. 
- :bulb:  How to use Microsoft Intune to manage Windows 10 updates on all your devices.
- :bulb:  Create a task sequence in Configuration Manager to automatically upgrade an operating system on a destination computer
- :bulb:  Using Microsoft Intune, you can manage your Windows updates. This includes viewing information about the update, approving or declining the update, and viewing the computers that will install the update when if it is approved.


### Describe Azure Virtual Desktop (AVD)
- A service that allows users to connect to a Windows desktop running in the cloud. 
- A desktop and app virtualization service that runs on Azure.
- Use cases:
	-   Set up a  **multi-session Windows 10 deployment**  that delivers a full Windows 10 with scalability.
	-   **Virtualize Office 365 ProPlus**  and optimize it to run in multi-user virtual scenarios.
	-   Provide  **Windows 7 virtual desktops**  with free Extended Security Updates.
	-   Bring your existing Remote Desktop Services (RDS) and Windows Server desktops and apps to  **any computer**.
	-   **Virtualize**  both desktops and apps.
	-   Manage Windows 10, Windows Server, and Windows 7 desktops and apps with a  **unified management**  experience.

## Harness business intelligence with Microsoft 365 analytics and reporting
### Explore how Workplace Analytics can help organizations improve productivity
### Explore the Microsoft 365 admin center
### Describe the additional admin centers in Microsoft 365
