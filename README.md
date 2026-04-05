[![Profile Quality Gate](https://img.shields.io/github/actions/workflow/status/M-Bash/M-Bash/profile-quality-gate.yml?branch=main&style=for-the-badge&logo=github&label=Profile%20Quality%20Gate&color=a6da95)](https://github.com/M-Bash/M-Bash/actions/workflows/profile-quality-gate.yml)

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=24273a&height=250&section=header&text=MAHAMED%20BASHIR&fontSize=70&fontColor=c6a0f6&fontAlignY=35&animation=fadeIn&desc=Cloud%20Architecture%20%7C%20Regulated%20AI%20%7C%20FinOps&descSize=20&descAlignY=55&descAlign=62" width="100%" alt="M-Bash Banner" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=24&duration=3500&pause=1000&color=8aadf4&center=true&vCenter=true&width=1000&lines=Engineering+High-Leverage+Cloud+Systems;Architecting+Regulated+AI+Backbones;Enforcing+Global+Data+Sovereignty;Optimizing+Infrastructure+Unit+Economics" alt="Typing SVG" />
</a>

<br/>

<a href="https://www.linkedin.com/in/mahamed-bashir" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-%238aadf4.svg?style=for-the-badge&logo=linkedin&logoColor=24273a" />
</a>
&nbsp;
<a href="mailto:mbas2097152@gmail.com" target="_blank">
  <img src="https://img.shields.io/badge/Email-%23ee99a0.svg?style=for-the-badge&logo=gmail&logoColor=24273a" />
</a>
&nbsp;
<a href="https://github.com/M-Bash/TokyoAPPI" target="_blank">
  <img src="https://img.shields.io/badge/Portfolio-%23c6a0f6.svg?style=for-the-badge&logo=react&logoColor=24273a" />
</a>

<br/>

<img src="https://img.shields.io/badge/AWS-Solutions_Architect_Associate-%23f5a97f.svg?style=for-the-badge&logo=amazon-aws&logoColor=24273a" />
<img src="https://img.shields.io/badge/HashiCorp-Terraform_Associate-%23c6a0f6.svg?style=for-the-badge&logo=terraform&logoColor=24273a" />

</div>

---

### Philosophy
I build systems that decouple **time** from **money**. I architect for highly-regulated industries where security is not a checkbox—it’s a prerequisite for existence. My work focuses on **Infrastructure-as-Code**, **Zero-Trust Security**, and **FinOps** discipline to ensure that scale never comes at the cost of stability or profitability.

---

### 🏛️ TokyoAPPI
**The Challenge:** Architect a telemedicine platform requiring 99.99% availability while strictly adhering to Japan's APPI data residency laws—preventing PHI (Patient Health Information) from persisting in failover regions.

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
    
    style User fill:#24273a,stroke:#8aadf4,color:#cad3f5
    style CF fill:#24273a,stroke:#f5a97f,color:#cad3f5
    style ALBT fill:#24273a,stroke:#a6da95,color:#cad3f5
    style RDST fill:#24273a,stroke:#c6a0f6,color:#cad3f5
    style EC2S fill:#24273a,stroke:#ee99a0,color:#cad3f5
```

[**Explore Repository**](https://github.com/M-Bash/TokyoAPPI) | [**View Audit Manifest**](https://github.com/M-Bash/TokyoAPPI/blob/main/DELIVERABLES/README.md)

</div>

---

### 🛠️ Core

<div align="center">

| Compute & Mesh | Infrastructure & Security | AI & Compliance |
| :--- | :--- | :--- |
| <p align="center"><img src="https://skillicons.dev/icons?i=aws,gcp,kubernetes" /></p> | <p align="center"><img src="https://skillicons.dev/icons?i=terraform,vault,githubactions" /></p> | <p align="center"><img src="https://skillicons.dev/icons?i=python,bash,linux" /></p> |

</div>

---

### 📊 Tracking

<div align="center">

![WakaTime](https://github-readme-stats.vercel.app/api/wakatime?username=M-Bash&layout=compact&theme=catppuccin_macchiato&hide_border=true)
![Activity](https://github-readme-stats.vercel.app/api?username=M-Bash&show_icons=true&theme=catppuccin_macchiato&hide_border=true&count_private=true)

</div>

---

### ⚡ Recent Activity
<!--START_SECTION:activity-->
<!-- This section is automatically updated by the profile-activity-worker -->
<!--END_SECTION:activity-->
