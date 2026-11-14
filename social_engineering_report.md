^o
# Social Engineering Attacks: Phishing, Pretexting and Baiting

## 1. Introduction

Social engineering is a form of cyberattack in which criminals manipulate people into revealing confidential information, providing unauthorised access, or performing actions that compromise an organisation's security. Instead of relying only on technical vulnerabilities in computer systems, attackers take advantage of human behaviour, trust and decision-making. These attacks often involve impersonating trusted individuals, creating a sense of urgency, or offering something attractive to encourage victims to cooperate.

Social engineering remains an effective attack method because people are involved in almost every organisational process, including communication, financial transactions and information sharing. Even organisations with advanced security systems can be exposed when an employee is persuaded to disclose a password, open a malicious attachment or ignore normal security procedures. The Cybersecurity and Infrastructure Security Agency (CISA) identifies phishing as a form of social engineering and highlights the importance of recognising suspicious communications and reporting them. This demonstrates why employee awareness is an important part of an organisation's overall cybersecurity strategy.

This report examines three common social engineering techniques: phishing, pretexting and baiting. It also discusses quid pro quo attacks, provides documented examples, and recommends measures that organisations can use to reduce their exposure to these threats.

## 2. Phishing Attacks

### 2.1 Definition and how phishing works

Phishing is a social engineering technique in which attackers impersonate legitimate organisations or individuals to trick victims into revealing sensitive information, clicking malicious links, downloading infected files or providing access to their accounts.

Phishing messages are commonly distributed through email, although attackers also use text messages, telephone calls and social media platforms. They may imitate banks, delivery companies, employers, universities or technology providers.

A typical phishing attack follows these steps:

1. The attacker selects a target and gathers information about the person or organisation.
2. A convincing message is created using the identity of a trusted organisation or individual.
3. The victim receives the message, which may contain an urgent request, suspicious link or attachment.
4. The victim follows the instructions, potentially entering login credentials or downloading malicious software.
5. The attacker uses the information or access obtained to compromise accounts, steal data or conduct further attacks.

Phishing messages frequently use psychological pressure. For example, a victim may be told that their bank account will be suspended unless they verify their details immediately. The intention is to make the person act before carefully checking whether the message is legitimate.

### 2.2 Types of phishing

**Spear phishing**

Spear phishing involves sending targeted phishing messages to specific individuals or organisations. Unlike ordinary phishing campaigns, these messages are personalised using information about the intended victim. Attackers may research an employee's job title, colleagues or responsibilities to make their communication appear genuine.

**Whaling**

Whaling is a specialised form of spear phishing that targets senior executives and other high-profile individuals. These individuals may have access to confidential business information, financial systems or important organisational decisions. Attackers often impersonate business partners, lawyers or senior employees.

**Vishing (Voice Phishing)**

Vishing involves using telephone calls or voice communications to deceive victims. An attacker may pretend to represent a bank, technical support department or government institution. The victim may be persuaded to disclose passwords, verification codes or personal information.

**Smishing (SMS Phishing)**

Smishing uses fraudulent text messages to trick victims into clicking malicious links, downloading applications or sharing confidential information. Messages may imitate banks, courier companies or service providers and often contain urgent instructions.

### 2.3 Real-world case study: RSA SecurID breach (2011)

One documented example of a spear-phishing attack occurred in March 2011, when RSA Security experienced a security breach involving information related to its SecurID authentication product.

According to public reporting by Computer Weekly, attackers sent two separate batches of targeted phishing emails to small groups of employees. The emails used the subject line "2011 Recruitment Plan" and included a malicious Excel spreadsheet attachment. One employee opened the attachment, which exploited an Adobe Flash vulnerability and installed malware on the employee's computer.

The attackers subsequently gained access to RSA's internal network and moved through the environment to obtain sensitive information associated with the SecurID product. The incident demonstrated how a seemingly ordinary recruitment-related email could become the starting point for a much larger security compromise.

The breach was particularly significant because RSA provided authentication technology used by other organisations. Compromising information associated with its security product created additional risks for customers who depended on that technology.

**Security lessons from the incident:**

- Employees should be cautious when opening unexpected email attachments, even when the subject appears relevant to their work.
- Security awareness must include all employees, not only senior management.
- Organisations should combine employee training with email filtering, endpoint protection and regular software updates.

Sources: Computer Weekly (2011); Ars Technica (2011).

### 2.4 Prevention recommendations

Organisations can reduce phishing risks through the following measures:

1. **Conduct regular security awareness training:** Employees should learn how to recognise suspicious senders, unusual requests, misleading links and unexpected attachments. Training should cover email, SMS and telephone-based phishing.

2. **Implement multi-factor authentication:** MFA provides an additional layer of account protection if a password is stolen. Organisations should prioritise phishing-resistant authentication methods, such as FIDO-based security keys or passkeys, where possible.

3. **Deploy email security controls:** Email filtering, attachment scanning, anti-malware protection and domain authentication technologies can help identify and block suspicious messages before they reach employees.

4. **Establish a clear reporting procedure:** Employees should have a simple way to report suspicious messages to the IT or cybersecurity department. Reported messages should be investigated promptly, and employees should know what to do if they have already clicked a suspicious link or disclosed information.

## 3. Pretexting Attacks

### 3.1 Definition and how pretexting works

Pretexting is a social engineering technique in which an attacker creates a false identity or believable scenario to gain the trust of a victim. The attacker uses this invented situation, known as a pretext, to persuade someone to disclose information, provide access or perform an action that would normally require authorisation.

Unlike phishing, which commonly relies on fraudulent messages and links, pretexting places greater emphasis on building a convincing story and establishing trust through interaction.

An attacker may pretend to be:

- An IT support technician investigating an employee's computer problem.
- A bank representative verifying suspicious transactions.
- A company manager requesting confidential documents.
- A supplier or contractor who needs access to an organisation's systems.
- A government official requesting personal information.

### 3.2 How attackers build a false scenario

Pretexting attacks generally involve several stages:

1. **Information gathering:** The attacker researches the organisation, its employees, job roles and communication procedures using publicly available information or other sources.

2. **Creating a believable identity:** The attacker chooses a role that would make the victim more likely to cooperate, such as an IT technician, manager or service provider.

3. **Establishing trust:** The attacker communicates confidently and uses organisational terminology or information that makes the story appear legitimate.

4. **Making a request:** The attacker asks the victim to disclose credentials, approve a login request, provide confidential information or grant access.

5. **Exploiting the information:** Once the victim cooperates, the attacker may use the information to access systems, impersonate employees or conduct further attacks.

The success of pretexting often depends on how convincingly the attacker can imitate normal organisational communication.

### 3.3 Real-world case study: Twitter social engineering incident (2020)

A well-known example of pretexting occurred during the Twitter security incident on 15 July 2020.

According to an investigation published by the New York State Department of Financial Services, attackers contacted several Twitter employees by telephone and pretended to work in the company's IT department. They claimed to be responding to VPN-related problems and used information about the employees and the organisation to make their stories believable.

The attackers persuaded employees to provide credentials through a fraudulent login process. This gave them access to internal systems and tools used to manage Twitter accounts.

The attackers subsequently compromised several high-profile Twitter accounts, including accounts belonging to politicians, business leaders and celebrities. These accounts were used to publish fraudulent cryptocurrency messages that encouraged people to send Bitcoin.

Twitter confirmed that the incident involved a phone-based spear-phishing attack targeting a small number of employees.

The incident demonstrates that attackers do not always need to exploit a technical vulnerability directly. By impersonating trusted IT personnel and taking advantage of normal workplace interactions, they can manipulate employees into providing access to important systems.

**Security lessons from the incident:**

- Employees should independently verify the identity of anyone requesting credentials or system access.
- IT support personnel should never request passwords or MFA codes from employees.
- Access to sensitive internal tools should be restricted according to job responsibilities.

Sources: Twitter (2020); New York State Department of Financial Services (2020).

### 3.4 Prevention measures

1. **Verify identities before sharing information:** Employees should confirm requests through official communication channels, particularly when someone requests passwords, confidential documents or access to internal systems.

2. **Introduce formal authorisation procedures:** Organisations should require additional approval for sensitive actions, such as resetting employee credentials, changing account permissions or transferring confidential information.

3. **Limit access privileges:** Employees should only have access to the systems and information necessary for their responsibilities. This reduces the damage an attacker can cause if an employee is deceived.

## 4. Baiting Attacks

### 4.1 Definition and how baiting works

Baiting is a social engineering technique in which attackers use an attractive offer, object or opportunity to encourage victims to perform an unsafe action. The attacker creates curiosity or excitement by offering something that appears valuable, useful or interesting.

Baiting can occur in both physical and digital environments. The main objective is to persuade the victim to interact with something that exposes their device, information or organisation to a security threat.

### 4.2 Types of baiting

**Physical baiting**

Physical baiting involves leaving infected or suspicious storage devices in locations where people are likely to find them. For example, an attacker may leave a USB flash drive in an office parking area, university computer laboratory or reception area.

The device may be labelled with an interesting description such as "Employee Salaries" or "Confidential Documents". A person who finds it may connect it to a computer out of curiosity or in an attempt to identify its owner.

If the device contains malicious files or exploits a device vulnerability, connecting it may expose the computer to malware or unauthorised access.

**Digital baiting**

Digital baiting involves using attractive online content to encourage victims to download malicious files or applications.

Examples include:

- Fake software downloads advertised as free premium applications.
- Fraudulent games or media files containing malware.
- Fake competitions promising prizes in exchange for personal information.
- Websites offering free documents or software that require victims to install suspicious programs.

The victim may believe they are receiving something useful, while the attacker uses the opportunity to distribute malware or collect sensitive information.

### 4.3 Case study: USB baiting experiment by Google researchers (2016)

A research study titled "Users Really Do Plug in USB Drives They Find", published by researchers including members of Google's security research community, examined how people respond to unknown USB storage devices.

During the controlled experiment, researchers distributed 297 USB flash drives across a university campus. The objective was to determine whether people would pick up and connect devices they found.

The study estimated that between 45% and 98% of the dropped drives were connected, demonstrating that this technique could be surprisingly effective. Some participants connected the devices because they wanted to identify the owner or return the storage device.

Although this experiment was not a criminal attack or a malware infection, it provided evidence of the human behaviour that makes USB baiting a security risk. In a real attack, a malicious USB device could expose an organisation to malware, information theft or other forms of compromise.

**Security lessons from the study:**

- Employees should never connect unknown USB devices to organisational computers.
- Organisations should establish procedures for handling unidentified storage devices.
- Technical restrictions should be used to prevent unauthorised removable media from accessing company systems.

Source: Tischer et al. (2016), *Users Really Do Plug in USB Drives They Find*.

### 4.4 Prevention measures

1. **Restrict removable storage devices:** Organisations should control the use of USB devices through endpoint security policies and device management tools. Only authorised storage devices should be permitted.

2. **Educate employees about suspicious offers:** Employees should be trained to avoid downloading software from untrusted websites or installing applications from unknown sources. Attractive offers should not be treated as proof that a download is safe.

3. **Use endpoint protection and application controls:** Antivirus software, endpoint detection tools and application allowlisting can help detect malicious files and prevent unauthorised programs from running.

## 5. Quid Pro Quo Attacks (Bonus)

### 5.1 Definition

Quid pro quo is a social engineering technique in which an attacker offers a service, benefit or reward in exchange for information or access. The phrase means "something for something". The attacker attempts to create a situation where the victim believes they are receiving assistance or a useful benefit.

For example, an attacker may contact an employee while pretending to provide technical support. They may offer to fix a computer problem in exchange for the employee's login credentials or remote access to their device.

Other examples include fraudulent technical support offers, fake rewards and requests to complete surveys in exchange for prizes.

### 5.2 How it works

A typical quid pro quo attack involves:

1. The attacker identifies a person who may need assistance or be interested in a particular benefit.
2. The attacker offers something that appears useful, such as technical support or a reward.
3. The victim is persuaded to provide information, access or another form of cooperation.
4. The attacker uses the information or access to compromise the victim or organisation.

### 5.3 Prevention measures

- Employees should use official support channels instead of accepting unexpected technical assistance.
- Organisations should establish procedures for verifying service providers and contractors.
- Employees should never exchange passwords, MFA codes or confidential information for promised services or rewards.

## 6. Comparison of Social Engineering Attacks

The following table summarises the main differences between the attacks discussed in this report.

| Attack type | Primary target | Psychological lever exploited | Best countermeasure |
|---|---|---|---|
| Phishing | Email and online account users | Urgency, fear and trust | Email filtering and employee awareness |
| Spear phishing | Selected employees or departments | Personal trust and familiarity | Identity verification and phishing-resistant MFA |
| Whaling | Senior executives and decision-makers | Authority and business pressure | Approval procedures for sensitive requests |
| Vishing | Individuals contacted by telephone | Trust and authority | Independent caller verification |
| Smishing | Mobile phone users | Urgency and curiosity | Avoid suspicious links and verify messages |
| Pretexting | Employees with access to information or systems | Trust and authority | Identity verification and access controls |
| Baiting | Employees and individuals using digital devices | Curiosity and reward | USB restrictions and application controls |
| Quid pro quo | Employees seeking assistance or benefits | Reciprocity and perceived obligation | Official support channels and verification |

## 7. Organisational Recommendations: Employee Security Awareness Training

Technical security controls are important, but employees also need to understand how their actions can affect organisational security. Organisations should introduce regular security awareness training that addresses the following five areas.

### 1. Recognising suspicious communications

Employees should be taught to identify suspicious emails, text messages and telephone calls. Training should include examples of impersonation, suspicious attachments, misleading links and requests for confidential information.

### 2. Verifying identities and requests

Employees should learn to confirm the identity of people requesting sensitive information or access. Verification should take place through official communication channels rather than relying on contact details supplied by the person making the request.

### 3. Safe handling of files and devices

Employees should understand the risks associated with unknown USB devices, unexpected attachments and software downloads from untrusted websites. Organisations should communicate clear rules for handling removable storage and installing applications.

### 4. Reporting security incidents

Employees should know how to report suspicious activity, phishing messages and possible security breaches. They should also understand that reporting an incident quickly is more important than hiding a mistake.

### 5. Regular training and security assessments

Security awareness should not be treated as a once-off activity. Organisations should provide refresher training, conduct controlled phishing simulations and review employee understanding. Training should be updated as new social engineering techniques emerge.

## 8. Conclusion

Social engineering remains a significant cybersecurity concern because it targets the people who interact with an organisation's systems and information. Phishing, pretexting and baiting use different methods, but they share the same objective: manipulating people into making decisions that benefit an attacker.

The RSA SecurID breach demonstrated how a targeted phishing email could become the starting point for a major security incident. The Twitter incident showed how impersonating IT personnel could result in unauthorised access to internal systems. The USB-drop experiment further demonstrated that curiosity and the desire to help can expose people to physical baiting techniques.

Based on these examples, three important recommendations can be made for organisations:

1. **Invest in employee awareness:** Employees should receive regular training so that they can recognise and respond appropriately to social engineering attempts.

2. **Establish strong verification procedures:** Sensitive requests should be independently verified, particularly when they involve credentials, financial transactions or access to organisational systems.

3. **Combine human awareness with technical controls:** Security training should be supported by MFA, access restrictions, endpoint protection, email filtering and clear incident reporting procedures.

Ultimately, cybersecurity is not only the responsibility of the IT department. Every employee has a role in protecting organisational information, and a strong security culture can significantly reduce the opportunities available to social engineers.

## 9. References

1. Cybersecurity and Infrastructure Security Agency (CISA). (2021). *Phishing General Security Postcard*. Available at: https://www.cisa.gov/sites/default/files/publications/Phishing%20General%20Security%20Postcard_6.24.2021_508c.pdf

2. CISA. (2022). *Implementing Phishing-Resistant Multi-Factor Authentication*. Available at: https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf

3. SANS Institute. Gragg, D. (2003). *A Multi-Level Defense Against Social Engineering*. SANS Reading Room. Available at: https://www.sans.org/white-papers/920

4. Computer Weekly. (2011). *RSA discloses phishing-attack data breach details*. Available at: https://www.computerweekly.com/news/1280095593/RSA-discloses-phishing-attack-data-breach-details

5. Twitter. (2020). *An update on our security incident*. Available at: https://blog.x.com/en/company/an-update-on-our-security-incident

6. New York State Department of Financial Services. (2020). *Twitter Investigation Report*. Available at: https://www.dfs.ny.gov/reports-and-publications/other-reports/Twitter_Report

7. Tischer, M., Durumeric, Z., Foster, S., Duan, S., Mori, A., and Bursztein, E. (2016). *Users Really Do Plug in USB Drives They Find*. IEEE Security and Privacy. Available at: https://research.google/pubs/users-really-do-plug-in-usb-drives-they-find/

8. National Institute of Standards and Technology (NIST). (2021, updated 2026). *Phishing*. Available at: https://www.nist.gov/itl/smallbusinesscyber/guidance-topic/phishing

