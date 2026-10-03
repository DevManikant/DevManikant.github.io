<div align="center">

# 👋 MANIKANT SHARMA

### `AUTOMATION ENGINEER` · `PYTHON DEVELOPER` · `QA AUTOMATION`

**I build automation solutions that are fast, reliable, and scalable.**

</div>

<!-- The container where the greeting will appear -->
<!-- The container where the greeting will appear -->
<div id="dynamic-greeting" style="background-color: #0d1117; border: 1px solid #30363d; padding: 15px; border-radius: 6px; font-family: monospace; color: #c9d1d9;">
    <span id="welcome-text">Loading connection details...</span>
</div>

<script>
    async function showVisitorGreeting() {
        try {
            // 1. Fetch the user's IP and coordinates using GeoJS (Reliable & CORS-friendly)
            const geoResponse = await fetch('https://get.geojs.io/v1/ip/geo.json');
            const geoData = await geoResponse.json();
            
            const ip = geoData.ip;
            const lat = geoData.latitude;
            const lon = geoData.longitude;

            // 2. Fetch weather using Open-Meteo
            const weatherResponse = await fetch(`https://api.open-meteo.com/v1/forecast?latitude=${lat}&longitude=${lon}&current=temperature_2m`);
            const weatherData = await weatherResponse.json();
            
            const temp = weatherData.current.temperature_2m;

            // 3. Inject the data into the HTML
            document.getElementById('welcome-text').innerHTML = 
                `> Hey <strong>IP=${ip}</strong>, welcome to my page.<br>` +
                `> The current temperature near you is around <strong>${temp}°C</strong>.<br>` + 
                `> Below is more information about me.`;
                
        } catch (error) {
            // Fallback message if tracking is blocked
            document.getElementById('welcome-text').innerText = "> Welcome to my page. Below is more information about me.";
            console.error("Could not load dynamic visitor data", error);
        }
    }

    showVisitorGreeting();
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
