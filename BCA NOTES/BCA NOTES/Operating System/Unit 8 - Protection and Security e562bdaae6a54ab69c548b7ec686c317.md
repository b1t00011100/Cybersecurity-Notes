# Unit 8 - Protection and Security

## Introduction

- Cyber Crime has led to a height-ened awareness of the need to protect data and resources from disclosure, to guarantee the authenticity of data and messages, and to protect systems from network based attacks.
- The discipline of cryptography and computer security have matured, leading to the development of practical, readily available application to enforce security.

### Computer Security Concepts

- **CIA Triad : C**onfidentiality, **I**ntegrity & **A**vailability.
    - **Confidentiality** : Assures that private or confidentail information is not made available or disclosed to unauthorized individuals.
    - **Integrity :** Assures that information and programs are changed only in a specific authorized manner.
    - **Availability :** Assures that systems work promptly and service is not denied to authorized users.
- Some additional concepts :
    - **Authenticity : V**erifying that users are who they say they are and that each input arriving at
    the system came from a trusted source.
    - **Accountability :** The security goal that generates the requirement for actions of an
    entity to be traced uniquely to that entity.

### Threats & Attacks

- Based on RFC 2828, describes four kinds of threat consequences and lists the kinds of attacks that result in each consequence :
    - **Exposure :** This can be delibrate, when an insider releases sensitive data such as credit card numbers, to an outsider. This can be human error as well as software error.
        - For ex: Univerities leaking students confidential data.
    - **Interception :** Interception is a common attack in the context of communication. On a LAN, such as a wireless LAN or a broadcast Ethernet, any devices attached to the lan can receive a copy of  packets intended for another device.
        - For ex : On the Internet, a determined hacker can gain access to email traffic and other data transfers.
    - **Inference :** An example of inference is known as traffic analysis, in which an adversary is able to gain information from observing the pattern or traffic on a network, such as amount of traffic between particulars pairs of hosts on the network.
    - **Intrusion :** An example of intrusion is an adversary gaining unauthorized access to sensitive data by overcoming the system’s control protections.
- Deception is a threat to either system integrity or data integrity.
    - Attacks that can result in this threat consequence :
    1. **Masquerade** : One example of masquerade is an attempt by an unauthorized user to gain access to a system by posing as an authorized user; this could happen if the unauthorized user has learned another user‘s logon ID and password. Another example is malicious logic, such as a Trojan horse, that appears to perform a useful or desirable function but actually gains unauthorized access to system resources or tricks a user into executing other malicious logic.

### Threats and Assests

- The asset of computer can be categorized as hardware, software, data and communication lines and networks.
    - **Hardware :** A major threat to computer system hardware is the threat to availability. Hardware is the most vulnerable to attack and the least susceptible to automated controls. Threats include accidental and delibrate damamge to equipment as well as theft.
    - **Software :** Software includes the operating system, utilities, and application programs. A key threat to software is an attack on availability. Software, especially application software, is often easy to delete. Software can also be altered or damaged to render it useless. Careful software configuration management, which includes making backups of the most recent version of software, can maintain high availability.