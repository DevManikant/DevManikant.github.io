<div align="center">

# 👋 MANIKANT SHARMA

### `AUTOMATION ENGINEER` · `PYTHON DEVELOPER` · `QA AUTOMATION`

**I build automation solutions that are fast, reliable, and scalable.**

</div>

<!-- The container where the greeting will appear -->
<!-- The container where the greeting will appear -->
<style>
  /* Import a slick coding font from Google Fonts */
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&display=swap');
  
  /* Styling for your Title Name */
  .hero-section { text-align: center; font-family: 'Segoe UI', Tahoma, sans-serif; margin-bottom: 40px; margin-top: 20px; }
  .hero-title { font-size: 3em; margin: 10px 0; font-weight: 800; color: #ffffff; }
  .hero-subtitle { font-size: 1.2em; color: #58a6ff; letter-spacing: 2px; font-weight: 600; margin-bottom: 10px; }
  .hero-desc { font-size: 1.1em; color: #8b949e; }
  
  /* Styling for the Terminal Window */
  .terminal-window {
    max-width: 750px; margin: 0 auto; background-color: #0d1117; 
    border: 1px solid #30363d; border-radius: 10px; 
    box-shadow: 0 10px 30px rgba(0,0,0,0.5); overflow: hidden;
  }
  .terminal-header { background: #161b22; padding: 12px; display: flex; gap: 8px; border-bottom: 1px solid #30363d; }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-red { background: #ff5f56; } .dot-yellow { background: #ffbd2e; } .dot-green { background: #27c93f; }
  
  .terminal-body { 
    padding: 25px; font-family: 'Fira Code', monospace; 
    font-size: 16px; color: #7ee787; line-height: 1.8; text-align: left;
  }
  
  /* Blinking cursor animation */
  .cursor { display: inline-block; width: 10px; height: 18px; background-color: #7ee787; animation: blink 1s step-end infinite; vertical-align: middle; margin-left: 5px; }
  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
  .highlight { color: #79c0ff; font-weight: 600; }
</style>

<!-- Clean HTML replacing your broken Markdown -->
<div class="hero-section">
    <h1 class="hero-title">👋 MANIKANT SHARMA</h1>
    <div class="hero-subtitle">AUTOMATION ENGINEER &bull; PYTHON DEVELOPER &bull; QA AUTOMATION</div>
    <div class="hero-desc">I build automation solutions that are fast, reliable, and scalable.</div>
</div>

<!-- The Animated Terminal -->
<div class="terminal-window">
    <div class="terminal-header">
        <div class="dot dot-red"></div>
        <div class="dot dot-yellow"></div>
        <div class="dot dot-green"></div>
    </div>
    <div class="terminal-body">
        <span id="typed-text"></span><span class="cursor"></span>
    </div>
</div>

<script>
    async function executeTerminalSequence() {
        const typedText = document.getElementById('typed-text');
        typedText.innerHTML = "> Initializing connection sequence...<br>";
        
        try {
            // Fetch IP and Location
            const geoResponse = await fetch('https://get.geojs.io/v1/ip/geo.json');
            const geoData = await geoResponse.json();
            
            // Fetch Weather
            const weatherResponse = await fetch(`https://api.open-meteo.com/v1/forecast?latitude=${geoData.latitude}&longitude=${geoData.longitude}&current=temperature_2m`);
            const weatherData = await weatherResponse.json();
            
            // Truncate messy IPv6 addresses for a cleaner terminal look
            let ipDisplay = geoData.ip;
            if(ipDisplay.length > 15) ipDisplay = ipDisplay.substring(0, 15) + '...';

            // The lines to type out
            const lines = [
                `> Connection established from <span class="highlight">IP: ${ipDisplay}</span>`,
                `> Location verified: <span class="highlight">${geoData.city || 'Unknown'}, ${geoData.country_code || ''}</span>`,
                `> Local environment temp: <span class="highlight">${weatherData.current.temperature_2m}°C</span>`,
                `> Status: <span style="color: #ffbd2e;">Awaiting further commands...</span>`
            ];

            typedText.innerHTML = ""; // Clear initialization text
            
            // Artificial delay to simulate a script running line by line
            for (let i = 0; i < lines.length; i++) {
                typedText.innerHTML += lines[i] + "<br>";
                await new Promise(r => setTimeout(r, 700)); // 700ms delay between lines
            }
            
        } catch (error) {
            typedText.innerHTML = "> Execution failed. Loading local fallback...<br>> Welcome to my portfolio.";
        }
    }

    // Run sequence on load
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
