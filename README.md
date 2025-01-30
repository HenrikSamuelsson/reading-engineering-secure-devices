# Reading Engineering Secure Devices

Notes on the book Engineering Secure Devices, Dominik Merli, No Starch Press (2024).

## Platform

The book includes a practical case study based on the [STM32MP157F-DK2](https://www.st.com/en/evaluation-tools/stm32mp157f-dk2.html) evaluation board from ST, and ST's [OpenSTLinux distribution](https://wiki.st.com/stm32mpu/wiki/Category:OpenSTLinux_distribution) with a Linux 5.15 kernel.

## Secure Development Process

Development shall follow best practices to ensure security .Security Development Lifecycle (SDL) practices. There is no need to start from scratch, a starting point to setup a SDL can be to look at one of the following resources:
- Security Development Lifecycle (SDL) practices at [Microsoft](https://www.microsoft.com/en-us/securityengineering/sdl/practices?oneroute=true)
- Software Assurance Maturity Model (SAMM) provided by [OWASP](https://owaspsamm.org/model/) 
- The [ISA/IEC 62443 Series of Standards](https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards) with requirements and processes for secure industrial automation and control systems (IACS)

## Kerckhoffs's Principle

Kerckhoffs Principle states that the security of a crypto system must lie in the choice of its keys only; everything else such as encryption, decryption, and signing, should be considered public knowledge.

## Symmetric Cryptography

Cryptography is based on transforming a plain text to a incomprehensible cipher text, encryption. And then reverse the cipher text back to the plain text, decryption. The benefit of having the cipher text is that we can share this with the world and still keep the plain text secret. 

The encryption and decryption requires knowledge of a secret known as the key. There are a class of cryptography schemes that uses the same key to encrypt and decrypt, symmetric cryptography.  

```text
encrypt(plain text, key) : cipher text
decrypt(cipher text, text) : plain text
```

## Abbreviations

List of abbreviations used in the book.

*A* - availability  
*An* - anonymity  
*Au* - authenticity  

*BOM* - bill of materials  
*BSIMM* - Building Security In Maturity Model  

*C* - confidentiality  
*CI* - continuous integration  
*CIA* - confidentiality integrity availability  
*CMOS* - complementary metal-oxide semiconductor  
*CRA* - Cyber Resilience Act  
*CRC* - cyclic redundancy check  
*CSA* - Cybersecurity Act  
*CTO* - Chief Technical Officer  
*CVEs* - common vulnerabilities and exposures   

*DAST* - dynamic application security testing  
*DoS* - denial of service  
*DDoS* - distributed DoS  
*DRBG* - deterministic random bit generators  

*ENISA* - European Union for Agency for Cybersecurity  

*GDPR* - General Data Protection Regulation  

*I* - Integrity  
*IC* - Integrated Circuit  
*IACS* - industrial automation and control systems  
*ICS* - industrial control systems  
*IEC* - International Electrotechnical Commission  
*IIoT* - industrial IoT  
*IoT* - internet of things  

*MAC* - message authentication code  
*MIC* - message integrity code  

*NIST* - National Institute of Standards and Technology  
*Nr* - non-repudiation  
*NRBG* - nondeterministic random bit generator  

*OT* - operational technology  
*OS* - operating system  
*OWASP* - Open Web Application Security Project  

*PCB* - printed circuit board  
*Pr* - privacy  
*Ps* - pseudonymity  
*PSA* - Platform Security Architecture  
*PSO* - Product Security Officer  

*RNG* - random number generator  
*RO* - ring oscillator  

*SAST* - static application security testing  
*SBOM* - software bill of materials  
*SDL* - secure development life cycle  
*SE* - secure element  
*SSH* - secure shell  
*STRIDE* - spoofing tampering repudiation information  disclosure denial of service elevation of privilege  

*TRNG* - true RNG  

## Terms

List of terms defined in the book.

*Amnesia:33* - set of thirty-three memory vulnerabilities affecting IoT devices

*attack vector* - Path or method used to attack a system, with intention to gain unprivileged access to a system asset

*brute force attack* - Systematic attack where each possible secret key is tried one by one in order

*cipher* - an algorithm for performing encryption or decryption

*denial of service* - a way to interrupt a service

*elevation of privilege* a way to act without permission

*embedded system* - an electronic system including a processing unit, memory, and input/output interfaces that are embedded within a larger mechanical or electronic system

*entropy* - Measure of unpredictability, system with high disorder will have high entropy

*information disclosure* - a way to extract information

*insecurity by design* - term coined when analyzing products that showed to have missed event the most basic security controls

*Mirai* - malware that exploited IoT devices, turning them into botnets

*pseudo randomness* - Output that appear random but in reality is completely deterministic, and don't contain an entropy sources

*repudiation* - plausibility to deny an action 

*ring oscillator* - electronic circuit used to generate noise to be used for random number generation

*Ripple20* - set of vulnerabilities in a software library that implements a TCP/IP stack

*search space* - The number of tries an attacker have to make to break the security algorithm, related to security level, 128 bits security level means 2^128 tries

*security by obscurity* - a security anti pattern based on having security by hiding details about a systems with intention to enhance security

*security level* Property of a cryptographic algorithm indicated by a certain bit length, 64-bit, 128-bit, and so on

*spoofing* - impersonate an entity

*Stuxnet* - computer worm that reportedly destroyed almost one-fifth of Iran's nuclear centrifuges

*tampering* - manipulation of data

*threat actor* - Person attacking a system with intention to penetrate the security

*threat modeling* - The process of using hypothetical scenarios, system diagrams, and testing to help secure systems and data.

*threat scenario* - Description of a possible way to attack a system, by exploiting a vulnerability, with intention to gain access to or prevent usage of an asset being an vital part of the system. 

*true randomness* - Output that is totally unpredictable, without any pattern

*vulnerability* - An exploitable weakness of a system, that can be used by an attacker to gain unprivileged access to a system asset.
