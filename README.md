<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&display=swap');
  
  /* Blends perfectly with your chosen Hacker Theme */
  .hero-section { text-align: center; margin: 40px 0 30px 0; }
  .hero-title { font-size: 2.5em; margin: 10px 0; font-weight: 700; color: #b5e853; /* Hacker green */ }
  .hero-subtitle { font-size: 1.2em; color: #ffffff; letter-spacing: 2px; }
  
  /* Rugged CLI Window styling */
  .hacker-terminal {
    max-width: 750px; margin: 0 auto 40px auto; background-color: #0f110f; 
    border: 1px solid #b5e853; border-radius: 2px; 
    box-shadow: 0 0 10px rgba(181, 232, 83, 0.1); overflow: hidden; text-align: left;
  }
  .hacker-header { 
    background: #1a1c1a; padding: 6px 12px; border-bottom: 1px solid #b5e853; 
    font-family: 'Fira Code', monospace; color: #777; font-size: 12px; 
  }
  .hacker-body { 
    padding: 20px; font-family: 'Fira Code', monospace; 
    font-size: 15px; color: #b5e853; line-height: 1.6;
  }
  
  .cursor { display: inline-block; width: 10px; height: 16px; background-color: #b5e853; animation: blink 1s step-end infinite; vertical-align: middle; margin-left: 4px;}
  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
  .highlight-white { color: #ffffff; font-weight: 600; }
</style>

<div class="hero-section">
    <h1 class="hero-title">👋 MANIKANT SHARMA</h1>
    <div class="hero-subtitle">AUTOMATION ENGINEER &bull; PYTHON DEVELOPER &bull; QA</div>
</div>

<div class="hacker-terminal">
    <div class="hacker-header">Administrator: Windows PowerShell</div>
    <div class="hacker-body">
        <span style="color: #fff;">PS C:\Automation_Env></span> ./init_session.ps1<br><br>
        <span id="typed-text"></span><span class="cursor"></span>
    </div>
</div>

<script>
    async function executeTerminalSequence() {
        const typedText = document.getElementById('typed-text');
        typedText.innerHTML = "[*] Bypassing execution policy...<br>[*] Initializing remote connection sequence...<br><br>";
        
        try {
            const geoResponse = await fetch('https://get.geojs.io/v1/ip/geo.json');
            const geoData = await geoResponse.json();
            
            const weatherResponse = await fetch(`https://api.open-meteo.com/v1/forecast?latitude=${geoData.latitude}&longitude=${geoData.longitude}&current=temperature_2m`);
            const weatherData = await weatherResponse.json();
            
            let ipDisplay = geoData.ip;
            if(ipDisplay.length > 15) ipDisplay = ipDisplay.substring(0, 15) + '...';
            
            let cityDisplay = geoData.city && geoData.city !== 'Unknown' ? geoData.city : 'Remote Node';

            const lines = [
                `[+] Handshake successful. Client IP: <span class="highlight-white">${ipDisplay}</span>`,
                `[+] Node coordinates verified: <span class="highlight-white">${cityDisplay}, ${geoData.country_code || ''}</span>`,
                `[+] Environment temp check: <span class="highlight-white">${weatherData.current.temperature_2m}°C</span>`,
                `[+] VNC Server ready. Awaiting automation scripts...`
            ];

            // Brief pause before outputting data
            await new Promise(r => setTimeout(r, 800));
            
            for (let i = 0; i < lines.length; i++) {
                typedText.innerHTML += lines[i] + "<br>";
                await new Promise(r => setTimeout(r, 600)); 
            }
            
        } catch (error) {
            typedText.innerHTML += "[-] Execution failed. Loading static fallback.<br>[+] Welcome to my portfolio.";
        }
    }

    executeTerminalSequence();
</script>
<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:238636&height=120&section=header" width="100%"/>
---

## 🧑‍💻 About Me

I'm an **Automation Engineer and Python Developer** focused on building practical automation systems and reliable testing solutions.

My experience spans **browser automation, QA automation, API testing, performance testing, web scraping, real-time monitoring, and database validation**.

I enjoy working on problems where **speed, reliability, and automation** matter — from running multiple browser instances in parallel to building systems that monitor real-time events.

```text
┌───────────────────────────────────────────────────────────┐
│                                                           │
│   BUILD          AUTOMATE          TEST          OPTIMIZE  │
│                                                           │
│      Python  →  Playwright  →  API  →  Performance       │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

---

# ⚙️ My Tech Arsenal

### 🐍 Languages

<p>
<img src="https://skillicons.dev/icons?i=python,javascript,c" />
</p>

### 🎭 Automation & Testing

<p>
<img src="https://skillicons.dev/icons?i=selenium,pytest,cypress" />
</p>

**Playwright** · **Selenium** · **PyTest** · **Cypress** · **BDD**

### 🔌 API & Performance

`REST API` · `Requests` · `Locust` · `API Automation` · `Load Testing`

### 🌐 Web & Backend

<p>
<img src="https://skillicons.dev/icons?i=react,nodejs,html,css,mongodb" />
</p>

### ☁️ Cloud & DevOps

<p>
<img src="https://skillicons.dev/icons?i=aws,azure,docker,git,github" />
</p>

### 🗄️ Database

`SQL` · `MongoDB` · `Backend Validation` · `Data Verification`

---

# 🚀 What I Build

<table>
<tr>
<td width="50%">

### 🤖 Automation Engineering

Building browser automation systems using **Python, Playwright, and Selenium**.

</td>
<td width="50%">

### 🧪 QA Automation

Creating automated test solutions for functional, UI, API, and end-to-end testing.

</td>
</tr>

<tr>
<td width="50%">

### ⚡ Performance Engineering

Working with parallel browser execution, event-driven automation, and performance optimisation.

</td>
<td width="50%">

### 🔌 API Testing

Automating REST API validation and verifying backend data using SQL.

</td>
</tr>

<tr>
<td width="50%">

### 🌐 Web Automation

Building web scraping, monitoring, and browser-based automation solutions.

</td>
<td width="50%">

### 📡 Real-Time Systems

Creating monitoring systems that detect events and deliver real-time notifications.

</td>
</tr>
</table>

---

# 🔥 Featured Projects

## ⚡ High-Performance Browser Automation

A browser automation solution designed for **time-sensitive workflows** using a hybrid Playwright architecture.

**Highlights:**

* Parallel browser automation
* Multiple concurrent Playwright instances
* DOM and JavaScript optimisation
* Mutation Observer optimisation
* Event-driven automation
* Low-latency execution

**Stack:**

`Python` `Playwright` `JavaScript` `Chromium` `DOM Analysis`

---

## 🎟️ Real-Time Ticket Availability Monitoring

A monitoring system designed to track ticket availability and notify users when tickets become available.

**Highlights:**

* Real-time availability monitoring
* REST API integration
* Automated notifications
* Cloud-based execution

**Stack:**

`Python` `REST API` `Azure Functions` `Telegram Bot`

---

## 🧪 API & Performance Testing

Automated testing solutions for validating APIs and measuring system performance.

**Highlights:**

* REST API automation
* Response validation
* Database verification
* Load testing
* Performance analysis

**Stack:**

`Python` `Requests` `Locust` `SQL`

---



---

# 🐍 My Contribution Journey

<div align="center">

<img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" alt="GitHub Contribution Snake Animation" />

</div>

---

# 📊 GitHub Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=DevManikant&theme=react-dark&hide_border=true&area=true" width="100%"/>

</div>

---

# 💡 My Engineering Philosophy

<div align="center">

### `AUTOMATE THE BORING.`

### `OPTIMIZE THE SLOW.`

### `TEST THE IMPORTANT.`

### `BUILD WHAT MATTERS.`

</div>

---

# 🌐 Let's Connect

I'm always interested in discussing:

`Automation` · `Python` · `QA Engineering` · `Playwright` · `Selenium` · `Performance Testing` · `Interesting Technical Problems`

<p align="center">

<a href="https://github.com/DevManikant">
<img src="https://img.shields.io/badge/GitHub-Explore%20My%20Code-181717?style=for-the-badge&logo=github"/>
</a>

<a href="YOUR_LINKEDIN_URL">
<img src="https://img.shields.io/badge/LinkedIn-Connect%20With%20Me-0A66C2?style=for-the-badge&logo=linkedin"/>
</a>

</p>

---

<div align="center">

### ⚡ Automate the boring. Focus on the impact.

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:238636,50:161b22,100:0d1117&height=120&section=footer" width="100%"/>

</div>
