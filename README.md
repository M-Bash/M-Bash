[![Profile Quality Gate](https://img.shields.io/github/actions/workflow/status/M-Bash/M-Bash/profile-quality-gate.yml?branch=main&style=for-the-badge&logo=github&label=Profile%20Quality%20Gate)](https://github.com/M-Bash/M-Bash/actions/workflows/profile-quality-gate.yml)
<!-- PART 1: THE HERO HEADER -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=000000&height=250&section=header&text=MAHAMED%20BASHIR&fontSize=70&fontColor=ffffff&fontAlignY=35&animation=fadeIn&desc=Cloud%20Infrastructure%20%7C%20DevSecOps%20%7C%20Automation&descSize=20&descAlignY=55&descAlign=62" width="100%" alt="Header" />
</div>

<!-- PART 2: THE HOOK (FIXED WIDTH & TEXT) -->
<div align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=500&size=22&duration=3500&pause=1000&color=79C0FF&center=true&vCenter=true&width=1000&lines=Architecting+Multi-Region+AWS+Backbones;Enforcing+Compliance+via+IaC;Automating+Zero-Trust+Security+Pipelines;Optimizing+High-Availability+Architectures" alt="Typing SVG" />
  </a>
</div>

<br/>

<!-- PART 3: THE SOCIAL PROOF (BADGES) -->
<div align="center">
  <a href="https://www.linkedin.com/in/mahamed-bashir" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  &nbsp;
  <a href="mailto:mbas2097152@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://github.com/M-Bash/TokyoAPPI" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-View_Projects-282C34?style=for-the-badge&logo=react&logoColor=61DAFB" />
  </a>
</div>

<br/>
<br/>
<p align="center">
  &nbsp;
</p>


---

### 👨‍💻 Engineering Philosophy

I believe that **hope is not a strategy**. Reliable infrastructure is built on deterministic code, rigorous security controls, and automated verification. I don't just deploy resources; I build platforms that allow teams to ship faster without breaking things.

<table>
  <tr>
    <td width="50%" align="center" style="border: none;">
      <h3>🏛️ Infrastructure as Code</h3>
      <p>If it isn't in Git, it doesn't exist. I strictly define infrastructure using Terraform to prevent drift and ensure disaster recovery is a <code>terraform apply</code> away.</p>
    </td>
    <td width="50%" align="center" style="border: none;">
      <h3>🛡️ Security by Design</h3>
      <p>Compliance isn't an afterthought. I bake IAM least-privilege, WAF shielding, and encryption into the pipeline. I build architectures that pass audits by default.</p>
    </td>
  </tr>
</table>

---

### 🛠️ Toolkit

<div align="center">
  <table style="border: none; border-collapse: collapse;">
    <tr>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=aws" width="48" height="48" alt="AWS" />
        <br><b>Cloud</b>
      </td>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=terraform" width="48" height="48" alt="Terraform" />
        <br><b>IaC</b>
      </td>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=python" width="48" height="48" alt="Python" />
        <br><b>Automation</b>
      </td>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=bash" width="48" height="48" alt="Bash" />
        <br><b>Scripting</b>
      </td>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=githubactions" width="48" height="48" alt="Actions" />
        <br><b>CI/CD</b>
      </td>
      <td align="center" width="96" style="border: none;">
        <img src="https://skillicons.dev/icons?i=linux" width="48" height="48" alt="Linux" />
        <br><b>Core</b>
      </td>
    </tr>
  </table>
</div>

<br/>

<!-- CERTIFICATIONS AREA -->
<div align="center">
  <img src="https://img.shields.io/badge/AWS-Solutions_Architect_Associate-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=FF9900" />
  <img src="https://img.shields.io/badge/HashiCorp-Terraform_Associate-232F3E?style=for-the-badge&logo=terraform&logoColor=5C4EE5" />
</div>

<br/>

---

### 🏗️ Featured Architecture Case Studies

#### 📡 TokyoAPPI: Multi-Region Compliance Backbone
> **The Challenge:** Architect a telemedicine platform requiring 99.99% availability while strictly adhering to Japan's APPI data residency laws—preventing PHI (Patient Health Information) from persisting in the failover region (Brazil).

<div align="center">

```mermaid
graph LR
    User((User)) -- HTTPS --> CF[CloudFront Edge]
    CF -- Primary --> ALBT[Tokyo ALB]
    CF -- Failover --> ALBS[Brazil ALB]
    
    subgraph Hub [Tokyo Hub - Authority]
        ALBT --> EC2T[App Tier]
        EC2T --> RDST[(RDS Master)]
    end
    
    subgraph Spoke [Brazil Spoke - Stateless]
        ALBS --> EC2S[Stateless Tier]
    end
    
    EC2S -- Private TGW Corridor --> RDST
```

</div>

**The Solution:**
*   **Asymmetric Hub-and-Spoke:** Centralized persistence in `ap-northeast-1` with a stateless, compute-only extension in `sa-east-1`.
*   **The Legal Corridor:** Established **Transit Gateway (TGW) Peering** to route cross-region traffic over the AWS private backbone, bypassing the public internet.
*   **Origin Cloaking:** Implemented a "Double-Lock" security posture using **WAFv2** at the edge and **X-Origin-Secret** header handshakes at the ALB.

`Terraform` `Transit Gateway` `CloudFront` `WAFv2` `SSM Bridge`

[**Explore Repository**](https://github.com/M-Bash/TokyoAPPI) | [**View Audit Manifest**](https://github.com/M-Bash/TokyoAPPI/blob/main/DELIVERABLES/README.md)

---

### ⚡ Recent Activity
<!--START_SECTION:activity-->
1. 🚀 Published release [Initial Production-Grade Compliance Backbone](https://github.com/M-Bash/TokyoAPPI/releases/tag/v1.0.0) in [M-Bash/TokyoAPPI](https://github.com/M-Bash/TokyoAPPI)
2. 🔒 Closed issue [#1](https://github.com/M-Bash/M-Bash/issues/1) in [M-Bash/M-Bash](https://github.com/M-Bash/M-Bash)
3. 🔒 Closed issue [#2](https://github.com/M-Bash/M-Bash/issues/2) in [M-Bash/M-Bash](https://github.com/M-Bash/M-Bash)
<!--END_SECTION:activity-->
