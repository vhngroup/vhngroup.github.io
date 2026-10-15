# Víctor Noguera — Builder Portfolio

📍 Colombia | ✉️ info@vhngroup.com | 🐙 [github.com/vhngroup](https://github.com/vhngroup) | 🔗 [LinkedIn](https://linkedin.com/in/victor--noguera)

I don't wait for classes to learn how to build. I find problems, figure out the stack required to solve them, and ship. I am a self-taught full-stack developer and AI engineer from Colombia. This portfolio details the production systems, AI integrations, and automations I have personally built.

---

## 1. The Business Engine: VHNGROUP E-Commerce Orchestration
**Links:** [vhngroup.com](https://vhngroup.com) | [Nequi API Repo](https://github.com/vhngroup/nequi)

**What I built:**  
I founded and single-handedly run a network of 5 live WordPress/WooCommerce sites. To keep them running smoothly on a Linux server without a dev team, I built a custom 243-line Bash orchestration pipeline (`Plugins_update_v2.sh` and `Orquestador.sh`). It automates inventory syncs with MercadoLibre, generates sitemaps, updates plugins, cleans the databases, and purges caches nightly via cron. I also wrote a custom Cloudflare WAF ruleset to drop malicious traffic and implemented an AWS Signature V4 payment gateway in raw PHP to connect to Nequi (Colombia's leading fintech).

**The Challenge:**  
Serving **458,000+ monthly requests** on a shared-but-optimized server means memory leaks or scraper bots will take the sites down. Manual updates were costing me 4 hours a week. Furthermore, Nequi's API requires AWS SigV4 authentication, which didn't have a simple PHP drop-in library for my specific WooCommerce setup.

**What I learned:**  
Real-world DevOps. I learned how to write memory-safe PHP (using 512MB limits to export 500 products per page without crashing), how to use `nohup` for reliable background processes, and how to write regex-based WAF rules to block AWS ASNs, headless browsers, and Shodan scanners at the edge. I learned cryptography basics to manually sign HTTP requests for AWS SigV4.

**Results & Traction:**  
- 5 profitable, live e-commerce sites.
- 458K+ legitimate requests served monthly with zero downtime.
- 0 hours spent on manual server maintenance or plugin updates.

---

## 2. Applied AI: RAG Agents & CV Analyzer
**Links:** [RAG Gemini Repo](https://github.com/vhngroup/rag_geminy) | [GitHub Profile](https://github.com/vhngroup)

**What I built:**  
An HR screening tool that ingests candidate resumes, compares them against job descriptions using OpenAI's GPT-4, and outputs a structured JSON compatibility score and summary. I also built a Retrieval-Augmented Generation (RAG) pipeline using Google Gemini and LlamaIndex for document Q&A over private knowledge bases.

**The Challenge:**  
Moving beyond basic API wrappers to actual RAG. Parsing messy, unstructured PDF resumes and engineering the prompts to force the LLM to output strict, programmatic JSON that an HR pipeline could actually ingest.

**What I learned:**  
I learned how vector embeddings work, how to chunk documents effectively, and how to use LlamaIndex to ground an LLM in private data rather than relying solely on its pre-trained weights.

**Results & Traction:**  
- Reduced manual CV screening time by an estimated 70% by instantly filtering out non-compatible resumes based on hard data, not keyword matching.

---

## 3. Computer Vision Arcades: Brick Breaker MediaPipe
**Links:** [Brick Breaker Repo](https://github.com/vhngroup/Brick_Breaker_MediaPipe) 

**What I built:**  
A fully playable "Brick Breaker" arcade game controlled entirely by hand gestures in front of a webcam. Built from scratch using Python, OpenCV, and Google's MediaPipe.

**The Challenge:**  
Processing 21 hand landmarks per frame and translating those spatial coordinates into paddle physics with less than 30ms of latency—purely on standard CPU and webcam hardware (no dedicated GPU).

**What I learned:**  
Real-time computer vision processing and frame buffer optimization. I learned how to translate 3D spatial coordinates from a 2D camera feed into smooth, responsive game mechanics.

**Results & Traction:**  
- A zero-lag, touchless arcade game. It proved to me that computer vision is ready for consumer-scale interaction without needing expensive hardware. 

---

## 4. Enterprise SAP Automation: RFC Python & VBA
**Links:** [SAP RFC Connector Repo](https://github.com/vhngroup/Python/tree/main/Conector_Sap) | [SAP Scripts Repo](https://github.com/vhngroup/SAP_Scripts)

**What I built:**  
A direct Python-to-SAP RFC connector (`pyrfc`) and a suite of 5 complex Excel VBA macros that automate SAP PM (Plant Maintenance) operations. The tools handle bulk notification editing, time extraction, and work order tracking.

**The Challenge:**  
SAP GUI scripting is notoriously slow, brittle, and breaks when UI layouts change. To move fast, I had to figure out how to bypass the graphical interface entirely and communicate directly with the SAP backend using Remote Function Calls (RFC).

**What I learned:**  
Enterprise system architecture and Windows COM automation. I learned how to reverse-engineer SAP's BAPI/RFC endpoints to read and write data programmatically, completely abstracting the complexity from the end-user.

**Results & Traction:**  
- These tools are actively used in real industrial plant maintenance operations.
- Tasks that took hours of manual data entry in SAP are now executed with a single click.

---

## 5. Machine Learning Infrastructure: Zero-Shot Voice Cloning
**Links:** [F5-TTS Voice Project Repo](https://github.com/vhngroup/Python/tree/main/Voice_Project)

**What I built:**  
A Dockerized Text-to-Speech (TTS) service using the F5-TTS model, capable of zero-shot voice cloning. 

**The Challenge:**  
Setting up complex Python ML dependencies (PyTorch, CUDA, specific audio libraries) natively is a nightmare of dependency conflicts. I needed a way to run this model reliably on any machine without breaking the host environment.

**What I learned:**  
Advanced Docker containerization for machine learning workloads. I learned how to manage large model weights within containers, configure hardware passthrough, and expose local ML models as consumable APIs.

**Results & Traction:**  
- A production-ready, locally hosted voice generation service that doesn't rely on expensive or rate-limited third-party APIs.

---

## 6. B2B Automated Scraping Pipelines
**Links:** [LinkedIn Bot Repo](https://github.com/vhngroup/LinkedinBot)

**What I built:**  
A concurrent scraping engine using Python, Selenium, and Scrapy that extracts product catalogs from over 10 different LATAM tech distributors. I also built a LinkedIn bot for B2B lead generation that searches by industry/role and exports contact databases.

**The Challenge:**  
Dealing with anti-bot protections, handling session timeouts, and parsing >100MB of messy, unstructured HTML into clean, relational inventory data.

**What I learned:**  
Web scraping at scale, headless browser orchestration, DOM traversal, and handling asynchronous JS rendering on target sites. 

**Results & Traction:**  
- Completely automated the inventory population for my e-commerce sites, eliminating the need to manually update prices and stock for thousands of products.

---

### *Other Explorations & Repositories*
Beyond the core projects above, my [GitHub](https://github.com/vhngroup) contains over 50 other repositories spanning:
- **Web:** Laravel LMS platforms, Astro/Svelte AI chat interfaces, Node.js REST APIs.
- **Security:** Tor-routed anonymized downloaders, parallel password crackers (leet-speak permutations via COM).
- **Network:** PowerShell zero-touch WiFi & SMB provisioning scripts deployed in a real school lab.
- **Data Science:** Tableau dashboards, Python algorithm visualizers, Pandas bank data analytics.
