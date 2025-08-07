# Module 8
## Event and Incident Detection
- Security Mindset - the ability to evaluate risk and constanatly seek out and identify the potential or actual breach of a system, applicaiton, or data
### Classifying for safety
- public data - already accessible to the public and poses a minimal risk to the organization
- private data - information that should be kept from the public
    - ex. e-mail addresses, employee identification numbers, and organization's research data
- sensitive data - information that must be protected from everyone that does not have authorized access
    - ex. PII, SPII, PHI like bank account numbers, usernames/passwords, SS #'s, passport numbers, and medical info
- confidential data - important for an organization's ongoing business operations and usually has limits on the # of people who have access
    - ex. might only be accessed by the signing of NDA's, like trade secrets, financial records, and sensitive government data

### A security event is only considered a security incident when an actual breach occurs

- Business continuity plan - a document that outlines the procedures to sustain business operations during and after a significant disruption
  - goal: keep the business itself running
    - conduct a business impact analysis - focuses on the possible effects a disruption of business functions have on an org
    - identify, document, & implement steps to recover critical business functions&processes - actionable steps toward responding to a security event
    - organize a business continuity team - brings various members of the org together to help execute the plan (cybersecurity, IT, HR, comms & operations dept's)
    - conduct training for the business continuity team - considers different risk scenarios and prepares for security threats during training

- Disaster recovery plan - allows an organization's security team to outline the steps needed to minimize the impact of a security incident, such as a successful
    ransomware attack
  - goal: restore technology infrastructure
    - implementing recovery strategies to restore software
    - implementing recovery strategies to restore hardware functionality
    - identifying apps and data that might be impaced after a security incident
        - ex. how to recover backups after an attack

## Escalation
- Incident Escalation - the process of identifying a potential security incident, triaging it, and handing it off to a more experienced team member
- CISO (Chief Information Security Officer)
### Low level security issues
- issues that are security risks, but that do not result in the exposure of PII (Personally Identifiable Information)
      - ex. an employee having one failed login attempt, or an employee who downloads unapproved software
  
### Incident Classification Types
- Malware infection - an icident type that occurs when malicious software designed to disrupt a system infiltrates an org's computers or network
- Unauthorized access - an incident type that occurs when an indiviual gains digital or physical access to a system or app without permission
- Improper Usage - an incident type that occurs when an employee of an organization violates the org's accetaple use policies

### Roles and Responsibilities During Escalation

### Data owners
 - is the person that decides who can access, edit, use, or destroy their information. Data owners have administrative control over specific information hardware or software and are accountable for the classification, protection, access, and use of company data. For example, consider a situation where an employee gains unauthorized access to software they do not need to use for work. This kind of security event would be escalated to the data owner of that software.

### Data controllers 
 - determine the procedure and purpose for processing data. This role largely focuses on collecting the personal information of customers. The data controller determines how that data is used. The data controller also ensures that data is used, stored, and processed in accordance with relevant security and privacy regulations. If sensitive customer information was at risk, that event would be escalated to data controllers.

### Data processors 
 - report directly to the data controller and are responsible for processing the data on behalf of the data controller. The data processor is typically a vendor and is often tasked with installing security measures to help protect the data. Data processing issues are typically escalated to the individual who oversees the third-party organization responsible for data processing.

### Data custodians 
 - assign and remove access to software or hardware. Custodians are responsible for implementing security controls for the data they are responsible for, granting and revoking access to that data, creating policies regarding how that data is stored and transmitted, advising on potential threats to that data, and monitoring the data. Data custodians are notified when data security controls need to be strengthened or have been compromised.

### Data protection officers (DP0's)
 - are responsible for monitoring the internal compliance of an organization’s data protection procedures. These individuals advise the security team on the obligations required by the organization's data protection standards and procedures. They also conduct assessments to determine whether or not the security measures in place are properly protecting the data as necessary. DPOs are notified when set standards or protocols have been violated.  

## Stakeholders
- an individual or group that has an interest in the decisions or activities of an organization
- 
 - Risk Managers - help identify risks and manage responses to security incidents
          - notify the legal department regarding regulatory issues
          - inform the organizatoin's public relations team
 - Chief Executive Officer (CEO) - responsible for financial and managerial decisions
          - report to shareholders and manage the operations of a company
 - Chief Financial Officer (CFO) - senior executive responsible for managing financial operations
          - concerned about security from a financial standpoint
          - interested in the costs associated with tools/strategies necessary to combat security incidents
 - Chief information Security Officer (CISO) - high level executives responsible for developing seucirty architecture                 and conduting risk analysis and system audits, and creating security and business continuity plans
 - Operations Manager - oversee security professionals to help identify and safeguard an organization
          - often work directly with analysts as first line of defense
          - generally responsible for the daily maintenance of security operations

### Creating security communications
- typically have a beginning, middle, and end. describe the conflict and an eventual resolution
      - the security story details what the security challenge is, how it iimpacts the organization, and possible             solutions
      - also includes data related to the challenege, it's impact and proposed solutions
          - can be in the form of reports that summarize findings or a list of issues that need attention

 ### If your message is straightforward, an instant message or phone call might be the route to take. If you have to describe a complex situation with multiple layers, an email or in-person meeting might be the better option. If you’re providing a lot of data and numbers, sharing a graph might be the best solution. Each situation helps you determine the best means of communication. 

## AI Usage
Task - what do you want the model to do 
    - Persona - what expertise the response should sound like (professional writer) or a specific audience
    - Format - how you want the output to appear. bullet list, graph, etc
Context - necessary details to refine the output
References - could help refine the output by giving past examples
Evaluate - just evaluating the first output
Iterate - trying again by editing the prompt for a different/better output
