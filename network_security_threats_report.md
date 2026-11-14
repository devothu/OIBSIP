^O
# Common Network Security Threats: Research Report

**Internship:** OIBSIP Cybersecurity Internship  
**Task:** Task 4 – Research Report  
**Topic:** Common Network Security Threats  
**Author:** Othusitse  
**Tools:** Markdown, GitHub, NIST, CISA, MITRE ATT&CK and security research publications

---

## 1. Introduction

Network security is essential in today's digital environment because organisations depend on interconnected systems to communicate, store information and provide online services. As networks become increasingly connected, they also become attractive targets for cybercriminals seeking to disrupt operations, steal sensitive information or gain unauthorised access. Network security threats can affect individuals, businesses, government institutions and critical infrastructure. Attacks such as Distributed Denial-of-Service (DDoS), Man-in-the-Middle (MITM), IP spoofing and DNS poisoning can compromise the confidentiality, integrity and availability of network resources. Understanding how these attacks operate, their potential consequences and the appropriate mitigation strategies is important for network administrators and cybersecurity professionals.

## 2. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) Attacks

### 2.1 Explanation and how the attack works

A Denial-of-Service (DoS) attack attempts to make a computer system, website or network service unavailable to legitimate users by overwhelming its resources or exploiting weaknesses in its operation.

A Distributed Denial-of-Service (DDoS) attack uses multiple compromised devices, commonly organised into a botnet, to send large volumes of traffic or requests towards a target simultaneously.

Common DDoS techniques include:

- **Volumetric attacks:** Consume available network bandwidth through excessive traffic.
- **Protocol attacks:** Exploit weaknesses in network protocols or connection handling to exhaust network resources.
- **Application-layer attacks:** Flood applications with requests that consume processing power, memory or database resources.

In a typical DDoS attack, an attacker controls or coordinates multiple devices that generate malicious traffic towards a target. The resulting traffic can overwhelm the target's network infrastructure, servers or applications, preventing legitimate users from accessing services.

### 2.2 Real-world example: Mirai botnet attacks (2016)

In September 2016, the Mirai botnet launched a major DDoS attack against the cybersecurity website KrebsOnSecurity. The attack generated exceptionally high volumes of traffic and disrupted access to the website.

In October 2016, another Mirai-related attack targeted Dyn, a major Domain Name System (DNS) service provider. Because many popular websites depended on Dyn's DNS services, the disruption affected access to several well-known online platforms.

The incident demonstrated how compromised Internet-connected devices, including routers and other IoT equipment, can be used collectively to disrupt major online services.

**Sources:** CISA's Understanding and Responding to DDoS Attacks; Congressional Research Service reporting on the 2016 Mirai attacks.

### 2.3 Impact

DDoS attacks can have serious consequences, including:

- **Service disruption:** Websites, applications and online services become unavailable.
- **Financial losses:** Organisations may lose revenue during periods of downtime.
- **Reputational damage:** Customers may lose confidence in an organisation that cannot maintain reliable services.
- **Operational disruption:** Employees and customers may be unable to access essential systems.
- **Recovery costs:** Organisations may incur additional expenses for incident response and infrastructure improvements.

### 2.4 Mitigation strategies

1. **Deploy DDoS protection services:** Use reputable DDoS mitigation providers, Content Delivery Networks (CDNs) and Web Application Firewalls (WAFs) to detect and filter malicious traffic before it overwhelms infrastructure.

2. **Implement traffic monitoring and rate limiting:** Monitor unusual traffic patterns, configure rate limits and apply appropriate filtering rules to reduce the impact of excessive requests.

3. **Develop an incident response and resilience plan:** Work with Internet Service Providers (ISPs), maintain sufficient network capacity, prepare failover arrangements and establish procedures for responding to attacks.

---

## 3. Man-in-the-Middle (MITM) Attacks

### 3.1 Explanation and how the attack works

A Man-in-the-Middle (MITM) attack occurs when an attacker secretly positions themselves between two communicating parties to intercept, monitor or manipulate information exchanged between them.

The attacker attempts to make both parties believe they are communicating directly with one another, while the attacker can observe or potentially modify the communication.

Common MITM techniques include:

- **ARP spoofing:** Manipulating Address Resolution Protocol information to redirect traffic through an attacker-controlled device.
- **Rogue Wi-Fi access points:** Creating fraudulent wireless networks that imitate legitimate networks.
- **DNS manipulation:** Redirecting users to attacker-controlled destinations.
- **Session hijacking:** Taking advantage of stolen session cookies or authentication tokens.

MITM attacks are particularly dangerous when communications are not properly encrypted or when users accept invalid digital certificates.

### 3.2 Real-world example: DigiNotar certificate authority breach (2011)

In 2011, the Dutch certificate authority DigiNotar was compromised. Attackers issued fraudulent digital certificates for several high-profile websites, including a fraudulent certificate for Google.

The fraudulent certificates could be used to impersonate legitimate websites and enable Man-in-the-Middle attacks.

Microsoft issued a security advisory warning that fraudulent certificates could allow spoofing, phishing and MITM attacks. The incident demonstrated the importance of trusted certificate authorities and secure digital certificate management.

**Sources:** Microsoft Security Advisory 2607712; Fox-IT's DigiNotar investigation report.

### 3.3 Impact

MITM attacks can result in:

- **Credential theft:** Usernames, passwords and authentication information may be intercepted.
- **Financial fraud:** Attackers may capture sensitive financial information or manipulate transactions.
- **Privacy violations:** Private communications and personal information may be exposed.
- **Data manipulation:** Information exchanged between communicating systems may be altered.
- **Unauthorised access:** Stolen session tokens or credentials may allow attackers to access protected systems.

### 3.4 Mitigation strategies

1. **Use HTTPS and strong TLS encryption:** Ensure websites and applications use valid TLS certificates and reject invalid or expired certificates. Disable outdated and insecure encryption protocols.

2. **Secure wireless networks:** Use WPA2-AES or WPA3 encryption, avoid connecting to suspicious public Wi-Fi networks and verify the identity of wireless access points.

3. **Implement network protection and authentication controls:** Use VPNs where appropriate, enable multi-factor authentication (MFA), secure session cookies and monitor networks for suspicious ARP or DNS behaviour.

---

## 4. IP Spoofing

### 4.1 Explanation and how the attack works

IP spoofing is a technique in which an attacker modifies the source IP address in an Internet Protocol packet to make it appear as though the packet originated from another device or network.

The source IP address is normally used by receiving systems to identify where network traffic originated. By forging this address, attackers can conceal the actual source of traffic, impersonate other systems or direct responses towards an unintended destination.

IP spoofing is commonly associated with:

- **Reflection attacks:** Attackers send requests to third-party servers using a forged source IP address belonging to the intended victim.
- **Amplification attacks:** The third-party servers send responses that may be significantly larger than the original requests.
- **Network impersonation:** Forged packets are used to make traffic appear to originate from a trusted or authorised address.

IP spoofing is generally more effective against connectionless protocols such as UDP because these do not require the same connection-establishment process as TCP.

### 4.2 Real-world example: Spamhaus DDoS attack (2013)

In March 2013, Spamhaus, an organisation involved in combating email spam, experienced a major DDoS attack.

The attackers used DNS reflection and amplification techniques involving open DNS resolvers. They sent DNS requests containing forged source IP addresses associated with the victim.

The DNS servers responded to the forged addresses rather than the actual attackers. This caused large volumes of DNS response traffic to be directed towards Spamhaus.

Reports of the incident described traffic reaching approximately 300 Gbps.

The attack demonstrated how IP spoofing can be combined with reflection and amplification to generate substantial network disruption.

**Sources:** Cloudflare's 2013 Spamhaus incident analysis; ICANN's advisory on amplified DDoS attacks; IETF RFC 2827 (BCP 38).

### 4.3 Impact

IP spoofing can contribute to several security problems:

- **Source concealment:** Makes it more difficult to identify the actual origin of malicious traffic.
- **DDoS attacks:** Allows attackers to direct reflected traffic towards a victim.
- **Trust exploitation:** Can undermine systems that rely only on source IP addresses for authentication or access decisions.
- **Network disruption:** Can contribute to traffic congestion and service outages.
- **Investigation difficulties:** Forged source addresses can complicate incident investigation and traffic attribution.

An important limitation is that IP spoofing alone does not automatically allow an attacker to receive traffic sent back to the forged address or bypass every network authentication mechanism.

### 4.4 Mitigation strategies

1. **Implement ingress and egress filtering:** Apply network filtering rules that prevent packets with invalid or unexpected source addresses from entering or leaving the network. Follow the principles described in IETF BCP 38 and BCP 84.

2. **Use network firewalls and access control lists (ACLs):** Configure routers and firewalls to reject suspicious packets and restrict traffic that does not match expected network communication patterns.

3. **Deploy network monitoring and anti-DDoS protection:** Monitor abnormal traffic volumes, identify spoofed traffic patterns and work with ISPs to reduce reflection and amplification attacks.

---

## 5. DNS Poisoning and DNS Spoofing

### 5.1 Explanation and how the attack works

The Domain Name System (DNS) translates human-readable domain names into IP addresses that computers use to communicate across networks.

DNS poisoning, also known as DNS cache poisoning, occurs when an attacker introduces false DNS information into a DNS resolver's cache. As a result, users may be directed to an incorrect or malicious IP address when attempting to access a legitimate domain.

DNS spoofing refers more broadly to the use of forged DNS responses or information to mislead a system about the correct destination of a domain name.

A typical DNS cache poisoning attack may involve:

1. A user or system requests the IP address associated with a domain name.
2. The attacker's objective is to cause a DNS resolver to accept a fraudulent response.
3. The resolver stores the incorrect DNS information in its cache.
4. Other users relying on the affected resolver may be directed to an attacker-controlled website.

DNS poisoning can be used for phishing, credential theft, malware distribution and traffic redirection.

### 5.2 Real-world example: Kaminsky DNS vulnerability (2008)

In 2008, security researcher Dan Kaminsky disclosed a significant DNS cache-poisoning weakness affecting DNS implementations.

The vulnerability involved weaknesses in DNS transaction ID predictability and insufficient randomness in DNS query source ports. Attackers could exploit these weaknesses to increase the likelihood that forged DNS responses would be accepted by vulnerable caching resolvers.

The United States Computer Emergency Readiness Team (US-CERT) issued an advisory explaining the vulnerability and recommending that administrators update affected DNS software.

The incident highlighted the importance of DNS security, software patching, source-port randomisation and DNS Security Extensions (DNSSEC).

**Sources:** US-CERT Vulnerability Note VU#800113; Internet Systems Consortium's technical guidance on CVE-2008-1447; SANS Internet Storm Center.

### 5.3 Impact

DNS poisoning can cause:

- **Phishing:** Users may be redirected to fraudulent websites that imitate legitimate services.
- **Credential theft:** Attackers may capture usernames, passwords and other sensitive information.
- **Malware distribution:** Victims may be directed to malicious websites that distribute harmful software.
- **Service disruption:** Users may be unable to reach legitimate online services.
- **Loss of trust:** Organisations may experience reputational damage if their domains or DNS infrastructure are compromised.

### 5.4 Mitigation strategies

1. **Implement DNSSEC:** Deploy DNS Security Extensions to validate the authenticity and integrity of DNS data. DNSSEC helps resolvers detect forged or altered DNS responses when properly configured and validated.

2. **Update and secure DNS infrastructure:** Regularly patch DNS server software, enable strong source-port and transaction-ID randomisation, restrict unnecessary DNS recursion and monitor DNS server configurations.

3. **Monitor DNS activity and protect DNS administration:** Monitor unusual DNS responses, review DNS records regularly, restrict access to DNS management systems and enable multi-factor authentication for administrative accounts.

---

## 6. Comparison of Common Network Security Threats

The following table summarises the four threats and compares their attack methods, potential targets, execution difficulty and mitigation considerations.

| Threat | Attack vector | Who is at risk? | Difficulty to execute | Ease of mitigation |
|---|---|---|---|---|
| DoS/DDoS | Excessive traffic, botnets, protocol exploitation and resource exhaustion | Websites, businesses, hosting providers and online services | Medium to High, depending on attack scale and resources | Medium – requires traffic filtering, upstream protection and response planning |
| MITM | Traffic interception, ARP spoofing, rogue Wi-Fi and certificate abuse | Individuals, businesses and users of insecure networks | Medium to High, depending on network access and security controls | Medium – encryption, certificate validation and network security reduce risk |
| IP Spoofing | Forged source IP addresses in network packets | Network operators, service providers and organisations exposed to reflection attacks | Low to Medium for basic spoofing; more difficult for complex attacks | Medium to High – ingress/egress filtering and anti-spoofing controls are effective when widely implemented |
| DNS Poisoning/Spoofing | Forged DNS responses, compromised DNS infrastructure or manipulated DNS settings | DNS providers, organisations and Internet users | Medium to High, depending on the targeted DNS infrastructure | Medium – DNSSEC, patching, access controls and monitoring reduce risk |

**Note:** Difficulty and mitigation ratings are qualitative estimates for general network environments. Actual risk depends on the attacker's capabilities, network architecture, existing security controls and the target's exposure.

---

## 7. Conclusion: Three Key Takeaways for Network Administrators

Network security threats continue to evolve, making it essential for network administrators to understand common attack techniques and implement effective security controls. The research demonstrates that attacks such as DDoS, MITM, IP spoofing and DNS poisoning can affect the availability, confidentiality and integrity of network resources.

Three key takeaways for network administrators are:

1. **Prioritise preventive security controls:** Implement strong encryption, secure network configurations, DNSSEC, anti-spoofing filters, firewalls and appropriate access controls to reduce the likelihood of successful attacks.

2. **Monitor networks continuously:** Regularly analyse network traffic, DNS activity, server logs and security alerts to identify unusual behaviour and respond to suspicious activity before it causes significant damage.

3. **Prepare for incidents and maintain resilience:** Develop incident response procedures, maintain reliable backups, work with service providers and regularly review security policies to ensure that essential network services remain available.

Ultimately, effective network security requires a combination of prevention, monitoring, preparedness and continuous improvement.

---

## 8. References

1. **Cybersecurity and Infrastructure Security Agency (CISA), FBI and MS-ISAC.** (2022). *Understanding and Responding to Distributed Denial-of-Service Attacks.*  
   https://www.cisa.gov/resources-tools/resources/understanding-and-responding-distributed-denial-service-attacks

2. **Congressional Research Service.** (2016). *Cybersecurity: Distributed Denial of Service (DDoS) Attacks.*  
   https://www.everycrsreport.com/reports/IN10600.html

3. **MITRE ATT&CK.** *Adversary-in-the-Middle (T1557).*  
   https://attack.mitre.org/techniques/T1557/

4. **Microsoft.** (2011). *Security Advisory 2607712: Fraudulent Digital Certificates Could Allow Spoofing.*  
   https://learn.microsoft.com/en-us/security-updates/securityadvisories/2011/2607712

5. **Fox-IT.** (2011). *DigiNotar Certificate Authority Breach – Operation Black Tulip.*  
   https://www.sec.gov/Archives/edgar/data/1044777/000119312511241796/dex992.htm

6. **Internet Engineering Task Force (IETF).** (2000). *RFC 2827: Network Ingress Filtering – Defeating Denial of Service Attacks Which Employ IP Source Address Spoofing.*  
   https://www.rfc-editor.org/rfc/rfc2827

7. **Cloudflare.** (2013). *The DDoS That Knocked Spamhaus Offline (And How We Mitigated It).*  
   https://blog.cloudflare.com/the-ddos-that-knocked-spamhaus-offline-and-ho/

8. **National Institute of Standards and Technology (NIST).** (2026). *SP 800-81 Rev. 3: Secure Domain Name System (DNS) Deployment Guide.*  
   https://csrc.nist.gov/pubs/sp/800/81/r3/final

9. **United States Computer Emergency Readiness Team (US-CERT).** (2008). *Vulnerability Note VU#800113: Multiple DNS Implementations Vulnerable to Cache Poisoning.*  
   https://kb.cert.org/vuls/id/800113/

10. **Internet Systems Consortium (ISC).** *CVE-2008-1447: DNS Cache Poisoning Issue (Kaminsky Bug).*  
    https://kb.isc.org/docs/aa-00924

11. **SANS Internet Storm Center.** (2005). *DNS Poisoning – March 2005 DNS Poisoning Summary.*  
    https://isc.sans.edu/presentations/dnspoisoning.html


