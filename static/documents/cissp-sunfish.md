# CISSP

Role: risk advisor/CISO, so do not fix problems, follow the process, report to senior management.
Human life is always the major priority; humans are always the weakest link in security.
All decisions start with risk management; risk management defines how much security is enough because it starts by evaluating the environment.
Security transcends technology.
Senior management is ultimately responsible for security; everyone else follows policies approved by senior management.
Security by design is always better than added security.
Layered defense grants better security than separated controls.
The "better" solution tends to be that that broadly solves the problem, not just part of it.

## D1. Security and Risk Management

### Business Continuity Management (BCM)

- Goals

	- 1. Safety of people
	- 2. Minimize the damage
	- 3. Survival of business

- Disaster recovery plan (DRP)

  Objective: provide a short-term plan for dealing with specific IT-oriented disruptions.
  Focus: efficiently attempting to mitigate the impact of a disaster by preparing the immediate response and recovery of critical IT systems. 
  Short-term.

	- Recovery strategy

		- Recovery Sites

		  Any recovery site MUST be geographically remote.

			- Cold

			  Weeks to activate, usually the less expensive.

			- Hot

			  Hours to activate, very expensive.

			- Warm

			  Days to activate, mid-term between hot and cold in terms of expenses.

			- Mobile

			  Days or hours to activate.

			- Reciprocal agreement

			  A.K.A., mutual aid agreement (MAA). Bidirectional agreement between two organizations in which one organization promises another organization that it can move in and share space if it experiences a disaster.

				- Mutual aid agreement (MAA)

			- Redundant

			  Instant or seconds to activate, owned by the company (not a service), most expensive.

	- Recovery plan development
	- Training, awareness, and documentation
	- Testing and maintenance

		- Read-through

		  Distribution of recovery checklists to disaster recovery personnel for review.

		- Structured walk-through

		  "Tabletop" exercises that involve assembling the disaster recovery team to discuss a disaster scenario.

		- Simulation

		  Similar to structured walk-throughs, but are more comprehensive and can involve the interruption of noncritical activities.

		- Parallel

		  Relocate personnel to the alternate recovery site and implement site activation procedures without interrupting the main facility.

		- Full-interruption

		  Just like parallel tests, but involve shutting down the primary site.

	- Phases

		- Recovery

		  Includes the preparation of the offsite facility (if needed), the rebuilding of the network and systems, and the organization of staff to move into a new facility.

		- Reconstitution

		  Time for the company to move back into its original site or a new site, the company is ready to enter into the reconstitution phase. Usually conducted by the salvage team.

- Business continuity plan (BCP)

  Objective: to ensure that the business will continue to operate before, throughout, and after a disaster event is experienced.
  Focus: business as a whole, ensuring that those critical services or functions the business provides or performs can still be carried out both in the wake of a disruption and after the disruption has been weathered.
  Long-term.

	- Project scope and planning

		- Structured analysis
		- Creation of a BCP team

			- BCP coordinator

		- Assessment of the resources
		- Analysis of legal and regulatory

	- Business impact assessment (BIA)

	  Formal method for determining how a disruption to the IT systems of an organization will impact the organization's requirements, processes, and interdependencies with respect to the business mission. The primary goal of the BIA is to determine the Maximum Tolerable Downtime (MTD) for a specific IT asset, in other words, the focus of BIA is on availability.

		- Identify critical assets

			- Gather data
			- Analyze data
			- Calculate the risk

		- Prioritize critical assets

			- Dependency charts

		- Fail/Recovery metrics

			- RPO

			  Amount of data loss or system inaccessibility (measured in time) that an organization can withstand.

			- MTD

			  RTO + WRT = MTD

				- RTO

				  Deals with getting the infrastructure and systems back up and running.

				- WRT

				  Deals with restoring data, testing processes, and then making everything "live" for production purposes.

			- MTBF

			  Quantifies how long a new or repaired system will run before failing.

			- MTTR

			  Describes how long it will take to recover a specific failed system.

			- MTTF

			  Normally calculated for items that will not be repaired when they fail, such as a tape.

	- Continuity planning

		- Strategy development
		- Provisions and processes
		- Plan approval
		- Plan implementation
		- Training and education

	- Plan approval and implementation
	- Continuity of operations plan (COOP)

	  Focuses on restoring an organization’s mission essential functions (MEF, e.g., senior management and core business areas) at an alternate site and performing those functions for up to 30 days before returning to normal operations.

		- 1. Operations assessment

		  Assessing how the organization operates to identify mission-critical staff, materials, procedures, and equipment.

		- 2. Review

		  Review the business process flowchart.

		- 3. Identify stakeholders

		  Identify suppliers, partners, contractors, and other businesses the organization interacts with on a daily basis, and create a list of these and other businesses the organization could use in an emergency.

- Frameworks

	- NIST SP 800-34

	  Contingency Planning Guide for Federal Information Systems
	  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-34r1.pdf

		- 1. Develop the contingency planning policy
		- 2. Conduct the business impact analysis (BIA)
		- 3. Identify preventive controls

			- See NIST 800-37 step 3: Select

		- 4. Create contingency strategies

			- Backups
			- Alternate sites
			- Equipment replacement

		- 5. Develop contingency plan

			- Supporting information
			- Activation and notification
			- Recovery
			- Reconstitution
			- Appendices

		- 6. Ensure plan testing, training, and exercises
		- 7. Ensure plan maintenance

	- ISO/IEC 27031

	  Focus on BCP. Enable an organization to measure its continuity, security and hence readiness to survive a disaster in a consistent and recognized manner.

		- ISO/IEC 24762

		  Focus on DRP.

	- ISO 22301

	  Specifies the requirements for setting up and managing an effective Business Continuity Management System (BCMS) for any organization, regardless of type or size.

### Relevant Organizations

- Organization for Economic Co-operation and Development (OECD)
- Internet Engineering Task Force (IETF)

	- Internet Architecture Board (IAB)

- European Union (EU)
- North Atlantic Treaty Organization (NATO)
- International Information System Security Certification Consortium (ISC)2

### Laws & Regulations

Be familiar with ​why laws are developed and put in place and their overall goals,​ instead of memorizing specific laws and dates.

- Legal systems

	- Civil/Legal system
	- Common

		- Criminal
		- Civil
		- Administrative

	- Religious/Customary

- Financial damage

	- Statutory
	- Compensatory
	- Punitive

- Legal liability
- Computer crimes

	- Computer as target
	- Computer as tool
	- Enticement

	  Occurs when an individual who was already planning to commit a crime is eventually lured into doing so at the urging of law enforcement.

	- Entrapment

	  Occurs when an individual who otherwise had no intention of committing a crime is lured into doing so at the urging of law enforcement.

- Intellectual property

  Intangible property

	- Trademark

	  Name, logo, slogan, symbol, image.
	  TM : unregistered mark
	  R: formally registered mark
	  Does not expire.

	- Trade secret

	  Noncompete and nondisclosure agreements (NCA/NDA) are two of the most common protection methods used. Does not expire.

		- Economic Espionage Act (1996)

		  Provides necessary structure to deal with espionage (data breaches), meaning that assets don't necessarily need to tangible to be stolen.

	- Patent

	  Refers to the rights to use, make or sell an invention. Generally lasts 20 years.

	- Copyright

	  Precludes unauthorized duplication, distribution, or modification of a creative work. Expires after 70 years.

		- License

		  Enables a copyright owner to grant specific uses of copyrighted material to others.

		- Digital Millennium Copyright Act (DMCA, 1998)

		  DMCA guarantees copy-prevention mechanisms in CD/DVD and limits the liabilities of ISPs.

	- Attacks

		- Piracy

		  Focus on infringement of copyright.

		- Cybersquatting

		  Focus on infringement of trademarks.

		- Typosquatting

		  Focus on infringement of trademarks.

		- Counterfeiting

		  Occurs when an entity creates a fake product and attempts to pass it off as another entity's product by using that entity's trademark.

		- Dilution

		  Occurs when an entity uses a trademarked term as a generic term.

		- Espionage

		  Could be used for many purposes, including to steal trade secrets.

- Privacy

  Protection of the confidentiality of personal information.

	- General Data Protection Regulation (GDPR, 2016)

		- Companies must inform authorities of major data breaches within 72 hours
		- Each EU member nation must create a centralized data protection authority
		- Individuals must have access to their own data
		- Information regarding an individual must be transferrable to another service provider at the individual's request
		- Individuals retain the "right to be forgotten" and have their information deleted if it is no longer required

	- OECD Privacy Guidelines
	- Privacy Shield Agreement (2016)

	  Replaced the Safe Harbor.

		- EU-US Safe Harbor

	- US Privacy Law: 4th Amendment

	  A search warrant is needed before searching private property.

	- Federal Privacy Act (1974)

	  How government agencies should maintain personal data, a primitive form of GDPR aimed at the government.

	- Gramm-Leach-Bliley Act (GLBA, 1999)

	  Privacy for financial institutions (also covers data breaches), giving customers the option to prohibit the sharing of their information.

	- USA Patriot Act (2001)

	  Changed existing laws by reducing restrictions of agencies that provided more privacy, thus reducing privacy of citizens mainly because of surveillance.

	- Health Insurance Portability and Accountability Act (HIPAA, 2009)

	  Subtitle D of HITECH, addressing privacy and security concerns with electronic transmission of health information. Also deals with data breaches, especially covering Personal Health Information (PHI).

- Security

	- Computer Fraud and Abuse Act (CFAA, 1986)

	  Unauthorized (including escalation of privileges) access to information, using government computers without authorization, trafficking computer passwords. Over-broad law, used to prosecute Aaron Schwartz.

	- Sarbanes-Oxley Act (SOX, 2002)
	- Federal Information Security Management Act (FISMA, 2002)

	  Requires that federal agencies implement an information security program that covers the agency operations and include the activity of contractors in their security management program. NIST SP 800-53 is used to help ensure compliance with FISMA.

	- Payment Card Industry Data Security STANDARD (PCI DSS, 2006)

	  Joint force among credit card companies to prevent identity theft and credit card fraud by 12 requirements.

- Wassenaar Arrangement

  Limits the export of cryptographic solutions.

### Ethics

- (ISC)2 Code of Ethics

  If there's a conflict among any of the canons, the professional must adhere to the canon that ranks highest (1 > 2 > 3 >4).

	- Preamble
	- Canons

		- 1. Protect society, the common good, necessary public trust and confidence, and the infrastructure.
		- 2. Act honorably, honestly, justly, responsibly, and legally.
		- 3. Provide diligent and competent service to principals.
		- 4. Advance and protect the profession.

	- Guidance

	  Advisory

- Computer Ethics Institute

	- Ten commandments of computer ethics

	  http://computerethicsinstitute.org/publications/tencommandments.html

- RFC 1087

	- Ethics and the internet

	  https://tools.ietf.org/html/rfc1087

### Risk Management

- Assets

	- Value

		- Quantitative
		- Qualitative

- Vulnerability

  Any type of weakness.

- Threat

  Any action or inaction that could cause damage, destruction, alteration, loss, or disclosure of assets or that could block access to or prevent maintenance of assets.

	- Vector

	  Potential medium that an attacker can use to exploit a vulnerability.

	- Agent

	  THREAT AGENT gives rise to THREAT exploits VULNERABILITY leads to RISK can damage ASSET and causes an EXPOSURE can be countermeasured by SAFEGUARD directly affects THREAT AGENT.

		- Advanced Persistent Threat (APT)

		  Sophisticated adversaries with advanced technical skills and significant financial resources. These attackers are often military units, intelligence agencies, or shadowy groups that are likely affiliated with government agencies.

			- APT28. Fancy bear
			- APT29. Cozy bear

		- Spy

			- Other companies

		- Insider

			- Grudge attack

		- Terrorist

			- Disrupt normal life

		- Hacktivist

			- Political belief

		- Script kid

			- Thrill attack

	- Frameworks

		- STRIDE

		  Developed by Microsoft, focus on application or operating system threats.
		  
		  Spoofing
		  Tampering
		  Repudiation
		  Information disclosure
		  Denial of service
		  Elevation of privilege.

			- Application threats

		- PASTA

		  Process for attack simulation and threat analysis. Seven-stage, risk-centric approach.
		  
		  I: Definition of the Objectives (DO) for the Analysis of Risks
		  II: Definition of the Technical Scope (DTS)
		  III: Application Decomposition and Analysis (ADA)
		  IV: Threat Analysis (TA)
		  V: Weakness and Vulnerability Analysis (WVA)
		  VI: Attack Modeling & Simulation (AMS)
		  VII: Risk Analysis & Management (RAM)

			- Risk-centric

		- DREAD

		  Designed to provide a flexible rating solution based on 5 questions:
		  
		  Damage potential: how severe the damage likely to be if the threat is realized?
		  Reproducibility: how complicated it is for the attacker to reproduce the exploit?
		  Exploitability: how hard it is to perform the attack?
		  Affected users: how many users are likely to be affected?
		  Discoverability: how hard it is for an attacker to discover the weakness?

			- Rating system

		- Trike

			- Risk-centric

		- VAST

		  Visual, agile, and simple threat. Based on Agile.

			- Agile-based

- Risk

  Possibility or likelihood that a threat will exploit a vulnerability resulting in a loss such as harm to an asset.
  
  Threats exploit vulnerabilities, which results in exposure. Exposure is risk, and risk is mitigated by safeguards. Safeguards protect assets that are endangered by threats.

	- Categories

		- Physical damage
		- Human interaction
		- Equipment malfunction
		- Attacks (inside and outside)
		- Misuse of data
		- Loss of data
		- Application error

	- Threat * vulnerability
	- Impact
	- Likelihood
	- Human safety is paramount ALWAYS
	- Analysis

		- Quantitative

		  Requires experienced assessors
		  Requires numerical data
		  Provides results that are measurable
		  More difficult to perform and require more time than qualitative risk assessments

			- AV ($)
			- EF (%)
			- SLE ($) = AV * EF
			- ARO (#)
			- ALE ($) = SLE * ARO
			- Total risk = threats * vulnerability * AV
			- Residual risk = total risk * control gaps
			- TCO

			  Total cost of a mitigating safeguard.

			- ROI

			  Amount of money saved by implementing a safeguard.

			- Cost benefit = ALE (before safeguards) - ALE (after safeguards) - annual cost of safeguards

				- > 0: good to implement
				- <= 0: not good to implement

		- Qualitative

		  Does not require a lot of numerical data
		  Provides results that are descriptive rather than measurable
		  Easier to perform and require less time than quantitative risk assessments
		  Recommended for assessors who do not have much experience performing risk assessments, but have extensive experience with

			- Risk analysis matrix
			- Delphi technique

			  Anonymous feedback-and-response process used to enable a group to reach an anonymous consensus during a qualitative risk assessment.
			  
			  The participants are usually gathered into a single meeting room. To each request for feedback, each participant writes down their response on paper anonymously. The results are compiled and presented to the group for evaluation. The process is repeated until a consensus is reached.

		- Hybrid

		  Quantitative + qualitative

- Decision

	- Avoid
	- Transfer
	- Mitigate

		- Security controls

			- Categories

				- Administrative

				  Policies, standards, baselines, guidelines, and procedures

				- Technical/Logical

				  Hardware (technical) and software (logical) mechanisms

				- Physical

				  Physical mechanisms

			- Types

				- Safeguards

				  Proactive mechanisms

					- Directive

					  Direct or control the actions of subjects to force or encourage compliance.

					- Deterrent

					  Discourage violation of security policies.

					- Preventative

					  Thwart or stop unwanted or unauthorized activity from occurring.

				- Countermeasures

				  Reactive mechanisms

					- Detective

					  Discover or detect unwanted or unauthorized activity.

					- Corrective

					  Provide various options to other existing controls to aid in enforcement.

					- Recovery

					  Modifies the environment to return systems to normal.

					- Compensating

					  More advanced or complex abilities than Corrective controls, an extension.

	- Accept

		- Documentation

- Frameworks

	- NIST SP 800-37 (RMF)

	  Risk Management Framework for Information Systems and Organizations
	  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r2.pdf

		- 1. Prepare

		  Prepare to execute the RMF from an organization and a system-level perspective by establishing a context and priorities for managing security and privacy risk.

		- 2. Categorize

		  Categorize the system and the information processed, stored, and transmitted by the system based on an analysis of the impact of loss.

		- 3. Select

		  Select an initial set of controls for the system and tailor the controls as needed to reduce risk to an acceptable level based on an assessment of risk.

		- 4. Implement

		  Implement the controls and describe how the controls are employed within the system and its environment of operation.

		- 5. Assess

		  Assess the controls to determine if the controls are implemented correctly, operating as intended, and producing the desired outcomes with respect to satisfying the security and privacy requirements.

		- 6. Authorize

		  Authorize the system or common controls based on a determination that the risk to organizational operations and assets, individuals, other organizations, and the Nation is acceptable.

		- 7. Monitor

		  Monitor the system and the associated controls on an ongoing basis to include assessing control effectiveness, documenting changes to the system and environment of operation, conducting risk assessments and impact analyses, and reporting the security and privacy posture of the system.

	- NIST SP 800-39

	  Managing Information Security Risk
	  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-39.pdf

		- Tiers

			- 1. Organization
			- 2. Mission/Business processes
			- 3. Information systems

		- Process

			- 1. Frame

			  Risk framing establishes the context and provides a common perspective on how organizations manage risk.

			- 2. Assess

			  Risk assessment identifies, prioritizes, and estimates risk to organizational operations (i.e., mission, functions, image, and reputation), organizational assets, individuals, other organizations, and the Nation, resulting from the operation and use of information systems.

			- 3. Respond

			  Risk response identifies, evaluates, decides on, and implements appropriate courses of action to accept, avoid, mitigate, share, or transfer risk to organizational operations and assets, individuals, other organizations, and the Nation, resulting from the operation and use of information systems.

			- 4. Monitor

			  Risk monitoring provides organizations with the means to:
			  verify compliance; 
			  determine the ongoing effectiveness of risk response measures;
			  identify risk-impacting changes to organizational information systems and environments of operation.

	- NIST SP 800-30

	  Guide for Conducting Risk Assessments
	  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-30r1.pdf

		- 1. Prepare for the assessment
		- 2. Conduct the assessment

			- Identify threat sources and events
			- Identify vulnerabilities and predisposing conditions
			- Determine likelihood of occurrence
			- Determine magnitude of impact
			- Determine risk

		- 3. Communicate results
		- 4. Maintain assessment

	- Operationally Critical Threat, Asset, and Vulnerability Evaluation (OCTAVE)

	  Team-oriented risk management methodology that employs workshops and is commonly used in the commercial sector. By Carnegie Mellon University.

		- Phase 1. Develop initial security strategies
		- Phase 2. Technical view - identify infrastructure vulnerabilities
		- Phase 3. Risk analysis - develop security strategies and plans

	- Facilitated Risk Analysis Process (FRAP)

	  Low-cost method of evaluating risk for one system or process at a time. Focused on systems that really need assessing.

	- ISO/IEC 27005

	  Integrates with ISMS (ISO 27001), dealing with IT and softer security issues.

	- ISO 31000

	  Can be broadly used in the organization.

	- Risk IT (ISACA)

	  Covers gaps in NIST SP 800-37 and ISO 31000.

	- PUSH

	  Mathematically associates the impact of a risk event with the likelihood that the risk event will occur.

	- CCTA Risk Analysis and Management Method (CRAMM)

	  3-stage approach to evaluate technical and nontechnical security aspects.

	- Security Officers Management and Analysis Project (SOMAP)

	  Open-source method for evaluating and managing risk.

	- Factor Analysis of Information Risk (FAIR)
	- Threat Agent Risk Assessment (TARA)

### Security Governance

- NIST SP 800-18

  Guide for Developing Security Plans for Federal Information Systems
  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-18r1.pdf

	- System inventory
	- Responsibilities
	- Security controls
	- Security plan development

- Plans

	- Strategic

		- 5 years

	- Tatical

		- 6-12 months

	- Operational

		- Days or weeks

- Security policy

  Defines the scope of security needed by the organization, an overview or generalization of an organization's security needs.
  Purpose: the reason the policy exists.
  Scope: entities covered by the policy.
  Responsibilities: what covered individuals must do.
  Compliance: how to measure its effectiveness and consequences for violations.

	- Standards

	  Define compulsory requirements for the homogenous use of hardware, software, and security controls.

		- Scoping
		- Tailoring

	- Baselines

	  A baseline defines the minimum level of security that every system throughout the organization must meet. They are optional/discretionary.

	- Guidelines

	  Offers recommendations on how standards and baselines are implemented and serves as an operational guide for both security professionals and users. They are optional/discretionary.

	- Procedures

	  Detailed step-by-step how-to document that describes the exact actions necessary to implement a specific security mechanism, control, or solution.

- Personnel

	- Self

		- Onboarding

			- Job descriptions
			- Job responsibilities
			- Background checks
			- Job training
			- Job action warnings
			- Acceptable use policies (AUP)
			- Nondisclosure agreement (NDA)
			- Noncompete agreement (NCA)

				- Expiration date

			- Privacy declaration

		- Least privilege
		- Separation of duties
		- Job rotation/Cross training
		- Mandatory vacations
		- Performance reviews
		- Awareness

		  Goal is to bring security to the forefront and make it a recognized entity for ALL users.

		- Training

		  Teaching employees to perform their work tasks and to comply with the security policy. Typically hosted by an organization and is targeted to GROUPS of employees with similar job functions.

		- Education

		  Detailed endeavor in which students/users learn much more than they actually need to know to perform their work tasks.

		- Exit interviews / Terminations

			- Preferably at the end of midweek shift

	- Third-party

		- Vendor
		- Consultant
		- Contractor

	- Outsourcing

		- Offshoring

		  Relocation of a business process from one country to another.

	- Service providers

		- Contracts

			- SLA

			  Stipulates all expectations regarding the behavior of the department or organization that is responsible for providing services and the quality of those services.

			- Attestation
			- Right to audit

				- Penetration test

		- Procurement
		- Vendor governance

### Concepts

- NIST SP 800-12

  An Introduction to Information Security
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-12r1.pdf

	- Governance

		- Information security policy

			- Policy elements

				- Purpose

				  The reason the policy exists.

				- Scope

				  Entities covered by the policy.

				- Responsibilities

				  What individuals must do to comply.

				- Compliance

				  How to measure the effectiveness of the policy and consequences for violating.

	- Management
	- Risk

		- Threats
		- Vulnerabilities

	- Roles
	- Glossary

- Trusted recovery

  Provides assurances that after a failure or crash, the system is just as secure as it was before the failure or crash occurred.

	- Physical

	  Human safety must be taken into account.

		- Fail safe

		  A fail-safe electrical lock will be unlocked when power is removed.

		- Fail secure

		  A fail-secure electrical lock will be locked when power is removed.

	- Electronic

	  The choice is dependent on whether security or availability is more important after a failure.

		- Fail open

		  Will fail in an open state, granting all access.

		- Fail secure

		  Will default to a secure state in the event of a failure, blocking all access.

- Session

  Any authenticated exchange between two parties that is used to carry on a conversation, with a discrete beginning, period of activity, and termination.

- Attack surface

  What is available to be used by an attacker against the product itself.

- Out-of-band

  Separate channel of communication used to avoid any vulnerabilities.

- Overt channel

  Transmission or other communication that is authorized and is performed in compliance with security policies.

- Compartmentalization

  Access control principle that isolates groups from users based on the information or access required by the groups --information does not flow between groups.

- Defense in depth

  AKA Layered defense

- Nonrepudiation

	- Integrity
	- Authentication

- Entities

	- Subjects

	  Active entity

	- Objects

	  Passive entity

- IAAA

	- Identification

	  Method by which a subject claims to have specific identity --username, account number, or email address.

	- Authentication

	  Process by which a system verifies the identity of the subject, usually by requiring a piece of information that only the claimed identity should have --password, cryptographic key, PIN, anatomical attribute, or token.

	- Authorization

	  Determination if a subject has the necessary rights and privileges to carry out the requested actions, like looking at some type of access control matrix or comparing security labels.

	- Accountability

	  Tracing an action to a subject.

- Due care

  Taking the precautions that a reasonable and competent person would take in the same situation, applicable to everyone.  Opposite: gross negligence.

	- Prudent man rule

	  Requires senior executives to take personal responsibility for ensuring the due care. Allowed organizations and executives to minimize punishment for infractions by demonstrating they used due diligence.

	- Informal

- Due diligence

  Doing everything in one's power to prevent an incident, usually associated with leaders. Due diligence is the management of due care.

	- Follows a process

- CIA

	- Confidentiality
	- Integrity
	- Availability
	- DAD (not CIA)

	  The opposite of CIA

		- Disclosure
		- Alteration
		- Destruction

## D2. Asset Security

### Asset

- Personnel
- Information
- Systems
- Devices
- Facilities

### Data Lifecycle

- Creation/Capture
- Data classification

	- Criteria

		- Value of the data
		- Level of damage if exposed or lost
		- Who should access the data
		- Sensitivity

		  Refers to the confidentiality of data and the need to control who has access to learn its contents.

			- Confidentiality
			- Exposition/Disclosure

		- Criticality

		  Data is considered critical to a business operation if key business processes depend on that data being available at all necessary times.

			- Availability
			- Lost/Destruction

	- Roles

		- Mission/Business owner

		  Person who is ultimately responsible for the security maintained by an organization. Signs off all policies, effectively authorizing and supporting the security policy. A.K.A: senior manager.

		- Data owner

		  High-level manager responsible for classifying and protecting the  information, as well as the frequency of data backup. A.K.A: information owner.

			- Accreditation
			- Data custodian

			  Responsible for implementing the data owner's prescribed protection, such as performing data backups, patching systems, and configuring antimalware.

		- System owner

		  Manager responsible for the computers that house the data, including OS updates and patches, hardware security, and hardening.

		- Data controller

		  Create and manage sensitive data, typically human resources employees.

			- Data processor

			  Manage data on behalf of data controllers, like an outsourced payroll.

		- Security professional
		- User
		- Auditor

		  Responsible for reviewing the data.

	- Levels

		- Military/Government

			- Top Secret

			  Disclosure could reasonably be expected to cause exceptionally GRAVE DAMAGE to national security.

			- Secret

			  Disclosure could reasonably be expected to cause SERIOUS DAMAGE to national security.

			- Confidential

			  Disclosure could reasonably be expected to cause DAMAGE to national security.

			- Sensitive but unclassified

			  Minor secret, no serious damage.

			- Unclassified

		- Commercial

			- Confidential

			  Disclosure could affect the company.

			- Private

			  For use within the company, but no impact.

			- Sensitive

			  Precautions on integrity and confidentiality.

			- Public

			  Disclosure is not welcome, but no impact.

	- Subjects

		- Clearances
		- Formal access approval
		- Need-to-know
		- Capability table/list

		  Specifies the access rights a certain subject possesses pertaining to specific objects. Similar to ACLs for objects.

	- Objects

		- Labels

		  Refers to the use of security attributes for internal data structures within information systems.

			- Marking

			  Refers to the use of human-readable security attributes.

		- ACL

		  Lists of subjects that are authorized to access a specific object, and they define what level of authorization is granted. Similar to capability tables for subjects.

			- Examples

			  Permits traffic from 10.1.1.2 to 172.16.1.1:
			  permit tcp host 10.1.1.2 host 172.16.1.1 eq smtp
			  
			  Permits all UDP traffic:
			  permit udp host 10.1.1.2 host 172.16.1.1 
			  
			  Denies all ICMP traffic:
			  deny icmp any any
			  
			  Allows web traffic:
			  permit tcp host 10.1.1.2 host 172.16.1.1 eq www

- Data storage

	- Persistence

		- Volatile
		- Nonvolatile

	- Access

		- Primary
		- Secondary

	- WORM
	- Cache

		- CPU registers
		- L1
		- L2

	- RAM

		- DRAM

		  Capacitors, must be refreshed, requires more energy, slower, cheaper.

		- SRAM

		  Flip-flops, does not need to be refreshed, requires less energy, faster, more expensive.

	- ROM

		- PROM
		- EPROM
		- EEPROM

			- Flash

			  Specific type of EEPROM where bytes are written in large sectors.

- Data usage
- Data archival
- Data destruction/purging

	- Data Remanence

	  Data that persists beyond noninvasive means to delete it.

		- Data disposal

			- Erasing/Deleting/Formating
			- Clearing/Overwriting

				- Purging

				  Intensive clearing, will repeat the process multiple times.

			- Degaussing
			- Destruction

				- Shredding
				- Incineration
				- Pulverizing

		- Declassification

		  Any process that purges media or a system in preparation for reuse in an unclassified environment. Often the efforts required to securely declassify media are significantly greater than the cost of new media for a less secure environment.

			- Object reuse

			  Reassigning to a subject media that previously contained one or more objects --this object can be physical or logical, such as computers, CD-RWs, variables, memory locations, and registers.

		- NIST SP 800-88

		  Guidelines for Media Sanitization
		  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf

			- Types of media

				- Physical
				- Electronic

			- Types of sanitization
			- Cryptography erase (CE)
			- Scope
			- Roles

### Data Protection

- In motion

	- Encryption

		- Link

		  Encrypts all the data along a specific communication path; not only is the user information encrypted, but the header, trailers, addresses, and routing data that are part of the packets are also encrypted. Occurs on lower layers of OSI model.

			- Slows down routing

		- End-to-end

		  Headers, addresses, routing, and trailer information are not encrypted, enabling attackers to learn more about a captured packet and where it is headed. With end-to-end encryption only the data payload is encrypted. Occurs on higher layers of OSI model.

			- More susceptible to eavesdroppers and sniffers

- In use

	- Process isolation
	- Memory protection

- At rest

	- Encryption
	- Backups

### Privacy

- Roles

	- DPO

- Privacy policy
- Personal data

	- PII/PHI/...

	  Examples include: phone numbers, social security numbers, email address, mailing address, and name.

		- NIST SP 800-122

		  Guide to Protecting the Confidentiality of Personally Identifiable Information (PII)
		  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-122.pdf

			- Confidentiality impact levels
			- Safeguards
			- Incident response

	- Direct identifiers
	- Indirect identifiers
	- Masking

	  Method of creating a structurally similar but inauthentic version of an organization's data that can be used for purposes such as software testing and user training.

	- Anonymization

	  Process of removing all relevant data so that it is impossible to identify the original subject or person.

	- Pseudonymization

	  Process of using pseudonyms to represent other data and can be reversed, so the PII would be revealed. Example: client 78424: John Doe.

## D3. Security Architecture and Engineering

### Frameworks

- Enterprise security architecture

	- Zachman

	  Model for the development of ENTERPRISE architectures with two-dimensional model that uses six basic communication interrogatives:
	  
	  What,
	  How,
	  Where,
	  Who,
	  When, and
	  Why
	  
	  Intersecting with different perspectives:
	  
	  Executives,
	  Business Managers,
	  System Architects,
	  Engineers,
	  Technicians, and
	  Enterprise-wide
	  
	  To give a holistic understanding of the enterprise.

	- Sabsa

	  Model and methodology for the development of information SECURITY enterprise architectures.

	- TOGAF

	  Model and methodology for the development of ENTERPRISE architectures. TOGAF can be used to develop the following architecture types:
	  
	  Business architecture
	  Data architecture
	  Applications architecture
	  Technology architecture

	- DoDAF
	- MODAF

- Security

	- ISO/IEC 27000 series

		- 27002: Code of practice
		- 27003: ISMS implementation
		- 27004: Security measurement
		- 27005: Risk management
		- 27031: BCP
		- 27034: application security

	- NIST SP 800-53

	  Security and Privacy Controls for Information Systems and Organizations
	  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf

		- Security controls
		- Privacy controls
		- Baselines

		  Comprehensive list of controls prioritized by low, medium, and high-impact.

- IT

	- COBIT

	  Defines goals for the controls that should be used to properly manage IT and to ensure IT maps to business needs, not specifically just security needs. "what is to be achieved"

	- ITIL

	  Best practices for IT service management. "how to achieve it"

- Privacy

	- OECD Guidelines

		- Collection limitation
		- Data quality
		- Purpose
		- Use limitation
		- Security safeguards
		- Openness
		- Individual participation
		- Accountability

### Evaluation Criteria

- Certification

  Complete evaluation of a product, system, process, event, or a skill that’s normally measured against an existing benchmark, norm, or standard.

	- TCSEC (Orange Book)

		- Confidentiality only
		- Single-box only
		- Security divisions

			- A. Verified protection
			- B. Mandatory protection
			- C. Discretionary protection
			- D. Minimal protection

	- ITSEC

		- Confidentiality & integrity
		- Functional levels

			- Same as TCSEC

		- Assurance levels

			- E0-E6

	- Common criteria

	  Accredited products:  https://www.niap-ccevs.org/Product/index.cfm

		- Protection profile (PP)

		  Set of security requirements and objects for the type of product to be tested.

		- Target of evaluation (ToE)

		  System or product to be tested.

		- Security target (ST)

		  Documentation that describes the ToE and any security requirements.

		- Security functional & assurance requirements
		- EAL

		  Rating level assigned to the ToE.

			- EAL1. Functionally tested
			- EAL2. Structurally tested
			- EAL3. Methodically tested and checked
			- EAL4. Methodically designed, tested, and reviewed
			- EAL5. Semi formally designed and tested
			- EAL6. Semi formally verified, designed, and tested
			- EAL7. Formally verified, designed, and tested

		- ISO/IEC 15408

- Accreditation

  Formal declaration by a third party (neutral) that the certification was carried out in a way that accords with the relevant standards and/or norms of the certification program. Includes senior management approval.

### Cloud Computing

- NIST SP 800-145

  The NIST Definition of Cloud Computing
  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf

- Service models

	- IaaS
	- PaaS
	- SaaS

- Deployment models

	- Private
	- Public
	- Hybrid
	- Community

- Technologies

	- Virtualization
	- Software-defined networks (SDN)
	- Big data

- Cloud access security broker (CASB)

  Enforce and ensure that proper security measures are implemented between a cloud solution and a customer organization.

### Virtualization

- Host

	- Hypervisor / Virtual machine monitor

		- Type 1 (bare metal)
		- Type 2 (application)

- Guest

	- Virtual machine

- VDI

	- Application virtualization

### Industrial Control Systems (ICS)

Consists of combinations of control components (e.g., electrical, mechanical, hydraulic, pneumatic) that act together to achieve an industrial objective (e.g., manufacturing, transportation of matter or energy).

- NIST SP 800-82

  Guide to Industrial Control Systems (ICS) Security
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-82r2.pdf

	- Components

		- Supervisory control and data acquisition (SCADA)

		  Used to control dispersed assets where centralized data acquisition is as important as control.

		- Distributed control system (DCS)

		  Usually process control or discrete part control systems.

		- Programmable logic controller (PLC)

		  Provide local management of processes through feedback control.

		- Remote terminal unit (RTU)
		- Human machine interface (HMI)
		- Intelligent electronic device (IED)
		- Sensor
		- Actuator

	- ICS x IT

		- Performance
		- Availability
		- Risks
		- Communications
		- Change management
		- Lifetime

	- ICS security program

### Distributed Computing

Any system with multiple computing nodes.

- Client-server

  Special case of a distributed system with only two tiers.

- Grid computing
- Parallel data systems
- P2P

### Common Vulnerabilities & Threats

- Hackers

	- Hats

		- Black

			- Cracker

		- White

	- Hacktivist
	- Script kid
	- APT

- Outsiders
- Insiders
- Phisher
- Botnets

	- Bot

		- Zombie

- Side-channels

  Nonintrusive and are used to uncover sensitive information about how a component works, without trying to compromise any type of flaw or weakness.

	- Timing information
	- Power consumption
	- Electromagnetic leaks
	- Sound

- Covert channels

  Way for an entity to receive information in an unauthorized manner.

	- Storage

	  Processes are able to communicate through some type of storage space on the system.

	- Timming

	  One process relays information to another by modulating its use of system resources.

- Backdoors

	- Maintenance hook

- Zero-days

  Vulnerability that is known before the existence of a patch.

	- Zero-day exploit

	  Refers to the existence of exploit code for a vulnerability that has yet to be patched.

- Malware

	- Viruses

		- Macro
		- Boot sector
		- Stealth
		- Polymorphic
		- Multipartite

	- Worms
	- Trojans

		- Remote access tool (RAT)

	- Logic bombs

- Rootkits

  Malware that replaces portions of the kernel and/or operating system.

- Buffer overflows
- Single point of failure
- Race conditions

	- TOCTOU

- Databases

	- Aggregation

	  User does not have clearance or permission to access specific information, but does have permission to access components of that information, allowing her to figure out the rest and obtain restricted information --includes combining information from several sources, so the combined information has greater sensitivity than its parts.

	- Inference

	  The intended result of aggregation, when the subject can DEDUCE the full story through its parts.

- Web

	- XSS

	  Target: client

		- Persistent

		  Targeted at websites that allow users to input data that is stored in a database or similar location, such as a forum or message board.

		- Nonpersistent/Reflected

		  Occurs when an attacker tricks the victim into opening a URL programmed with a rogue script to steal the victim’s sensitive information, such as a cookie or session ID.

		- DOM

		  Attacker uses the Document Object Model (DOM) environment to modify the original client-side JavaScript causing the victim's browser to execute the resulting abusive JavaScript code.

	- XSRF

	  Target: server

		- 1. Attacker forges a request do to something malicious, such as transferring funds
		- 2. Attacker sends the request to a victim who could be logged on a website
		- 3. Victim clicks on that link, therefore sending the request to the website
		- 4. Website receives and processes the request, thus the attacker achieves her goal

	- SQLi

### Web Architecture

- Applets

  Server sends code and it is executed on the client.

	- Java

		- Sandboxes

	- ActiveX

		- Digital certificates

- OWASP

	- Top-10
	- API security
	- ZAP

### Service-oriented Architecture (SOA)

- XML

	- SOAP
	- WSDL

- JSON

	- REST

### Databases

- Data protection

	- Polyinstantiation

	  Database security technique that appears to permit the insertion of multiple rows sharing the same uniquely identifying information.

	- Cell suppression

	  Hides a cell for some users, depending on their clearances and the data classification.

	- Views

	  A selection of certain information from a database containing only the data a user can have access to.

- Big data

	- Data warehousing
	- Data mining

### Cryptology

- Steganography

  Method of hiding data in another media type so that the very existence of the data is concealed, a type of security through obscurity.

	- Hidden data, not cryptography
	- Components

		- Carrier

		  Signal, data stream, or file that has hidden information inside of it.

		- Stegomedium

		  Medium in which the information is hidden in steganography, such as JPEG or TIFF, or a Word document.

		- Payload

		  The actual information that the sender wants to keep secret.

- Cryptanalysis

	- Ciphertext only

	  Attacker has the ciphertext of several messages, and tries to find the key; easy to obtain the ciphertext (sniffing), but hard to figure out the key.

	- Known plaintext

	  Attacker has the plaintext and the ciphertext of several messages and tries to find the key.

	- Chosen plaintext

	  Attacker has the plain and ciphertexts, but can choose the plaintext, this way she can figure out the way the cipher works and find the key.

		- Adaptive chosen-plaintext

	- Chosen ciphertext

	  Attacker can choose the ciphertext to be decrypted and has access to the resulting plaintext --attacker must have control over the system. Usually launched against asymmetric algorithms.

		- Adaptive chosen-ciphertext

	- Differential

	  Attacker uses different ciphertexts and different plaintext (specific differences) and analyses the results, trying to figure out the key, similar to adaptive chosen plaintext attacks.

	- Linear

	  Attacker carries a known plaintext attack on several different messages encrypted with the same key, then he evaluates the probability of inputs ending up in a specific combination.

	- Side-channel

	  Use physical data to break a cryptosystem, such as monitoring CPU cycles or power consumption used while encrypting or decrypting.

	- Meet-in-the-middle

	  Attacker encrypts from one end and decrypts from the other end (meeting in the middle) --the primary reason why 2DES is not used.

	- Man-in-the-middle
	- Replay

	  Attacker captures some type of data and resubmits --countermeasures: timestamps and sequence numbers.

	- Birthday

	  Tries to force a collision in an hashing algorithm, based on birthday paradox, it takes 2**n/2 to find a collision in a 2**n-bit message digest.

	- Social engineering

	  Typically uses persuasion, coercion, or bribery.

	- Brute-force

- Cryptography

  Generally, all algorithms have a lifespan, keys should be changed periodically, and the more bits the key has, the more secure the system is.
  
  Confidentiality
  Authentication
  Integrity
  Nonrepudiation
  
  C = E(P, K)
  P = D(C, K)

	- Goals

		- Confidentiality
		- Integrity
		- Authenticity
		- Nonrepudiation

	- Techniques

		- Substitution

		  Uses a key to dictate how the substitution should be carried out.

			- Confusion

			  Attacker can't find a relationship between the key and the ciphertext.

		- Transposition

		  Values are scrambled, or put in a different order, where the key determines the positions the values are moved to.

			- Difusion

			  A single plaintext bit has influence over several of the ciphertext bits.

		- Monoalphabetic
		- Polyalfabetic

		  Example: Vigenère cipher

		- XOR

		  Equal = 0, different = 1.

		- Nonce

		  Number to be used once

		- Initialization vector (IV)
		- Padding

		  Process of adding material to plaintext data before it is encrypted.

	- Cryptographic strength

		- Work factor

	- Public key infrastructure (PKI)

		- Digital certificates

			- X.509

				- Version
				- Serial number
				- Signature algorithm
				- Issuer name
				- Validity period
				- Subject's name (DN)
				- Subject's public key
				- V3 support extensions

		- Certificate authority (CA)

			- Intermediate/Issuing CA
			- Registration authority (RA)

			  Establishes and confirms the identity of the individual requesting the certificate, initiates the certification process with a CA on behalf of an end user, and can perform certificate lifecycle management functions. Does not sign certificates.

			- Cross certification

			  Process of two CAs to establish a trust relationship.

		- Certificate revocation list (CRL)

		  Plain text with serial numbers of revoked certificates, so does not scale well.

		- Online certificate status protocol (OSCP)

		  Replacement for CRLs and uses client-server design that scales better.
		  User sends the serial number to the OSCP server
		  OSCP server typically returns "good", "revoked", or "unknown".

	- Digital Signatures

		- Hashing+Encryption
		- Nonrepudiation

	- Key management

		- Key storage

		  The organization that issued the public/private key pairs retains a copy.

		- Key escrow

		  A copy is retained by a third-party organization (and sometimes multiple organizations), often for law enforcement purposes.

		- Retired key

		  May no longer be used, but is able to decrypt former messages.

		- Destroyed key

		  No longer exists therefore cannot be used anymore.

		- Escrowed encryption

		  Private key is often divided into two or more parts, each held in escrow by different trusted third-party organizations, which will only release their portion of the key with proper authorization, such as a court order.

	- Asymmetric

		- Methods

			- Discrete logarithm

				- Diffie-Hellman
				- ElGamal

					- Doubles the length of the message
					- Public domain

			- Factoring prime numbers

				- RSA

					- n is the product of 2 large prime numbers (p*q)
					- e (public key) is a random integer 1 < e < (p-1)*(q-1)
					- d (private key) d * e - 1 is multiple of (p-1)*(q-1)
					- C = p ** e mod n
					- P = c ** d mod n

			- Elliptic curve (ECC)

		- Zero knowledge proof

		  Means that someone can tell you something without telling you more information than you need to know. In cryptography, it means proving that you have a specific key without sharing that key or showing it to anyone.

		- Usage

			- Encrypt with public key
			- Decrypt with private key
			- Digitally sign with private key
			- Verify signature with public key

		- Characteristics

			- 2 keys: public and private
			- n * 2 keys required
			- n key pairs required

				- Scalable

			- Slow

	- Symmetric

		- Block

			- Modes

				- ECB

				  Fastest and easiest to implement, used to encrypt small pieces of data. No IV or chaining, and does not propagate errors.

				- CBC

				  Commonly used to encrypt large chunks of data, so it's not mandatory to use different IVs for EACH message. Does chaining, therefore propagates errors.

				- CFB

				  Can be used to encrypt streams, like sending one character at a time to a server. Block sizes vary, starting from 1 bit. It's imperative to use different IVs for different messages, since each message tends to be small. It is basically CBC in stream mode --feedback is chaining for stream mode. Obviously propagates errors.

				- OFB

				  Similar to CFB, but has no chaining --useful for sending digital audio or video. Does not propagate errors.

				- CTR

				  Similar to OFB, but uses a counter, instead of an IV. Does not propagate errors.

			- Algorithms

				- DES

					- DEA

						- Lucifer (IBM)

					- 64-bit keys

						- 56-bit effectively

				- 3DES

					- 168-bit keys (3TDEA)

					  All three keys are different and independent from each other.

					- 112-bit (2TDEA)

					  Two of the three keys are equal.

					- 56-bit (backward compatible to DES)

					  All keys are equal.

				- AES

					- Rjindael
					- Keys and blocks

						- 128-bit
						- 192-bit
						- 256-bit

				- Twofish

					- 128-256 bits

				- Blowfish

					- 32-448 bits

				- IDEA

				  International Data Encryption Algorithm

					- 128-bit keys
					- 64-bit block
					- PGP

					  PGP can encrypt emails, documents, or an entire disk drive. PGP uses a web of trust model to authenticate digital certificates, instead of relying on a central CA.

				- RC5

					- Up to 2048-bit keys
					- Blocks

						- 32-bit
						- 64-bit
						- 128-bit

				- RC6

				  Block cipher built upon RC5, in order to become AES.

		- Stream

		  Stream ciphers require a lot of randomness, which requires a lot of processing power. Because it is hard to generate truly random and unbiased keystream, stream ciphers are considered less secure than block ciphers.

			- RC4

			  Used in SSL, 802.11 protocol (improperly), a.k.a., ARC4 (code was leaked), vulnerable to modification attacks, WPA used it, but then moved to AES in WPA2.

		- One-time pad (OTP)

		  A.K.A. Vernam cipher

			- Unbreakable
			- Pretty hard to implement
			- Requirements

				- Key must be truly random
				- Key must have the same length as the message
				- Keys must not be repeated

		- Characteristics

			- Same key to encrypt and decrypt
			- Key must be distributed out-of-band
			- (n * (n - 1)) / 2 keys needed

				- Nonscalable

			- Fast

	- Hashing

		- MD5 (128 bits)
		- SHA

			- SHA-1 (160 bits)
			- SHA-2

				- 256 bits
				- 384 bits
				- 512 bits

			- SHA-3

		- Requisites

			- Variable-length input
			- Fixed-length output
			- Easy to compute
			- Computationally impossible to reverse (one-way)
			- Collision-free

	- Kerckhoff's principle

### Perimeter Security

Safe of people is ALWAYS the most important

- Mechanisms

	- Fences

	  Depending on the height, could be deterrent or preventative. The tallest the fence, the more probability to be deterrent.

	- Walls
	- Bollards
	- Gates

	  Should be minimized.

		- Locks

		  Preventive

			- Key

				- Pin tumbler lock
				- Warded lock

			- Combination
			- Cards

				- Smartcards

				  Microchip

					- Contact
					- Contactless

						- RFID

				- Magnetic stripe

				  “Smart” means the card contains a computer circuit.

			- Mantraps
			- Turnstiles

	- Barriers

	  Helps minimizing or deterring attacks.

	- Lights

	  Deterrent or detective access control.

	- CCTV

	  Detective access control.

		- Apperture

			- Depth of field

			  The smaller the aperture, the larger the depth of field.

		- Field of view
		- Infrared

	- Emanations

		- TEMPEST
		- Faraday cage

	- Alarms

		- Ultrasonic
		- Microwave
		- Infrared
		- Photoelectric

	- Guards

		- Self
		- Contract

	- Dogs

	  The primary drawback to using dogs as a perimeter control is the legal liability.

	- Asset tracking

	  Show the exact equipment and data that the employee must return to the company and helps in case of theft.

- Site selection

	- Utility reliability

	  Related to the quality of energy delivered to the site. Is it possible to have more than one energy service? Is the utility reliable?

	- Crime rates
	- Site marking
	- Shared tenancy / Adjacent buildings

		- Shared demarc

	- CPTED

		- Access control
		- Surveillance
		- Territorial reinforcement

- Environmental

	- Power

		- Equipments

			- UPS
			- Generator

		- Issues

			- Power excess

				- Spike
				- Surge

			- Power loss

				- Fault
				- Blackout

			- Power degradation

				- Sag/Dip
				- Brownout
				- In-rush current

			- EMI

	- HVAC

		- Temperature

		  Data center: 20-25C (68-77F)

		- Humidity

		  Data center: 40-55%

			- Static
			- Corrosion

		- Air quality
		- Positive pressure

	- Fire

		- Detection

			- Flame

			  Usually requires line of sight to detect the flame.

			- Smoke

				- Ionization
				- Photoelectric

			- Heat

		- Roles

			- Safety warden

			  Ensures that all personnel safely evacuate the building in the event of an emergency or drill.

			- Meeting point leader

			  Assures that all personnel are accounted for at the emergency meeting point.

		- Classes

			- A. Common combustibles

			  Examples: wood, paper.
			  Suppression: water, soda acid.

			- B. Liquid

			  Examples: burning alcohol, oil, petroleum products.
			  Suppression: gas, soda acid.

			- C. Electrical

			  Examples: electrical equipment, wiring.
			  Suppression: gas.

			- D. Combustible metals

			  Examples: metals.
			  Suppression: dry powder.

			- K. Kitchen

			  Examples: burning oil, grease.
			  Suppression: wet chemicals.

		- Suppression

		  Objectives of any suppression element:
		  reducing the temperature of the fire
		  reducing the supply of oxygen
		  reducing the supply of fuel, and
		  interfering with the chemical reaction within fire.

			- Water

				- Wet

				  Have water right up to the sprinkler heads.

				- Dry

				  As the dry pipe sprinkler heads open, the air pressure drops in each pipe, allowing the valve to open and send water to that head.

				- Deluge

				  Similar to dry pipes, except the sprinkler heads are open and larger than dry pipe heads. The pipes are empty at normal air pressure; a deluge valve holds the water back. The valve opens when a fire alarm triggers.

				- Preaction

				  Combination of wet, dry, or deluge systems and require two separate triggers to release water.

			- Soda acid
			- Dry powder
			- Wet chemicals
			- Gas

				- Carbon dioxide (CO2)

				  Only recommended for use in unstaffed areas.

				- Halon

				  Currently being phased out in favor of replacements with similar properties.

				- Argon
				- FE-13
				- FM-200
				- Inergen

### Security Models

Maps abstract goals of the policy, specifying data structures and techniques necessary to enforce security policies.

Security models take the requirements and provide the necessary mathematical formulas, relationships, and logic structure to accomplish this goal.

From there, specifications are developed per OS type, and individual vendors can decide how they are going to implement mechanisms to meet these specifications.

- Bell-LaPadula

  Confidentiality model
  Simple security property: no read-up
  *-security property: no write-down
  Strong tranquility property: security labels will not change while the system is operating
  Weak tranquility property: security labels will not change in a way that conflicts with defined security properties.

	- Confidentiality

- Biba

  Integrity model
  Simple integrity property: no read-down
  *-integrity property: no-write up

	- Integrity

- Lipner

  Integrity model
  Based on  Bell-LaPadula and Biba 
  Assign security levels and functional categories to subjects and objects

	- BLP+Biba

- Clark-Wilson

  Focused on integrity.
  Principles: well-formed transactions and separation of duties
  Triple: Subject --> Interface (program) --> Object

	- Well-formed transactions

- Brewer-Nash

  Chinese wall
  Avoids conflicts of interest
  Permits controls to change dynamically based on previous actions

	- Conflicts of interest
	- Chinese wall

- Graham-Denning

  Addresses how access rights between subjects and objects are defined, developed, and integrated.
  Eight primitives: create/delete objects/subjects, provide read/grant/delete/transfer access rights.

	- 8 primitives

- Harrison-Ruzzo-Ullman

  Extends Graham-Denning 
  Operates on access matrices
  Tackles the problem of how to deal with the creation and deletion of files
  Deals with access rights of subjects and the integrity of those rights

	- Access matrices

- Take-Grant

  Employs a directed graph
  Operations: take, grant, create, remove

	- Graph

- Noninterference

  Goghen-Meseguer
  Avoids covert channels between different clearances.
  Any actions that take place at a higher security level do not affect or interfere with actions that take place at a lower level.

	- Covert channels

### TCB

Collection of all hardware, firmware, and software components within a system that provides some kind of security and enforces the system's security policy; mechanisms that enforce the security policy.

- Primary components

	- Hardware
	- Software

		- Reference monitor

	- Security perimeter

	  Imaginary boundary that separates the TCB from the rest of the system.

### Design Concepts

- Security domains

  Groups of subjects and objects with similar security requirements. Confidential, Secret, and Top Secret are three security domains used by the US DoD, for example.

- Layering

  Separates hardware and software into modular tiers.

	- 1. Hardware
	- 2. Kernel and device drivers
	- 3. Operating system
	- 4. Applications

- Ring model

  Form of CPU hardware layering.

	- 0. Kernel

	  In practice OSes run entirely in the layer.

	- 1. Operating system

	  A new mode called hypervisor mode (and informally called “Ring-1”) allows virtual guests to operate in Ring 0, controlled by the hypervisor one ring “below.” The Intel Virtualization Technology (Intel VT, aka “Vanderpool”), and AMD-Virtualization (AMD-V, aka “Pacifica”) CPUs support a hypervisor.

	- 2. Device drivers

	  In practice this layer is not used.

	- 3. User applications
	- Abstraction

	  Hides unnecessary details from the user.

		- System calls (syscalls)

		  Processes communicate between the rings via system calls.

### Systems Security

- NIST SP 800-160

  Systems Security Engineering
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-160v1.pdf

	- Acquisition
	- Supply
	- Organizational

		- Infrastructure
		- Human resources

	- Technical management

		- Risk management
		- Configuration management

	- Technical

		- System requirements
		- Architecture definition
		- Design definition
		- Implementation
		- Integration
		- Verification
		- Transition
		- Validation
		- Operation
		- Maintenance
		- Disposal

- Kernel

	- Reference monitor

	  Abstract machine that mediates all access subjects have to objects to provide security.

		- Subject
		- Mediation

			- Rules
			- Logging & monitoring

		- Object

### Secure Hardware Architecture

- System unit

  Computer's case

- Bus

  Primary communication channel on a computer system.

- Memory

	- Virtual memory

		- Paging

		  Copies fixed-length blocks of memory to and from disk.

		- Swapping

		  Copies the entire process to and from disk.

	- Process isolation

	  OS provide separate memory spaces for each process' instructions and data.

		- Hardware segmentation

		  Enforces isolation through the use of physical hardware controls.

	- Data execution prevention (DEP)

	  Can be enabled within hardware and/or software, attempts to prevent code execution in memory locations that are not predefined to contain executable content.

	- Address space layout randomization (ASLR)

- CPU

	- Control unit

	  Sends instructions to the ALU.

	- ALU

	  Performs mathematical calculations.

	- Interruption

	  Indicates that an asynchronous event has occurred.

	- FDX

	  All steps take 1 clock cycle to complete.

		- Fetch
		- Decode
		- Execute
		- Write

	- Pipelining

	  Combines multiple CPU steps into one process, allowing simultaneous FDX.

		- Process states

			- 1. New

			  Goes to Ready when loaded.

			- 2. Ready

			  Goes to Running when scheduled.

			- 3. Running

			  Goes to Ready when context is switched.
			  Goes to Blocked when at wait.
			  Goes to Done when terminated.

			- 4. Blocked

			  Goes to Running when wakes up.

			- 5. Done

	- Execution types

		- Multiprogramming

		  Old; mainframe; implemented by specific program.

		- Multitasking

		  New; PC; implemented by OS; multiple processes, single threads.

		- Multiprocessing

			- Symmetric (SMP)

			  Single computer with multiple CPUs, sharing OS, memory, and data bus.

			- Asymmetric (AMP)

		- Multithreading

		  Single process, multiple threads.

	- Special registers

		- Program Counter

		  Address of the next instruction to run.

		- Stack Pointer (SP)

		  Address of the last program request in a stack.

		- Program Status Word (PSW)

		  Indicates if CPU is running in user (a.k.a., problem state) mode, or in privileged (a.k.a., kernel or supervisor) mode. This is the ring information itself.

- BIOS/UEFI
- TPM

  Protected and encapsulated microcontroller security chip that provides a safe haven for storing and processing security-intensive data such as keys, passwords, and digital certificates.

	- Binding

	  The content of a given hard disk drive is affixed with a particular computing system.

	- Sealing

	  A system is "sealed" to a particular hardware and software configuration.

## D4. Communication and Network Security

### Models

- ISO/OSI

	- L1. Physical

		- PDU: Bits

	- L2. Data link

		- PDU: Frames
		- MAC layer

		  Specifies the interface with the protocol requirements of the physical layer.

			- IEEE 802.3

		- LLC layer

		  Communicates with the network layer.

			- IEEE 802.2

	- L3. Network

		- PDU: Packets

	- L4. Transport

		- PDU: Datagrams/Segments

	- L5. Session

	  Establishes a connection between two applications, maintaining it during the transfer of data, and controlling the release of this connection. Three modes: simplex, half-duplex, full-duplex.

		- Dialog management

			- 1. Connection establishment
			- 2. Data transfer
			- 3. Connection release

	- L6. Presentation

	  Provides a common means of representing data in a structure that can be properly processed by the end system --also handles data compression and encryption issues. No protocols work at this layer, only services.

	- L7. Application

		- PDU: Message

- TCP/IP

	- L1. Network access

		- OSI: L1, L2

	- L2. Internet

		- OSI: L3

	- L3. Transport/Host-to-host

		- OSI: L4

	- L4. Application

		- OSI: L5, L6, L7

- Multilayer
- Encapsulation

  Message created by a program is passed DOWN to the network protocol's stack.

- Protocols

	- Point-to-Point Protocol (PPP)

	  Operates at Data Link layer and can transmit multiple protocols.

		- Serial Line Internet Protocol (SLIP)

		  Similar to PPP, but has lower overhead and works only with IP.

	- IEEE 802.3 (Ethernet)

		- CSMA/CD

		  Devices transmit data and if they don't receive response, send a jam signal valid for the collision domain, then all devices wait for a random short period of time to start communicating again.

		- MAC

		  First 3 bytes designates the vendor.

			- EUI-48 (48 bits)
			- EUI-64 (64 bits)

	- ARP

	  Resolves IP to MAC addresses.

		- Reverse ARP (RARP)

		  MAC to IP

	- Authentication

		- Password Authentication Protocol (PAP)

		  Used by remote users to authenticate over PPP connections, providing identification and authentication. Passwords are sent in cleartext, which makes PAP the most insecure method. Vulnerable to sniffing and MitM attacks.

		- Challenge Handshake Authentication Protocol (CHAP)

		  Uses a challenge/response mechanism to authenticate the user, which addresses the main flaw in PAP.
		  
		  User sends a logon request, server sends a challenge (nonce), user encrypts the challenge with an predefined password and sends it, server decrypts and compares the result.
		  
		  Since the handshake is repeated multiple times during the connection, CHAP is NOT vulnerable to MitM attacks.

			- MS-CHAP

			  Provides mutual authentication, and has two versions (MS-CHAPv1 and MS-CHAPv2) incompatible with each other.

		- Extensible Authentication Protocol (EAP)

		  Provides a framework to enable many types of authentication techniques to be used when establishing network connections --it extends the norm (PAP, CHAP) to other methods, such as OTPs, token cards, biometrics, Kerberos, digital certificates, and future mechanisms. EAP works with a variety of technologies, including PPP, PPTP, L2TP, IEEE 802 wired and wireless.

			- LEAP

				- Password-based
				- Cisco
				- Insecure

			- EAP-TLS

				- Digital certificates

			- EAP-TTLS

				- Similar to EAP-TLS, but no certificate for clients

			- PEAP

			  Developed by Cisco Systems, Microsoft, and RSA Security, is similar to and is a competitor of EAP-TTLS, as they both do not require client-side certificates.

				- Requires certificate only for the server
				- PEAPv0/MS-CHAPv2

				  Digital certificate for server only.

				- PEAPv1/EAP-GTC

			- ...

	- IEEE 802.1AE (MACSec)

	  MAC Security standard (MACSec), provides confidentiality, integrity, and authentication, protecting hop-by-hop protection at layer 2, just like a VPN at layer 3.

		- Protection hop-by-hop at L2

	- IEEE 802.1AR (DevID)

	  Defines globally unique per-device secure identifier (DevID) to allow establishment of the trustworthiness of devices --802.1AR can be used along with EAP-TLS.

		- Unique per-device identifiers

	- IEEE 802.1AF

	  Carries out key agreement functions for the session keys used for data encryption.

		- Key agreement functions

	- IEEE 802.1X

	  Before start communicating, a new device used 802.1X to authenticate to the network (using is the digital certificate and identification data of that device --802.1AR), which is processed by EAP-TLS. A RADIUS server usually authenticates the device, then keying material is installed, then data encryption and frame integrity checking takes place (802.1AE) as traffic goes from one network device to another.

		- Authentication

			- EAP

		- Network Access Control (NAC)

			- Preadmission

			  System must meet all requirements, such as patch application and antivirus updates before it is allowed to communicate with the network.

			- Postadmission

			  Allows and denies access based on user activity, which is based on a predefined authorization matrix.

		- Entities

			- Supplicant

				- Wireless device

			- Authenticator

				- Wireless Access Point (WAP)

			- Authenticator server

				- RADIUS server

	- Mobile

		- 1G. FDMA
		- 2G. TDMA
		- 3G. CDMA
		- 4G. OFDMA

	- Frame relay

	  Packet-switched layer 2 WAN protocol that provides no error recovery and focuses on speed. Replaced the old X.25 packet-switched WAN technology.

		- PVC

		  Virtual circuit analogous to a T1 line.

		- SVC

	- MPLS

	  Forwards WAN data using labels via a shared MPLS cloud network.

	- IP

		- IPv4

			- 32 bits
			- RFC 1918

				- Private addresses

					- 10/8
					- 172.16/12
					- 192.168/16

		- NAT

			- Static

			  NAT has a pool of public addresses, and each private address is mapped to a specific public address.

			- Dynamic

			  NAT software has a pool of public addresses, leasing works on a first-come, first-served basis.

			- PAT

			  Company owns and uses only one public IP address for all systems.

		- IPv6

			- 128 bits
			- ::1/128

				- Localhost

			- FE80::/64

				- Autoconfigure

			- Tunneling

				- 6to4
				- Teredo
				- ISATAP

		- Connectionless
		- Unreliable
		- Best effort
		- CIDR

	- Internet Control Message Protocol (ICMP)

		- 0: echo reply
		- 3: destination unreachable
		- 5: redirect
		- 8: echo request
		- 9: router advertisement
		- 10: router solicitation
		- 11: time exceeded

	- TCP/UDP

		- TCP connection: 3-way handshake

			- 1. SYN
			- 2. SYN/ACK
			- 3. ACK

		- TCP disconnection: 4-way handshake

			- 1. FIN/ACK
			- 2. ACK
			- 3. FIN/ACK
			- 4. ACK

		- TCP forced disconnection

			- RST

		- UDP: connectionless
		- Ports

			- Well-known (0-1023)

				- 20-21. FTP

					- 20. Data
					- 21. Commands

				- 22. SSH/SFTP/SCP
				- 25. SMTP

					- MIME

					  Provides a standard way to format email, including characters, sets, and attachments.

						- S/MIME

						  Leverages PKI to encrypt and authenticate MIME-encoded email.

				- 23. Telnet
				- 49. TACACS
				- 53. DNS
				- 67-68. DHCP
				- 80. HTTP

					- SHTTP

					  Encrypts packets at the application layer of the OSI model, encrypting only HTTP data, therefore is seen as an HTTP packet and can be sent over port 80.

				- 88. Kerberos
				- 101. POP3
				- 143. IMAP
				- 161-162. SNMP

					- 161. GET
					- 162. TRAP

				- 389. LDAP
				- 443. HTTPS

					- TLS

						- SSL

				- 500. IKE
				- 515. LDP
				- 636. LDAPS
				- 993. IMAPS
				- 995. POP3S

			- Registered (1024-49151)

				- 1701. L2TP
				- 1812-1813. RADIUS

					- 1812. Authentication
					- 1813. Accounting

				- 3389. RDP
				- 5900. VNC

			- Dynamic (49152-65535)

	- DNP3

	  Provides an open standard used primarily within the energy sector for interoperability between various vendors of SCADA and smart grid applications.

		- Multilayer protocol

	- Storage

		- Fibre channel
		- FCoE

		  Uses Ethernet directly to connect storages, not TCP or IP.

		- iSCSI

		  Similar to FCoE, but uses higher layers of the TCP/IP model.

	- VoIP

		- SIP

		  Only used for signaling.

			- Handshake

				- 1. Invite
				- 2. Trying
				- 3. Ringing

		- H.323

		  Similar to SIP.

		- RTP

		  Carries the voice stream.

			- SRTP

	- OpenFlow

	  SDN TCP protocol that uses TLS.

	- Routing

		- Link state

		  Maintain a topography map of all connected networks and use this map to determine the shortest path to the destination. Typically converge faster than distance vector protocols.

			- OSPF
			- IS-IS

		- Distance vector

		  Maintain a list of destination networks along with metrics of direction and distance as measured in hops.

			- RIP
			- IGRP
			- EIGRP

	- Converged protocols

	  Merging of specialty or proprietary protocols with standard protocols, such as those from the TCP/IP suite.

		- FCoE
		- iSCSI
		- MPLS
		- VoIP
		- SDN

### Network Concepts

- Communication types

	- Simplex
	- Half-duplex
	- Full-duplex

- Network Types

	- PAN
	- LAN
	- MAN
	- WAN

		- Dedicated links

			- T lines

			  Used in US, Japan, South Korea, and Canada.

				- T1

					- 1.544 Mbps

				- T3

					- 44736 Mbps

			- E lines

			  Used in the rest of the world.

				- E1

					- 2048 Mbps

				- E3

					- 34368 Mbps

		- Nondedicated links

			- DSL

				- ADSL

				  Download speed > upload speed

				- SDSL

				  Download speed == upload speed

				- HDSL
				- VDSL

	- SAN

- Network segments

	- Intranet

	  Private network.

	- Extranet

	  Provides access to reserved partners. Cross between intranet and internet.

	- Demilitarized zone (DMZ)

	  Extranet for public consumption.

	- Internet

	  Public network.

- Network topologies

	- Ring

		- Passing token

	- Bus
	- Star
	- Mesh

- Switching

	- Circuit

	  Circuit or channel (i.e., a portion of a circuit) was dedicated between two nodes, like a T1 line.

	- Cell

	  Similar to packet-switched, but uses fixed-length cells instead of variable-length packets, ex.: ATM.

	- Packet

	  Break data into packets, each sent individually.

		- QoS

	- Message

	  Predecessors of packet switching, but here an entire message is routed from hop to hop until destination, ex.: Telex and Unix-to-Unix copy (UUCP).

### Media Types

- Metallic cables

  Information is coded in voltage levels.

- Optical fibers

  Information is coded in wavelength (color), phase, or polarization of the light.

- Free space

  Radio signals, light, infrared laser beams.

### Cabling

- Coaxial
- Twisted-pair

	- Shielded
	- Unshielded
	- Categories

		- Cat1

			- 1 Mbps

		- Cat 2

			- 4 Mbps

		- Cat3

			- 10 Mbps

		- Cat4

			- 16 Mbps

		- Cat5

			- 100 Mbps

		- Cat6

			- 1 Gbps

		- Cat7

			- 10 Gbps

- Fiber-optic

	- Modes

		- Single
		- Multi

- Problems

	- Noise
	- Attenuation
	- Crosstalk
	- Fire

### Wireless

- Architecture

	- Infrastructure WLAN

	  WAPs connect wireless and wired networks.

	- Stand-alone

	  Only one WAP, not connected to a wired network.

	- Ad-hoc

	  No WAPs, wireless devices connect directly through NICs.

- CSMA/CA

  Devices listen to inbound interface and only send data in outbound interface if it's clear.

	- CSMA

	  Devices tries to communicate and if don't receive ACK, retransmit.

- Techniques

	- Spread spectrum

		- Direct-sequence spread spectrum (DSSS)

		  Uses the entire band at once, "spreading" the signal throughout the band.

		- Frequency-hopping spread spectrum (FHSS)

		  Uses a number of small frequency channels throughout the band and "hops" through them in pseudorandom order.

	- Orthogonal frequency-division multiplexing (OFDM)

	  Allows simultaneous transmissions to use multiple independent wireless frequencies that do not interfere with each other.

- Security

	- WEP

		- Problems

			- Static encryption keys
			- Ineffective use of IVs

			  Uses a weak 24-bit IV, sent in clear text.

			- Lack of packet integrity assurance

		- RC4
		- Insecure

	- Wi-Fi Protected Access (WPA)

		- TKIP
		- RC4

	- WPA2 (IEEE 802.11i)

		- AES

			- Encryption

		- CCMP

			- Integrity

	- Wi-Fi Protected Setup (WPS)

		- Insecure
		- Should never be used

- IEEE standards

	- IEEE 802.11a

		- 5 GHz
		- OFDM
		- 54 Mbps

	- IEEE 802.11b

		- 2.4 GHz
		- DSSS
		- 11 Mbps

	- IEEE 802.11g

		- 2.4 GHz
		- OFDM
		- 54 Mbps

	- IEEE 802.11n

		- 5 or 2.4 GHz
		- OFDM
		- 100 Mbps

	- IEEE 802.11ac

		- 5 GHz
		- OFDM
		- 1.3 Gbps

	- IEEE 802.15 (WPAN)

		- IEEE 802.15.1 (Bluetooth)

			- 2.4 GHz
			- 1-3 Mbps

		- IEEE 802.15.4 (ZigBee)

	- IEEE 802.16 (WiMAX)

- RFID

	- Active
	- Semipassive
	- Passive

### Components

- Endpoint

  Endpoints are everything except the network communication devices, including desktops, servers, mobile devices, and other embedded systems.

- Private Branch Exchange (PBX)
- Modem

	- Cable modem

- Repeater

	- Hub

- Bridge
- Switch

	- L2
	- L3
	- L4
	- Collision domains
	- VLANs
	- Trunks

- Router

	- Broadcast domains

- Gateway

  Makes conversions between protocols.

- Bastion host

  Highly exposed device connected to an untrusted network, such as a firewall, mail/web/DNS server.

- Firewall

	- Types

		- Packet-filtering

		  Network layer. Makes simple filtering decisions based on each individual packet.

			- Stateless

		- Stateful

		  Network layer. Makes filtering decisions based on previous packets that have been sent. A.K.A, dynamic packet filtering firewalls.

			- Dynamic packet filtering

		- Proxy

			- Circuit-level

			  Session layer. E.g., SOCKS.

			- Application-level

			  Application layer. Terminates the connection with the source device and initiates a new connection with the destination device, thereby hiding the source of the traffic.

		- Deep packet inspection

		  Has filtering mechanism that operates typically at the application layer in order to filter the payload contents of a communication rather than only on the header values. DPI can also be known as complete packet inspection and information extraction (IX). DPI filtering is able to block domain names, malware, spam, or other identifiable elements in the payload of a communication.

		- Kernel proxy

		  Application layer. 5th generation, creates dynamic, customized network stacks when a packet needs to be evaluated, allowing evaluation in all layers for each connection.

		- Next-generation

		  Multiple layers. Incorporates a signature-based IPS engine, connects to external data sources (such as MS-AD).

	- Architecture

		- Multihomed

		  Device that has 2 or more interfaces each of which connected to different networks.

		- Screened host

		  A.K.A., single-tiered configuration. Firewall that communicates directly with a perimeter router and the internal network: internet --> router --> external firewall --> LAN.

		- Screened subnet

		  A.K.A., two-tiered configuration. External firewall screens the traffic entering the DMZ and sends it to another firewall, thus creating a DMZ between the two firewalls: internet --> router --> external firewall --> internal firewall --> LAN.

	- Rules

		- Silent

		  Drops "noisy" traffic without logging.

		- Stealth

		  Disallows access from unauthorized systems.

		- Negate

		  Provides tighter permission rights.

		- Cleanup

		  Drops and logs any traffic.

- Unified Threat Management (UTM)

  Provides all (or many) security functionalities (like firewall, proxy, antivirus, IPS, DLP) in a single network appliance.

- IDPS

  Anomaly
  Protocol
  Pattern/Signature

	- Network-based

		- NIDS

		  Sniffs the internal interface of the firewall in read-only mode and sends alerts to a NIDS Management server via a different (ie, read/write) network interface.

		- NIPS

		  Alters the flow of network traffic.

			- Active response

			  Like the NIDS. The difference is that the monitoring interface is read/write

			- Inline

	- Host-based

		- HIDS
		- HIPS

	- Events

		- True positive (goal)
		- True negative (goal)
		- False positive (issue)
		- False negative (issue, worst case scenario)

	- Detection types

		- Knowledge/Signature-based
		- Behavior-based (statistical intrusion detection)

- SIEM

	- NIST SP 800-92

		- Infrastructure

			- Time synchronizing
			- Log security
			- Normalization

		- Planning

			- Roles & responsibilities
			- Log policy
			- Log retention
			- Log disposal

		- Operation

			- Clipping level/Threshold
			- Sampling
			- Log rotation
			- Correlating events

	- Common log types

		- Security

		  Access to resources such as files, folders, printers, and so on.

		- System

		  System events such as when a system starts or stops, or when services start or stop.

		- Application

		  Information for specific applications.

		- Firewall

		  Events related to any traffic that reaches a firewall.

		- Proxy

		  Include the ability to record details such as what sites specific users visit and how much time they spend on these sites.

		- Change

		  Change requests, approvals, and actual changes to a system as a part of an overall change management process.

- Data loss prevention (DLP)

  A first critical step is to conduct an inventory of all the data in your organization in order to characterize and prioritize its sensitivity.

	- Host-based
	- Network-based

- Content Distribution Network (CDN)

  Multiple servers distributed across a large region, each of which provides content that is optimized for users close to it --improves the resilience against DDoS attacks.

	- Availability

- SDN

  Control plane resides in a central node that manages all the devices in the network.

	- Control plane

	  Where the internetwork routing decisions are being made --where routes reside.

	- Data/Forwarding plane

	  Where traffic forwarding decisions are being made --where packet forwarding resides, based on routes.

- Honeypot

	- Honeynet
	- Darknet
	- Tarpit

### VPN

- Point-to-Point Tunneling Protocol (PPTP)

  Microsoft-proprietary VPN protocol that works at the data link layer of the OSI model, provide a single connection and can only work over PPP connections.
  
  Authentication: yes
  Data encryption: no
  Compatibility: IP
  Dial-up: yes
  Connection: single (point-to-point)

- Layer 2 Forwarding Protocol (L2F)

  Operates at the Data Link Layer; can encapsulate any LAN protocol; created by Cisco; does not provide encryption; replaced by L2TP.
  
  Authentication: yes
  Data encryption: no
  Compatibility: IP
  Dial-up: yes
  Connection: single (point-to-point)

- Layer 2 Tunneling Protocol (L2TP)

  Provides the functionality of the PPTP, but it can work over networks other than just IP, and it provides a higher level of security when combined with IPSec.
  
  Authentication: yes
  Data encryption: no
  Compatibility: any protocol
  Dial-up: yes
  Connection: single (point-to-point)

- IP Security Protocol (IPSec)

  Operates at the Network Layer; limited to IP.
  https://tools.ietf.org/html/rfc2401
  
  Authentication: yes
  Data encryption: yes
  Compatibility: IP
  Dial-up: no
  Connection: multiple

	- Protocols

		- ESP (id 50)

		  May provide confidentiality (encryption), and limited traffic flow confidentiality. It also may provide connectionless integrity, data origin authentication, and an anti-replay service. (One or the other set of these security services must be applied whenever ESP is invoked.)

		- AH (id 51)

		  Provides connectionless integrity, data origin authentication, and an optional anti-replay service.

	- IKE

	  Negotiates the encryption algorithm selection process. Provides authenticated keying material for use with ISAKMP.

	- Security association (SA)

	  Simplex (one-way) connection that may be used to negotiate ESP or AH parameters.

		- Internet Security Association and Key Management Protocol (ISAKMP)

		  The internet security association and key management protocol (ISAKMP) manages the SA creation process.

			- Authenticate communicating peers
			- Create and manage SAs
			- Provide key generation mechanisms
			- Protect against threats

	- Modes

	  http://www.firewall.cx/networking-topics/protocols/870-ipsec-modes.html

		- Tunnel

		  IPSec's default mode. With tunnel mode, the entire original IP packet is protected by IPSec (data and header encryption). This means IPSec wraps the original packet, encrypts it, adds a new IP header and sends it to the other side of the VPN tunnel (IPSec peer). Between AH and ESP, ESP is most commonly used in IPSec VPN Tunnel configuration.

			- Hosts

			  A host MUST support both transport and tunnel mode.

			- Secure gateways

			  The requirement for any (transit traffic) SA involving a security gateway to be a tunnel SA arises due to the need to avoid potential problems with regard to fragmentation and reassembly of IPsec packets, and in circumstances where multiple paths (e.g., via different security gateways) exist to the same destination behind the security gateways.

				- Secure gateways as hosts

				  Note that for the case where traffic is destined for a security gateway, e.g., SNMP commands, the security gateway is acting as a host and transport mode is allowed. But in that case, the security gateway is not acting as a gateway, i.e., not transiting traffic.

			- Connection

				- Site-to-site VPNs
				- Client-to-site VPNs (remote access)

		- Transport

		  A transport mode SA is a security association between two hosts.
		  
		  When using ESP, provides security services only for higher layer protocols (payload), but does not encrypt the IP header (data encryption only),.
		  When using AH the protection is extended to selected portions of the IP header. Typically used to secure GRE tunnels. If the IP address changes (e.g., when using NAT), using AH will make the connection unviable.

			- Hosts

			  A host MUST support both transport and tunnel mode.

			- Connection

				- Host-to-gateway VPNs (gateway maintenance)
				- Host-to-host VPNs

- TLS-VPN

### Attacks

- Locks

	- Lock picking

	  Uses a tension wrench ("L" tool) to find correct alignment.

	- Lock racking

	  Forces alignment with a tension wrench.

	- Lock bumping

	  Forces alignment with a bump key.

- Spoofing/Masquerading
- DoS

	- Malformed packets

		- Ping of death

			- ICMP

		- Teardrop

		  Attacker sends several large overlapping IP fragments. When the victim system attempts to reassemble these packets, the system could crash.

			- IP

		- Local Area Network Denial (LAND)

		  Uses a malformed IP packet in which the source and destination IP address is the same, so the victim's system tends to crash when reassembling it.

			- IP

	- Flooding

		- Smurf

			- ICMP

		- Fraggle

			- UDP

		- SYN-flood

			- TCP

	- Distributed (DDoS)

- Ransomware
- Sniffing
- Spamming
- Phishing

	- Spear phishing

	  Target is a specific group or person.

	- Whaling

	  Target is specifically C-level.

	- Vishing

	  Phishing over VoIP.

- Skimming

  Involve the unauthorized capture and use of credit or debit card information --like using devices in ATMs.

- Phlashing

  Attack on BIOS.

- DNS

	- Pharming

	  Cyberattack intended to redirect a website's traffic to another, fake site.

	- Hijacking/Poisoning/Redirection

	  Achieved by malware that overrides a computer's TCP/IP configuration to point at a rogue DNS server under the control of an attacker, or through modifying the behavior of a trusted DNS server so that it does not comply with internet standards.

- Social engineering

  Act of manipulating a person to take an action that may or may not be in the "target's" best interest.

	- Shoulder surfing
	- Dumpster diving
	- Tailgating/Piggybacking

- Brute-force

	- Forced browsing

	  Attack where the aim is to enumerate and access resources that are not referenced by the application, but are still accessible.

	- Passwords

		- Dictionary

			- Password guessing

		- Rainbow tables

- Obfuscation

	- Humans

		- Lexical obfuscation

		  Variable names in the source code are defined in a way that may be hard to guess their purposes.

		- Data obfuscation

		  Data is encoded in another set of characters or encoding to make it hard to identify.

		- Control-flow obfuscation

		  Control flow is coded in a way it confuses the person who may analyze it.

	- Computers

		- Prevention obfuscation

		  Makes it difficult to computers to deobfuscate or decompile the code.

## D5. Identity and Access Management

### Technologies

- Administration

	- Centralized
	- Decentralized/Distributed

- SSO

	- Federated identity

	  Portable identity and its associated entitlements that can be used across business boundaries.

		- SPML

		  Used for federation. Specifically designed for exchanging user information for federated identity SSO purposes.

			- Requesting authority
			- Provisioning service provider
			- Provisioning service target

		- Transitive trust

		  The friend of my friend is my friend.

	- SAML

	  Used for SSO. XML-based language that is commonly used to exchange authentication and authorization (AA) information between organizations. Similar to OpenID.

		- Typically uses SOAP or HTTP
		- Service provider
		- Identity provider
		- Principal
		- Assertions

			- Authentication
			- Attribute
			- Authorization

	- XACML

	  Used to define access control policies within an XML format.

	- OpenID

	  Authentication

	- OAuth

	  Authorization

		- OAuth 1.0
		- OAuth 2.0

	- OpenID Connect (OIDC)

	  Authentication + Authorization. OpenID + OAuth.

- IDaaS

	- Cloud
	- Synced
	- Federated

- Directory services

  Allow an administrator to configure and manage how identification, authentication, authorization, and access control take place.

	- X.500
	- Namespaces
	- LDAP

		- Objects

			- DN

			  Represents a collection of attributes about a specific object and is stored in the directory as an entry.

			- RDN
			- DC
			- CN
			- OU
			- O
			- UID

- Kerberos

  Uses symmetric encryption and provides mutual authentication of both clients and servers.

	- Components

		- Principals
		- Realm
		- Key distribution center (KDC)

			- Authentication service (AS)
			- Ticket granting ticket (TGT)
			- Ticket granting service (TGS)

		- Service ticket (ST)

	- Steps

		- 1. User --credentials--> KDC (AS)
		- 2. User <--session key,TGT-- KDC (AS)

		  KDC sends the user a Ticket Granting Ticket (TGT) encrypted with the TGS's secret key.

		- 3. User --session key,TGT--> KDC (TGS)

		  System sends the TGT to the TGS (which runs on the KDC), and a request to access the resource --the TGT proves was previously authenticated.

		- 4. User <--session key 2-- KDC (TGS)

		  TGS creates and sends a second ticket to the user, which will be used to authenticate to the resource. This second ticket contains two instances of the same session key:
		  one encrypted with the user's password
		  the other encrypted with the resource's password --this second key also contains the her system's IP address, sequence number, and a timestamp.

		- 5. User --session key 2--> resource

		  The user's system receives the second ticket, decrypts, and extracts the embedded session key, adds a second authenticator set of identification to the ticket, and sends to the resource.
		  
		  The resource receives the ticket, decrypts and extracts the session key, and decrypts and extracts the two authenticators in the ticket --if the resource is able to decrypt and extract the session key, it knows the KDC created the ticket.

	- SESAME

	  Adds to Kerberos: heterogeneity, sophisticated access control features, scalability of public key systems, better manageability, audit and delegation.

- Web access management (WAM)

  Controls what users can access when using a web browser to interact with web-based enterprise assets.

	- 1. User --credentials--> web server
	- 2. Web server requests --> WAM --> LDAP
	- 3. User requests to access a resource (object).
	- 4. Web server verifies that object access is authorized and allows access to the requested resource.

- Remote access technologies

	- Diameter

	  Provides the same type of functionality as RADIUS and TACACS+ but also provides more flexibility and capabilities to meet the new demands of today's complex and diverse networks.

	- TACACS

		- TACACS+

		  Provides better password protection by allowing 2FA.

		- XTACACS

	- RADIUS

	  Third-party authentication system and described in RFCs 2865 and 2866. Provides AAA, but only encrypts the passwords.

- Credential management systems

	- Registration

	  Manager of the new employee generates a ticket, based on HR information, to create the new account, which provides proof of identity.

		- Proof of identity

	- Maintenance

	  Requests for changes to the permissions on the account follow the same method of registration step.

	- Authoritative system of record (ASOR)

	  Contains the subject's name, associated accounts, authorization history per account, and provision details.

	- Password vaults/managers
	- Password synchronization

		- Not SSO

	- Self-service password reset

	  User provides data and resets password.

### NIST SP 800-63-3

Digital Identity Guidelines
https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-63-3.pdf

- A. Enrollment and identity proofing

  https://doi.org/10.6028/NIST.SP.800-63a

- B. Authentication and lifecycle management

  https://doi.org/10.6028/NIST.SP.800-63b

- C. Federation and assertions

  https://doi.org/10.6028/NIST.SP.800-63c

### Authentication methods

- Type 1. Something you know

	- Password

		- Types

			- Static
			- Passphrase
			- One-time
			- Dynamic

		- Storage

			- Salt

			  Different for every password in a database and are stored in the same database as the hashed passwords.

			- Pepper

			  Same for every password in a database.

	- Questions

- Type 2. Something you have

	- Synchronous dynamic token

		- Time
		- Counter

	- Asynchronous dynamic token

		- Challenge-response token

	- Smartcard

- Type 3. Something you are

	- Enrollment

	  Process of registering with a biometric system, which involves creating an account for the first time.  <2'

	- Throughput

	  Process of authenticating to a biometric system. 6"-10"

	- Accuracy

		- Type I error: false reject rate (FRR)

		  Authorized subject is rejected by the biometric sys- tem as unauthorized.

		- Type II error: false accept rate (FAR)

		  Unauthorized subject is accepted as valid. Worse than false reject for security reasons.

		- Crossover error rate (CER)

	- Types

		- Fingerprint

		  Widely used form of biometric authentication.

			- Whorls
			- Ridges
			- Bifurcations

		- Iris

		  Second best and mostly accepted form of authentication.

		- Retina

		  Most accurate form of biometric as it scans the blood vessel behind the eyes, but not acceptable as it reveals the health condition of the person (PHI).

		- Facial scan
		- Hand geometry
		- Keyboard dynamics
		- Dynamic signature
		- Voiceprint

### Models

- MAC

  System-enforced access control based on a subject's clearance and an object's labels.

	- Clearances (subject)
	- Classification (object)
	- Security Modes

		- Dedicated

		  Signed NDA: ALL
		  Clearance: ALL
		  Approval: ALL
		  Need-to-know: ALL

		- System high

		  Signed NDA: ALL
		  Clearance: ALL
		  Approval: ALL
		  Need-to-know: some

		- Compartmented

		  Signed NDA: ALL
		  Clearance: ALL
		  Approval: some
		  Need-to-know: some

		- Multilevel

		  Signed NDA: ALL
		  Clearance: some
		  Approval: some
		  Need-to-know: some

- DAC

  Subjects full control of objects they have created or have been given access to, including sharing the objects with other subjects.

	- Standard Windows
	- Standard Unix

- Nondiscretionary

  Administrators centrally administer nondiscretionary access controls and can make changes that affect the entire environment.

	- RBAC

	  Role-based access control defines how information is accessed on a system based on the role of the subject.

	- Rule-based

	  Uses a series of defined rules (in the form of "if/then" statements), restrictions, and filters for accessing objects within a system.

	- ABAC

	  Attribute-based access control (ABAC) includes contexts, such as the time of day, the state or phase of a project, and other contextual events, in order to provide further granularity to which objects can be accessed by which subjects, when, and how.

### Identity Lifecycle

- 1. Provisioning

	- Entitlement

	  Privileges granted to users when first provisioning an account.

- 2. Modifying

	- Access aggregation

	  Amount of privileges that users collect over time.

		- Privilege creep

- 3. Auditing
- 4. Suspending

	- Deletion

## D6. Security Assessment and Testing

### Audit

Systematic assessment of significant importance to the organization that determines whether the system or process being audited satisfies some external standards.

- Assessment

  Series of tests across a deployment of related devices or systems, performed to determine the general security posture of an entire functional area.

	- Test

	  Procedure that records some set of properties or behaviors in a system being tested and compares them against predetermined standards.

- Audit trails

  Provide the data that supports audits or review and essentially are what make auditing and subsequent detection of attacks and misbehavior possible.

### Audit Process

- Determine the goals
- Involve the right business unit leaders
- Determine the scope
- Choose the audit team
- Plan the audit
- Conduct the audit
- Document the results
- Communicate the results

### Vulnerability Assessment

More automated
Minutes or hours
Nonintrusive
Interviews and tools
Standard scanners
Report false positives

- Written agreement
- Type

	- Credentialed/Authenticated
	- Uncredentialed/Unauthenticated

- SCAP

	- CVE

	  Naming system for vulnerabilities.

	- CVSS

	  Standardized scoring system for severity.

	- CCE

	  Naming system for system configuration issues.

	- CPE

	  Naming system for operating systems, applications, and devices.

	- XCCDF

	  Language for specifying security checklists.

	- OVAL

	  Language for describing security testing procedures.

- Misleading

	- False positive
	- False negative

- Phases

	- Prepare

	  Determine the scope, update tools.

		- Scope
		- Tools

	- Scan

	  Should be automated for better results.

	- Remediate

	  Fix, remediate, or accept the risk.

	- Document

### Penetration Testing

Manual
Days
Intrusive
Tools and intuition
Advanced techniques
Rule out false positives

- Perspective

	- Internal
	- External

- Approach

	- Blind
	- Double-blind

- Knowledge

	- Black-box/Zero-knowledge

	  Provides a penetration tester with information that could otherwise be easily obtained by using publicly available sources.

	- White-box/Crystal-box/Full-knowledge

	  Provides every piece of available information to the penetration tester.

	- Gray-box/Partial-knowledge

	  Provides a penetration tester with a limited amount of information about the customer's environment but does not provide access to everything.

- Methodology

	- Planning
	- Reconnaissance
	- Scanning/Enumeration
	- Vulnerability assessment
	- Exploitation
	- Reporting
	- Frameworks

		- NIST SP 800-115

		  Technical Guide to Information Security Testing and Assessment
		  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-115.pdf

			- Review techniques

				- Documentation
				- Logs
				- Ruleset
				- System configuration
				- Network sniffing
				- File integrity checking

			- Target identification and analysis techniques

				- Network discovery
				- Vulnerability scanning
				- Wireless scanning

					- Bluetooth scanning

			- Target vulnerabilities validation techniques

				- Password cracking
				- Social engineering
				- Pentest phases

					- Planning
					- Discovery
					- Attack

						- Gaining access
						- Escalating privileges
						- System browsing
						- Install additional tools

					- Reporting

			- Security assessment planning

				- Assessment policy
				- Prioritizing and scheduling
				- Selecting and customizing
				- Logistics
				- Plan development
				- Legal considerations

			- Security assessment execution

				- Coordinating
				- Assessing
				- Analysis
				- Data handling

					- Collection
					- Storage
					- Transmission
					- Destruction

			- Post-testing activities

				- Mitigation recommendations
				- Reporting
				- Remediation/Mitigation

		- OWASP Testing Guide
		- OSSTMM
		- FedRAMP Penetration Test Guidance
		- PCI DSS Information Supplement on Penetration Testing

### Log Review & Analysis

- Sampling

  Process of extracting elements from a large body of data to construct a meaningful representation or summary of the whole.

- Clipping-level/Threshold

  Form of nonstatistical sampling that records only events that exceed a threshold.

### Software Testing

- By automation

	- Manual
	- Automatic

- By runtime

	- Static

	  Includes walk-throughs, syntax checking, and code reviews.

		- Misuse case

		  Uses clear examples of ways that software users might attempt to misuse the application, so this testing evaluates the vulnerability of software to these known risks.

	- Dynamic

	  Security checks are performed while actually running or executing the code or application under review.

		- Fuzzing

		  Uses modified inputs to test software performance under unexpected circumstances.

			- Mutation

			  Modifies known inputs to generate synthetic inputs that may trigger unexpected behavior.

			- Generational

			  Develops inputs based on models of expected inputs to perform the same task.

- By visibility

	- White-box

	  Gives the tester access to program source code, data structures, variables, etc.

	- Black-box

	  Gives the tester no internal details; the software is treated as a black box that receives inputs.

- By proactiveness

	- Synthetic transations

	  Proactive. Involve building scripts or tools that simulate activities normally performed in an application.

	- Real user monitoring

	  Reactive, monitors the user experience.

- By levels

	- Unit

	  Low-level tests of software components, such as functions, procedures, or objects.

	- Interface

	  Testing multiple software components as they are combined into a working system.

		- APIs
		- UIs
		- Physical interfaces

	- System

	  Testing the whole system.

	- Acceptance

	  Testing to ensure that the software meets the customer's operational requirements.

- Coverage

	- Formula

	  test coverage = (# use cases tested) / (total # use cases)

	- Criteria

		- Branch

		  All if/else statements was tested in every possible ways.

		- Condition

		  All logical tests has been executed under all sets of inputs.

		- Function

		  All functions have been tested and returned results.

		- Loop

		  Every loop has been executed under conditions that cause code execution multiple times, only once, and not at all.

		- Statement

		  Every lines have been executed.

### Testers/Assessors

- Internal
- External/Second party

  Typically tied to the terms of a contract between business entities.

	- Big four

		- Ernst & Young
		- Deloitte & Touche
		- PricewaterhouseCoopers
		- KPMG

- Third-party

  Usually used to determine if an entity is compliant with applicable government regulations. They are likely to have a breadth of experience beyond what internal teams may possess, due to having inspected a wider array of systems, controls, and enterprises.

	- SOC-1

	  Focused on financial reporting risks.

		- Type 1

		  A point in time.

		- Type 2

		  A period of time.

	- SOC-2

	  Focused on 5 trust principles:
	  Security
	  Availability
	  Confidentiality
	  Integrity
	  Privacy

		- Type 1

		  A point in time.

		- Type 2

		  A period of time.

	- SOC-3

	  Summarized and sanitized version of SOC 2 for public distribution.

- Metrics

	- KPI
	- KRI

		- Examples

			- Number of open vulnerabilities
			- Time to resolve vulnerabilities
			- Vulnerability/defect recurrence
			- Number of compromised accounts

### Site survey

Process of investigating the presence, strength, and reach of Wireless Access Points (WAPs) deployed in an environment.

## D7. Security Operations

### BCM (BCP + DRP)

- Disaster types

	- Natural
	- Human

		- Intentional

			- Warfare
			- Terrorism
			- Sabotage
			- Personnel shortages

				- Strikes
				- Pandemics
				- Transportation

		- Nonintentional

			- Errors
			- Omissions

	- Environmental

		- Electrical
		- Temperature
		- Humidity

- DR process

	- 1. Respond

	  Assess the damage, speed is essential.

	- 2. Activate team

		- Calling tree
		- Recovery team

		  Efforts in reconstituting critical business functions at an alternate location.

		- Skeleton crew

		  Consists of the employees who carry out the most critical functions following a disaster to start working first during the recovery process with the main objective of maintaining critical operations.

	- 3. Communicate

	  Communication for updates must occur out-of-band and external communications must take place.

		- Internal
		- External

	- 4. Assess

	  A more detailed and thorough assessment will be performed by the disaster recovery team.

	- 5. Reconstitution

	  The primary goal of the reconstitution phase is to successfully recover critical business operations at either a primary or secondary site.

		- Salvage team

		  Employed to begin the recovery process at the primary facility that experienced the disaster.

		- Succession planing

		  Addresses the steps that will be taken to fill a senior executive role should that person retire, leave the company, or die to protect the company by maintaining leadership roles.

- Backups

	- Archive bit
	- Types

		- Mirror
		- Full
		- Incremental
		- Diferential

	- Validation

		- Checksum
		- CRC
		- Hash
		- Preventative restoration

	- Rotation scheme

		- FIFO
		- Grandfather-father-son (GFS)
		- Tower of Hanoi

	- Techniques

		- Electronic vaulting

		  Good tool for data that need to be backed up on a daily or possibly even hourly rate.

			- Tape vaulting

		- Remote journaling

		  Saves the database checkpoints and database journal to a re- mote site.

		- Database shadowing

		  Uses two or more identical databases that are updated simultaneously. The shadow databases can exist locally, but it is best practice to host one shadow database offsite.

		- Database replication

		  Mirrors a live database, allowing simultaneous reads and writes to multiple replicated databases by clients.

- Continuity of Operations

	- Fault tolerance

		- RAID

		  Mirroring: stores the full data in multiple disks.
		  Striping: spreads data across multiple disks.
		  Parity: stores both the data and the corresponding parity.

			- 0. Striping

			  Disks: 2
			  Redundancy: no

			- 1. Mirroring

			  Disks: 2
			  Redundancy: yes

				- Disk duplexing

				  With mirroring the two (or more) physical places where the data is written may be attached to the same controller, leaving the storage still subject to the single point of failure of the controller itself; in duplexing, two or more controllers are used.

			- 5. Parity

			  Disks: 3
			  Redundancy: yes

			- 10. Striping & mirroring

			  Disks: 4
			  Redundancy: yes

		- Hierarchical storage management (HSM)

		  Provides continuous online backup functionality. It combines hard disk technology with the cheaper and slower optical or tape jukeboxes.

		- Online transaction processing (OLTP)

		  Used when databases are clustered to provide high fault tolerance and performance. It provides mechanisms to watch for and deal with problems when they occur.

		- System redundancy

			- Redundant hardware

			  Provide internal hardware redundancy of components that are extremely prone to failure.

			- High-availability/Failover clusters

			  Uses multiple systems that are already installed, configured, and plugged in, so that if a failure causes one of the systems to fail, another can be seamlessly leveraged to maintain the availability of the service or application being provided.

				- Active-active/Load balance

				  Each member actively processes data in advance of a failure.

				- Active-passive/Hot standby

				  Backup systems only begin processing when a failure is detected.

### Forensics

Forensics is a science and an art that requires specialized techniques for the recovery, authentication, and analysis of electronic data that could have been affected by a criminal act.

- Collection

  Evidence gathering, including interviewing witnesses.
  Develop a plan to acquire the data
  Acquiring the data
  Verifying the integrity of the acquired data

	- Secure the scene
	- Locard's exchange principle

	  States that a criminal leaves something behind at the crime scene and takes something with them.

	- Motive, opportunity, and means (MOM)

	  Strategy used to understand why a crime was carried out and by whom.

		- Motive

		  Motive is the “who” and “why” of a crime.

		- Opportunity

		  Opportunity is the “where” and “when” of a crime.

		- Means

		  Means pertains to the capabilities a criminal would need to be successful.

	- Sources

		- Oral/Written statements
		- Documents
		- Digital forensics

			- Live evidence (volatile)
			- Secondary storage

				- Allocated space
				- Unallocated space

				  Includes portions that have never been allocated, as well as previously allocated portions that have been marked unallocated.

				- Slack space

				  Extra space within the cluster.

				- Bad blocks/clusters/sectors

				  Attackers could intentionally mark sectors or clusters as being bad in order to hide data within this portion of the disk. Sector == block.

			- eDiscovery

			  Facilitates the processing of electronic information for disclosure.

	- Chain of custody

	  History that shows how evidence was collected, analyzed, transported, and preserved in order to be presented in court. Dictates that all evidence be labeled with information indicating who secured and validated it.

	- Forensics field kit

		- Documentation tools

		  Tags, labels, and timelined forms...

		- Disassembly and removal tools

		  Antistatic bands, pliers, tweezers, screwdrivers, wire cutters...

		- Package and transport supplies

		  Antistatic bags, evidence bags and tape, cable ties...

- Examination

  Assessment and extraction the relevant pieces of information from the collected data.

	- Evidence

		- Types

			- Real

			  Things that may actually be brought into a court of law, such as computer equipment and weapons.

			- Testimonial

			  Consists of the testimony of a witness either verbal or recorded.

			- Documentary

			  Written items brought into court to prove a fact at hand.

				- Best evidence

				  The original document must be introduced.

				- Parol evidence

				  On agreements put into written form, it is assumed that the document contains all the terms.

			- Hearsay

			  Indirect evidence.

		- Characteristics

			- Relevant

			  Must have a reasonable and sensible relationship to the findings.

			- Complete

			  Must present the whole truth of an issue.

			- Sufficient

			  Must be persuasive enough to convince a reasonable person of the validity of the evidence.

			- Reliable

			  Must be consistent with the facts.

		- Integrity

			- Evidence must be reliable
			- Chain of custody

		- Beyond a reasonable doubt
		- Rule of thumb: always work on the copy of the evidence

- Analysis

  Include identifying artifacts from the information that has been extracted.

	- Investigative techniques

		- Media analysis
		- Software analysis
		- Network analysis

	- Types of investigations

		- Criminal
		- Civil
		- Regulatory
		- Administrative

- Report

  Preparing and presenting the information resulting from the analysis phase.

- NIST SP 800-86

  Guide to Integrating Forensic Techniques into Incident Response
  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-86.pdf

	- Establishing forensics capability
	- Forensics process

		- Collection
		- Examination
		- Analysis
		- Reporting
		- Recommendations

### Incident Response

- Process

	- 1. Detection

	  Systems configuration, initial alert, triage.

	- 2. Response

	  CSIRT activation, evidence collection.

	- 3. Mitigation

	  Contain the incident by limiting its scope.

	- 4. Reporting

	  Report the incident to stakeholders, must be compliant to regulatory laws.

		- Compliance to regulatory laws

	- 5. Recovery

	  Return systems to a fully functional stage.

	- 6. Remediation

	  Perform root cause analysis and implement methods to prevent future incidents.

		- Root cause analysis

	- 7. Lessons learned

	  Examine the incident and the response and possibly take actions to improve detection.

- NIST SP 800-61

  Computer Security Incident Handling Guide
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf

	- Events and incidents
	- Handling

		- Preparation

			- Preparing to handle
			- Prevention

		- Detection and analysis

			- Analysis
			- Documentation
			- Prioritization
			- Notification

		- Containment, eradication, and recovery

			- Strategy
			- Gathering and handling
			- Identifying attackers

		- Post-incident activity

			- Lessons learned
			- Evidence retention

	- Coordination and information sharing

- Computer security incident response team (CSIRT)

	- Basics

		- Documentation

			- Constituency
			- Roles and responsibilities
			- Code of practice
			- Contact lists
			- Call trees

		- Forensics

	- Types

		- Virtual

		  Made up of experts who have other duties and assignments within the organization.

		- Permanent

		  Folks strictly dedicated to incident response.

		- Hybrid

		  Some members are permanently assigned to the team, whereas others are called as needed.

### Malware

- Types

	- Virus

		- Companion

		  Self-contained executable files that escape detection by using a filename similar to, but slightly different from, a legitimate operating system file.

		- Multipartite

		  Use more than one propagation technique in an attempt to penetrate systems that defend against only one method or the other.

		- Polymorphic

		  Modify their own code as they travel from system to system.

		- Stealth

		  Hide themselves by actually tampering with the operating system to fool antivirus packages into thinking that everything is functioning normally.

			- Boot sector

	- Worm
	- Trojan
	- Logic bomb
	- Ransomware
	- Rootkit

	  Freely available on the internet and exploit known vulnerabilities in various operating systems, commonly used to escalate privileges.

	- Spyware/Adware
	- Zero-day

- Antimalware

	- Policy

		- Training and awareness

	- Prevention

		- Whitelist
		- Network segmentation

	- Detection

		- Signature-based scanners

			- No zero-day detection

		- Heuristic-based scanners

			- High false-positives

		- Activity monitors
		- Change detection

	- Treatment

		- 1. Tries to disinfect
		- 2. Quarantines
		- 3. Deletes

### Endpoint Security

- Antimalware
- Application whitelisting
- Removable media controls
- Disk encryption
- Cable locks
- NIST SP 800-46

  Guide to Enterprise Telework, Remote Access, and Bring Your Own Device (BYOD) Security
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-46r2.pdf

	- Remote access security

		- Tunneling
		- Application portals
		- Remote desktop
		- BYOD

		  Each person uses its own device to work.

			- COPE

			  Company purchases and provides devices to employees.

			- CYOD

			  User chooses a device from a company's list. Requires 2 devices: 1 for business, 1 for personal use.

	- Remote access solution security

		- Remote access server security
		- Remote access server placement
		- AAA

	- Telework client device security

		- Virtual machines
		- Encryption
		- Backups

	- Telework and remote access life cycle

		- Initiation
		- Development
		- Implementation
		- Operations and maintenance
		- Disposal

### Monitoring

- NIST SP 800-137

  Information Security Continuous Monitoring (ISCM) for Federal Information Systems and Organizations
  https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-137.pdf

	- Fundamentals

		- Organization-wide view
		- System authorizations
		- Roles

	- Process

		- Define
		- Establish
		- Implement
		- Analyze/Report
		- Respond
		- Review/Update

### Asset Management

- Configuration management

	- NIST SP 800-128

	  Guide for Security-Focused Configuration Management of Information Systems
	  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-128.pdf

		- Planning

		  Includes developing policy and procedures to incorporate Security-Focused Configuration Management (SecCM) into existing information technology and security programs, and then disseminating the policy throughout the organization.

		- Identifying and implementing configurations

		  A secure baseline configuration for the system is developed, reviewed, approved, and implemented.

		- Controlling configuration changes

		  The emphasis is put on the management of change to maintain the secure, approved baseline of the system.

		- Monitoring

		  Used as the mechanism within SecCM to validate that the system is adhering to organizational policies, procedures, and the approved secure baseline configuration.

	- Baselining
	- Vulnerability management

- Change management

	- Request
	- Review

	  Experts within the organization review the change.

	- Approval

	  Based on the review, these experts then approve or reject the change. They also record the response in the change management documentation.

	- Test

	  Once the change is approved, it should be tested, preferably on a non- production server.

		- New functionality
		- Regression

		  Ensures that a change has not broken existing functionality or introduced new problems.

	- Schedule & implement

	  The change is scheduled so that it can be implemented with the least impact on the system and the system’s customer.

	- Document

	  The last step is the documentation of the change to ensure that all interested parties are aware of it. This often requires a change in the configuration management documentation.

		- Configuration management
		- BCP/DRP update

- Patch management

	- Monitoring

		- Threat intelligence
		- Vendor notification
		- Automated

			- Agent
			- Agentless
			- Passive

	- Acquire and evaluate
	- Open new change

		- Change management

### Administrative Security

- Least privilege

  Minimum amount of authorization.

	- Privileges

	  Combination of rights and permissions.

		- Permissions

		  Focus on objects. Refer to the access granted for an object and determine what you can do with it.

		- Rights

		  Focus on subjects. Refers to the ability to take an action on an object.

	- Need-to-know

	  More granular than least privilege. A user have no access to information that is not required by her, even if she has a rank, clearance level, or authorization for greater access.

- Separation of duties (SoD)

  Multiple people are required to complete critical or sensitive transactions.

	- Collusion

	  Two parties conspiring to undermine the security of the transaction.

- Rotation of duties/Job rotation

  One person does not perform critical functions or responsibilities for an extended period of time.

- Mandatory leave/Forced vacation

  Reduces or detects personnel single points of failure, and detects and avoids fraud.

- Nondisclosure agreement (NDA)
- Noncompete agreement (NCA)

  Attempts to prevent an employee with special knowledge of secrets from one organization from working in a competing organization in order to prevent that second organization from benefiting from the worker’s special knowledge of secrets.

- Background checks

## D8. Software Development Security

### Programming Concepts

- Machine language/code

  Format the computer’s processor can understand and work with directly, represented in binary format (1 and 0).

	- CPU dependent

- Assembly language

  Symbolic representation of machine-level instructions --symbols are mnemonics.

	- Assemblers

	  Tools that convert high-level language statements into the necessary machine-level format for specific processors to understand.

- Bytecode
- Source code
- Compiler
- Interpreter
- Linking

  Capability for one program to call another program.

- Embedding

  Capability to place one piece of data inside a foreign program or document --as used in OLE.

### Object-oriented Programming

- Class

  Collection of the common methods from a set of objects that defines the behavior of those objects.

- Object/Instance

  Objects are instances of or examples of classes that contain their methods.

- Attribute
- Method

  Internal code that defines the actions an object performs in response to a message.

- Message

  Communication to or input of an object.

- Inheritance

  Occurs when methods from a class (parent or superclass) are inherited by another subclass (child).

- Polymorphism

  Characteristic of an object that allows it to respond with different behaviors to the same message or method because of changes in external conditions.

- Deferred commitment

  Internal components of an object can be redefined without changing other parts of the system.

- Cohesion

  Reflects how many different types of tasks a module can carry out. High cohesion means that the module carries out one basic task (such as subtraction of values) or several tasks that are very similar (such as subtraction, addition, multiplication). The higher the cohesion, the easier it is to update or modify and not affect the other modules that interact with it.

	- The higher, the better

- Coupling

  Indicates how much interaction one module requires to carry out its tasks. If a module has low or loose coupling, this means the module does not need to communicate with many other modules to carry out its job. These modules are easier to understand and easier to reuse than those that depend upon many other modules to carry out their tasks.

	- The lower, the better

- Object Request Broker (ORB)

	- COM
	- DCOM
	- CORBA

### Software Development Lifecycle (SDLC)

There are some SDLC models, but the main concept is:
You imagine the system
Document the desired functionalities
Design how data will enter and the outputs
Select the methodology, code and test
Document how the system processes data
Test the system by a 3rd party
Document tests and compliance to controls
System is certificated by an authorized officer
Management approves (accredits) system to implementation
System is put into operation
Regular maintenance takes place

- Requirements gathering

  Why to create, what will do, and for whom --security/privacy risk assessment, risk-level acceptance, and informational, functional, behavioral requirements.

	- Conceptual definition

	  Simple statement on the purpose of the project.

	- Functional requirements  determination

	  Functional requirements defined in terms of inputs, behavior, and outputs.

- Design

  How to accomplish the goals identified --attack surface analysis, threat modeling.

	- Control specifications development

	  Design of adequate security controls.

	- Design review

	  How the parts of the system will interoperate and how the modular system structure will be defined.

- Development

  Programming to meet desired requirements --automated CASE tools, static analysis.

	- Code review walk-through

	  Development personnel review the code.

		- Peer review
		- Fagan

			- Planning

			  Inspection entry criteria, participants, arrange the meeting.

			- Overview

			  What is to be inspected, assign roles to participants.

			- Preparation

			  Roles fulfillment.

			- Inspection

			  Find defects.

			- Rework

			  Author reworks all defects, possibly.

			- Follow-up

			  Ensuring all fixes are effective and no secondary defects are introduced.

		- Metrics

			- Lines of code (LoC)
			- Function point

			  Estimates the size of an application by the number of LoCs that perform a specific function.

			- Defect density

			  Determines the average number of defects per LoC.

			- Risk density

			  Assigns risk rankings (high, medium, low...) to defects discovered during review and can be used with other metrics, such as LoC or Function Point.

- Testing

  Verification and validation --dynamic analysis, fuzzing, manual testing, and unit, integration, acceptance, regression testing.

	- System test review

	  Developers and users validate the system against predefined usual and unusual scenarios.

		- Verification

		  Software is evaluated against some specification.

			- Certification

			  Comprehensive evaluation of the technical and nontechnical security features of an IT system and other safeguards made in support of the accreditation process to establish the extent to which a particular design and implementation meets a set of specified security requirements. 
			  
			  System certification is the technical evaluation of each part of a computer system to assess its concordance with security standards. Performed by internal teams.

			- Accreditation

			  Formal declaration by the designated approving authority (DAA) that an IT system is approved to operate in a particular security mode using a prescribed set of safeguards at an acceptable level of risk. Performed by third-party.

		- Validation

		  Does the software meets real world requirements?

			- Acceptance

			  Examines whether software meets various end-state requirements, whether from a user or customer, contract, or compliance perspective.

				- User

				  Focuses mainly on the functionality, thereby validating the fitness- for-use of the system by the business user.

				- Operational

				  Validates whether the system meets the requirements for operation (system administration) before the system is released.

				- Contract

				  Performed against the contract’s acceptance criteria for producing custom-developed software.

				- Compliance

				  Performed against the regulations that must be followed, such as governmental, legal, or safety regulations.

- Operations and maintenance

  Deploying and ensuring proper configuration, patch, and monitoring --final security review.

	- Maintenance and change management

	  Ensure continued operation, handling changes through a formalized process.

- Methodologies

	- Waterfall

	  Sequential life-cycle approach, each phase must be entirely complete before the next phase can begin, with reviews at the end of each phase. Best used in small projects.

	- Spiral

	  4 main phases:
	  determine objectives,
	  risk analysis,
	  development and test, and
	  plan the next iteration.

	- RAD

	  Allows the customer to be involved during the development phases, the planning of how to improve the software is interleaved with the process of developing the software. Combines the use of prototyping and interactive development.

		- Prototypes

	- Agile

	  Umbrella for several development methodologies, focusing on incremental and interactive development methods.

		- Scrum

		  One of the most widely adopted agile methodologies in use, acknowledges the fact that customer needs cannot be completely understood and will change over time. Composed of many sprints, a fixed-duration development interval that is usually 2 weeks in length and promises delivery of specific features.

		- XP

		  Uses pair programming and relies on test-driven development.

	- DevOps

		- Developers
		- Quality assurance
		- Operations

### Software Licensing

- Free software

	- Free as in beer

		- Freeware

	- Free as in freedom

		- Open source

- Shareware
- Software escrow

  Process of having a third-party store an archive of computer software.

### Constrained Interfaces

- Database views
- Command suppression
- Dimmed/Disabled options

### Databases

- Types

	- Relational

	  Consisted of attributes (columns) and rows (tuples).

		- Tables/Relations

			- Rows/Tuples
			- Columns/Attributes

		- Primary key

			- Candidate key

		- Foreign key

	- Hierarchical

	  Combines records and fields related in a logical tree structure with branches and leaves, commonly used to build indexes for relational databases.

		- DNS

	- Object-oriented

	  Returns not only the data, but code to process it.

	- Object-relational

	  Relational database with OO frontend.

- Checkpoint

  Used to recover data if there is a system failure or problem during a transaction.

- Normalization

  Seeks to make the data in a database table logically concise, organized, and consistent by removing redundant data and improving the integrity and availability of the database.

- Queries

	- DDL

	  Used to create, modify, and delete tables.

	- DML

	  Used to query and update data stored in the tables.

- Data warehousing

  Combining data from multiple databases/sources into a large database in the warehouse.

- Data mining

  Massaging the data held in the data warehouse into more useful information, usually producing metadata.

- ACID

	- Atomicity

	  Transactions are divided into units of work.

	- Consistency

	  Transactions follow the integrity policy of each database.

		- Integrity

			- Semantic

			  Each attribute (column) value is consistent with the attribute data type.

				- Attributes

			- Entity integrity

			  Each tuple has a unique primary key that is not null.

				- Tuples

			- Referential

			  Every foreign key in a secondary table matches a primary key in the parent table.

				- Foreign key

	- Isolation

	  Transactions do not interact with other transactions --their results are only available after the transaction is done.

		- Concurrency

		  Processes running simultaneously, which can negatively affect the integrity of the database if not properly controlled.

	- Durability

	  Transaction is verified, committed, and cannot be rolled back.

		- Journal

		  Log of all database transactions.

### Capability Maturity Model (CMM)

- L1. Initial

  Development is ad hoc or even chaotic, success is usually the result of individual heroics.

- L2. Repeatable

  Formal management structure, change control, and quality assurance are in place. No formal process models defined.

- L3. Defined

  Formal procedures are in place that outline and define processes carried out in each project.

- L4. Managed

  Formal processes are in place to collect and analyze quantitative data, and metrics are defined and fed into the process-improvement program.

- L5. Optimizing

  Company has budgeted and integrated plans for continuous process improvement.

### Common Software Vulnerabilities

http://cwe.mitre.org/top25/archive/2020/2020_cwe_top25.html

- Buffer overflow

  Occur when a programmer fails to perform bounds checking, used to insert and run shellcode.

- Race condition/TOCTOU

  Attacker attempts to alter a condition after it has been checked by the operating system, but before it is used, like in TOC/TOU attacks.

- XSS

  Leverages the third-party execution of web scripting languages such as JavaScript within the security context of a trusted site. Executes a script in a trusted context: 
  
  <script>alert(“XSS Test!”);</script>
  
  The previous code would pop up a harmless “XSS Test!” alert. A real attack would include more JavaScript, often stealing cookies or authentication credentials.

- XSRF

  Attempts to trick the victim into loading a web page that contains a malicious request or operation. Tricks a user into processing a URL, sometimes by embedding the URL in an HTML image tag, that performs a malicious act; for example, tricking a white hat into rendering the following image tag:
  
  <img src=“https://bank.example.com/transfer-money?from=WHITEHAT& to=BLACKHAT”>

- SQLi
- Privilege escalation
- Backdoor
- Covert channel

### SEI's top 10 secure code practices

https://wiki.sei.cmu.edu/confluence/display/seccode/Top%2B10%2BSecure%2BCoding%2BPractices

- 1. Validate input
- 2. Heed compiler warnings
- 3. Architect and design for security policies
- 4. Keep it simple
- 5. Default deny
- 6. Adhere to principle of least privilege
- 7. Sanitize data sent to other systems
- 8. Practice defense in depth
- 9. Use effective quality assurance techniques
- 10. Adopt a secure coding standard

## References

### CISSP Official Study Guide

Authors: Mike Chapple and James Michael Stewart and Darril Gibson
Publisher: Sybex
Edition: 8th
Year: 2018

### CISSP All-in-One

Authors: Shon Harris and Fernando Maymí
Publisher: McGraw Hill
Edition: 8th
Year: 2019

### Eleventh Hour CISSP

Authors: Eric Conrad and Seth Misenar and Joshua Feldman 
Publisher: Syngress
Edition: 3rd
Year: 2017

### Destination Certification

https://www.youtube.com/c/DestinationCertification

## Credits

### José Lopes

https://lopes.id/
https://linkedin.com/in/jlopesjr
https://github.com/lopes
https://twitter.com/lopesoj
https://reddit.com/user/forkd_

*XMind - Trial Version*