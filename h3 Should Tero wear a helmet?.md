# Table of contents
- Braiterman et al 2020
- Shostack 2022
- Shostack 2014
- OWASP CheatSheets Series Team 2021
- Security hygiene
- Make-belief boogie-man - a threat model for imaginary company.

# Braiterman et al 2020

> https://www.threatmodelingmanifesto.org/

- Threat modelling is like examining a system to find privacy and security problems.
- Everyone should do it.
- We can use the Threat Modelling Manifesto to create our own way of doing it.
- The Manifesto has values (which are the important things) and principles (which are the basic truths) to guide us.
- **Values:** are about finding and fixing issues, understanding and working together.
- **Principles:** are there to tell us to analyze to make things more secure and adapt as the system changes.
- Good patterns help threat modelling, like having a plan, considering different perspectives, having useful tools, and turning theory into practice. 
- Bad patterns hurt threat modelling, like getting too stuck on problems, focusing too much, and aiming for perfection.

# Shostack 2022

> https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf

This is a short course about threat modelling, which is like thinking about how to keep things safe from bad stuff. Here are the main points:

1. **Introduction**: This course is about threat modelling, and it's really short.

2. **Why Threat Model**: You do this to think about security before making anything (like code or components) to make sure it's safe.

3. **Four Questions**: four questions to answer in threat modelling: What are we working on? What can go wrong? What can we do better? Did we do a good job? 

4. **Collaboration**: Working together is important.

5. **Sketching**: Drawing helps put ideas into a form that others can understand. It's useful for answering the question "What can go wrong?"

6. **Record Your Work**: Make a document with drawings. This helps you learn more about the system and add details.

7. **Data Flow Diagrams**: Threats often follow data. Diagrams with elements like external entities, processes, data flows, storage, and trust boundaries can help you understand the system.

8. **What Can Go Wrong**: STRIDE is a tool to help think about possible problems.

9. **Introducing STRIDE**: STRIDE is a way to structure thinking about what can go wrong. It stands for Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, and Elevation of privilege.

10. **What to Do About It**: If you find threats, you need to do something about them. You must not ignore them.

11. **Risk Management**: This is about dealing with some of the threats you find. Threat modelling helps inform risk management.

12. **Did We Do a Good Job**: Ask yourself if you would recommend threat modelling to a colleague. 

# Shostack 2014

> https://learning.oreilly.com/library/view/threat-modeling-designing/9781118810057/9781118810057c01.xhtml#c1

**Chapter 1 - Dive In and Threat Model:**

- Threat modeling is about using models to find security problems.
- Anticipate the threats that could affect you.
- Practice is essential to understand threat modeling.

**What Are You Building:**

- Diagrams are useful for communicating information about software systems.
- Consider security and control early when making system diagrams.
- Define "who controls what" for better understanding.
- Focus on identifying threats after creating the diagram.

**What Can Go Wrong:**

- Use techniques like "Elevation of Privilege" and the "STRIDE Mnemonic" to identify security issues.
  - Spoofing : Pretending to be someone else.
  - Tampering : Unauthorized modification of data.
  - Repudiation : Denying actions, whether true or false.
  - Denial of Service : Disrupting system availability.
  - Information Disclosure : Unauthorized exposure of data.
  - Elevation of Privilege : Unauthorized access to perform actions.

- Address threats with actions like mitigating, eliminating, transferring, or accepting them.

**Addressing Each Threat:**

- Different strategies are needed for addressing specific threats like STRIDE.
- Validate input, don't just sanitize it.
- Trust the operating system's security features but complement them with proper configuration and coding.
- Treat each identified threat as a bug in your software and prioritize them.
- Validate the threat model by checking the model, updating the diagram, and checking each threat.
- Develop tests for each addressed threat to detect potential problems or vulnerabilities.

# OWASP CheatSheets Series Team 2021

> https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html.

**Introduction:**

- Threat modeling helps create models for existing and new systems.
- Key steps include documenting data flow, identifying threats, and documenting security controls.

**Threat Modeling Terminology:**

- Understand terms like threat agent, impact, likelihood, controls, preventions, mitigations, data flow diagram, and trust boundary.

**Getting Started:**

- Define business objectives and security requirements.
- Create data flow diagrams to visualize system architecture.
- Use design documents, such as the 4+1 view model, to document the system.
- Understand how the system interacts with its ecosystem and create flow diagrams.
- Define and evaluate assets, considering data in transit and at rest.
- Define trust boundaries, user roles, trust levels, and authorization.

**Identify Threat Agents:**

- Define all possible threats by understanding threat agents, means, motive, and opportunities.
- Map threat agents to application entry points.
- Map abuse cases to use cases to identify logical threats.
- Re-define attack vectors considering compromised user roles.

**Write your Threat traceability matrix:**

- Define the impact and probability for each threat.
- Use methodologies like DREAD or PASTA to evaluate risks.
  - **D**amage - how bad would an attack be?
  - **R**eproducibility - how easy it is to reproduce the attack?
  - **E**xploitability - how much work is it to launch the attack?
  - **A**ffected users - how many people will be impacted?
  - **D**iscoverability - how easy it is to discover the threat?

- Rank risks based on severity.
- Determine countermeasures and mitigation.
- Identify risk owners and agree on risk mitigation with stakeholders.
- Build a risk treatment strategy: reduce, transfer, avoid, or accept risks.
- Select appropriate controls to mitigate risks.
- Test risk treatments to verify remediation.
- Reduce risk in the risk log for verified treated risks.
- Periodically retest risks to adapt to changing threats.

# Security hygiene

## Basic Security Practices for Everyone

- **Strong Passwords**: Use strong and unique passwords.
- **Multi-Factor Authentication (MFA)**: Add an extra layer of security.
- **Software Updates**: Keep your system and apps up-to-date.
- **Antivirus and Anti-Malware**: Install reputable security software.
- **Firewall**: Enable your computer's built-in firewall.
- **Secure Browsing**: Use secure websites (HTTPS) and privacy-focused browser extensions.
- **Data Backup**: Regularly back up important data.
- **Physical Security**: Lock your devices and be cautious in public places.

## Security Practices for Advanced Users

- **Network Segmentation**: Separate devices with different security needs.
- **VPN**: Encrypt your internet connection, especially on public Wi-Fi.
- **Secure Messaging**: Use encrypted messaging apps for sensitive communication.
- **Password Rotation**: Change passwords periodically.

# Make-belief boogie-man - a threat model for imaginary company.

Foodie Delights Inc. is an imaginary company that specializes in producing artisanal and gourmet food products. With a passion for quality and a commitment to food safety, they have gained a loyal customer base. 

## **(1) What are we working on?**

### Our Assets:

- Customer databases with personal information and purchase histories.
- Proprietary recipes and production processes.
- Inventory and supply chain data.
- Online storefront and e-commerce platform.
- Production and quality control systems.
- Employee data and payroll systems.

#### Prioritization of Key Assets:

Foodie Delights Inc. recognizes that customer health data, especially allergies and dietary restrictions, is a crown jewel asset. Protecting this data is critical as it not only impacts the customer but also the reputation of the company. Additionally, the proprietary recipes and production processes are highly valuable, as they are the core of the company's competitive advantage.

### Security Supports Business:

In the food industry, trust and reputation are important. Security is not just a technical requirement but an integral part of the business strategy. A security breach could lead to regulatory fines, and severe reputational damage.

### **Diagram of Company Systems:**

<img width="351" alt="image" src="https://github.com/piafernandez/h3-Should-Tero-wear-a-helmet-/assets/71267247/dfe6ec41-c968-4520-a592-08d01bb3d669">


**Description:**

1. **Customer Database:** This is where customer health data, including allergies and dietary restrictions, is securely stored.

2. **E-commerce Platform:** The online storefront and e-commerce platform where customers place orders, interact with the company, and make purchases.

3. **Production Systems:** Systems related to food production, including proprietary recipes, quality control, and production processes.

4. **Inventory & Supply Chain Management:** Manages the company's inventory, tracks supply chain data.

5. **Quality Control & Production:** Responsible for maintaining product quality, including quality control processes and production management.

6. **HR System:** Manages employee data, including personnel records and payroll information.

## **(2) What can go wrong?**

### STRIDE

> To assess potential threats, Foodie Delights Inc. employs the STRIDE model.

Spoofing: Unauthorized access to customer data or production systems through impersonation.

- A hacker could spoof their identity to gain access to the customer database and steal personal information.

Tampering: Unauthorized modification of recipes, production processes, or customer orders.

- Tampering with recipes could lead to contaminated products and health risks.

Repudiation: Disputes arising from altered orders or unauthorized actions within the system.

- Repudiation could occur if an employee alters an order, leading to customer complaints.

Information Disclosure: Exposure of customer health data or proprietary recipes.

- Unauthorized disclosure of proprietary recipes could result in competitors replicating Foodie Delights' products.

Denial of Service: Attacks on the e-commerce platform or production systems that disrupt operations.

- A distributed denial-of-service (DDoS) attack on the e-commerce platform could disrupt online sales.

Elevation of Privilege: Unauthorized access leading to privileges within the systems.

- An insider threat could lead to an employee elevating their privileges to access sensitive data.

### Prioritized Risks:

1. Unauthorized access to customer health data due to its sensitivity.

   - Probability: Let's assign a probability of 0.7 (70%) as this type of breach is moderately likely.

   - Monetary Value: A conservative estimate of the potential monetary loss from a breach could be 1,000,000 euros.
   - Expected Value: Expected Value = Probability (0.7) * Monetary Value 1,000,000 = 700,000 euros

2. Tampering with proprietary recipes, which could affect product quality and reputation.

   - Probability: Assign a probability of 0.4 (40%) as insider threats and cyberattacks targeting intellectual property are less common.

   - Monetary Value: Estimate the potential monetary loss from recipe tampering at 500,000 euros.
   - Expected Value: Expected Value = Probability (0.4) * Monetary Value 500,000 euros = 200,000 euros

3. DDoS attacks on the e-commerce platform, impacting sales.

   - Probability: Assign a probability of 0.5 (50%) as DDoS attacks are relatively common.
   - Monetary Value: Estimate the potential monetary loss from a DDoS attack at 250,000 euros.
   - Expected Value: Expected Value = Probability (0.5) * Monetary Value 250,000 euros = 125,000 euros

Based on these estimated values, we can prioritize the risks as follows:

1. Unauthorized Access to Customer Health Data: High Expected Value (700,000 euros)
2. Tampering with Proprietary Recipes: Moderate Expected Value (200,000 euros)
3. DDoS Attacks on E-commerce Platform: Low-Moderate Expected Value (125,000 euros)

### Threat Actors:

Foodie Delights Inc. may be targeted by cybercriminals, competitors, and angry employees. Their threat model should consider a wide range of potential adversaries.

#### Known TTPs (Tactics, Techniques, Procedures):

Common TTPs include phishing, SQL injection, malware distribution, insider threats, and social engineering.

#### COI (Capability, Opportunity, Intent):

Adversaries with the capability and opportunity to breach customer data, tamper with recipes, or disrupt online sales may have malicious intent driven by financial gain or competitive advantage.

## **(3) What are we going to do about it?**

To mitigate identified risks, Foodie Delights Inc. will:

- Implement multi-factor authentication to prevent unauthorized access.
- Utilize encryption to protect customer health data and proprietary recipes.
- Implement intrusion detection systems to detect tampering and repudiation.
- Regularly conduct security training for employees to mitigate insider threats.
- Invest in DDoS mitigation solutions for the e-commerce platform.

## **(4) Did we do a good enough job?**

To assess their security measures, Foodie Delights Inc. will:

- Conduct regular security audits and penetration testing.
- Perform continuous threat modeling and evaluation.
- Collaborate with third-party experts to assess the effectiveness of their security measures.

# Sources and links

- *Threat Modeling Manifesto*. https://www.threatmodelingmanifesto.org/. Accessed 6 Sept. 2023.
- *World’s Shortest Threat Modeling Course - YouTube*. https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf. Accessed 6 Sept. 2023.
- *Chapter 1: Dive In and Threat Model! - Threat Modeling: Designing for Security [Book]*. https://www.oreilly.com/library/view/threat-modeling-designing/9781118810057/9781118810057c01.xhtml. Accessed 7 Sept. 2023
- *Threat Modeling - OWASP Cheat Sheet Series*. https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html. Accessed 7 Sept. 2023.

- *ChatGPT - OpenAI* [ChatGPT (openai.com)](https://chat.openai.com/?model=text-davinci-002-render-sha) Accessed 7 Sept. 2023.
