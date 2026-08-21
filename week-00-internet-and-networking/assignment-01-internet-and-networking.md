# Week 00 - Internet and Networking

Part of the DevOps Micro Internship (DMI) Cohort 3 with Agentic AI

---

# 🧑‍💻 Task 1: Using ChatGPT as Your Learning Assistant

## Scenario

You're new to DevOps and will frequently encounter technical questions. ChatGPT can be your learning companion.

## Your Task

Write a clear ChatGPT prompt to help you understand:

> "What is a protocol in networking? Explain with a simple real-life example."

Take a screenshot of your interaction showing:

* Your detailed prompt (with clear expectations)
* ChatGPT's simplified response with an example

## Screenshot

Save your screenshot in the `screenshots` folder and update the file name below.

![Task 1 Screenshot](PIC 1.png)
PIC 2.png
PIC3.png
PIC4.png


Replace `task-1-chatgpt.png` with your actual screenshot file name.

---

## What I Learned (2–3 lines)

I learned that a protocol is simply a set of rules that lets devices communicate and understand each other, similar to how WhatsApp messages or phone calls follow steps like connecting, sending, and confirming. Without protocols, computers wouldn't know how to format, send, or verify data, so nothing would actually work.

---

# 🌐 Task 2: Internet and Networking

## Scenario

Your friend is launching an online bookstore named **EpicReads**.

He asked you to explain how users globally can access his website hosted in Finland.

## Your Task

Write a short explanation (**100–150 words**) that includes:

* Packet Switching
* IP Address
* TCP/IP
* HTTP/HTTPS

💡 **Tip:** You may use ChatGPT (as demonstrated in Task 1) to refine your explanation.

## Answer

When a user anywhere in the world tries to access EpicReads, their device first needs to find the website's location. It sends a request to a DNS server, which acts like a phonebook and translates the domain name (epicreads.com) into the numerical IP address of the server hosting it in Finland.

Once the address is known, the user's request travels across the internet using packet switching. The data is broken into small packets, each one routed independently across various networks until it reaches the Finland-based server. The server processes the request and sends the response back the same way, in packets, which are reassembled on the user's device.

This is possible because every device on this journey follows shared protocols like TCP/IP, which define how data is formatted, sent, and confirmed, so no matter where in the world a user is, the request finds its way to Finland and back.

---

# 🏗️ Task 3: Application Architecture & Stack

## Scenario

EpicReads bookstore has two application versions:

### Two-Tier Application

* Frontend
* Database

### Three-Tier Application

* Frontend
* Backend
* Database

## Your Task

* Draw simple diagrams (hand-drawn or tool-based such as draw.io)
* Label each layer clearly
* List at least two common technologies or tools used for each layer
* Submit a screenshot or photo clearly showing your own drawing

## Diagram Screenshot / Photo

Save your diagram image in the `screenshots` folder and update the file name below.

![Application Architecture Diagram](PIC5.png)


Replace `task-3-diagram.png` with your actual diagram file name.

---

## Technologies Used

### Frontend

* React (for building an interactive, component-based user interface)
- HTML/CSS with a framework like Tailwind (for styling and responsive layout)


### Backend

* Node.js with Express (to handle server-side logic and API requests)
- REST API (to allow the frontend to communicate with the backend)


### Database

* PostgreSQL (a relational database, ideal for structured data like books, orders, and users)
- Redis (optional, for caching frequently accessed data like popular book listings)


---

# 🌍 Task 4: Domain Name & DNS (Basic Concepts)

## Scenario

Your friend's bookstore **EpicReads** is currently accessible through:

```text
52.172.142.222:3000
```

He purchased the domain:

```text
epicreads.com
```

## Your Task

In **50–100 words**, explain in your own words:

1. What is DNS (Domain Name System)?
2. Which DNS record type should be used to connect the domain to the given IP, and why?

## Answer

DNS (Domain Name System) works like the internet's phonebook. It translates human-friendly domain names, like epicreads.com, into the numerical IP address that computers actually use to locate a server, such as 52.172.142.222.

To connect epicreads.com to this IP address, an A record should be used. An A record maps a domain name directly to an IPv4 address, which is exactly what's needed here since we have a numeric IP and want the domain name to resolve to it. Since the site also runs on port 3000, that detail would be handled separately in the server or reverse proxy configuration, not through DNS itself.

---

# 💻 Task 5: Visual Studio Code Setup (Hands-on)

## Your Task

Install Visual Studio Code (if not already installed).

Take a screenshot of your VS Code environment showing:

* Terminal open inside VS Code
* Running a basic command:

### Windows

```powershell
dir
```

### Linux / macOS

```bash
pwd
ls
```

* Your selected VS Code theme clearly visible

⚠️ **Important:** The screenshot must show your username or another identifiable detail to confirm it is your environment.

## Screenshot

Save your screenshot in the `screenshots` folder and update the file name below.

![VS Code Setup Screenshot](PIC6.png)


Replace `task-5-vscode.png` with your actual screenshot file name.

---

# 🔗 Task 6: Publish Your Assignment as a LinkedIn Post

## Objective

Publishing on LinkedIn helps you:

* Build your professional online presence
* Reinforce your learning
* Document your DevOps journey publicly

## Your Task

Summarize your answers from Tasks 1–5 into a LinkedIn post.

Clearly structure your post into the following sections:

* ChatGPT
* Internet & Networking
* App Architecture
* DNS
* VS Code Setup

Add the following credit note at the end of your post:

> **P.S. This post is part of the DevOps Micro Internship (DMI) with Agentic AI — Cohort 3 — by Pravin Mishra. My graded progress is public: https://dmi.pravinmishra.com/s/YOUR-GITHUB-USERNAME.html · Start your DevOps journey: https://dmi.pravinmishra.com/?utm_source=student&utm_medium=ps-linkedin&utm_campaign=cohort3**

---

## LinkedIn Post URL

Paste your LinkedIn post URL here:https://www.linkedin.com/posts/onyemaechibrenda_thecaketechgirl-activity-7449881174187032576-h_c_?utm_source=share&utm_medium=member_ios&rcm=ACoAAFXeP7cBfyttCN7YeWGWskgXxa5AJ5Vk1KA 

```text

```

---

## LinkedIn Post Backup Copy

From baking cakes to building systems…
Turns out both need the right layers 🍰☁️

I used apps everyday, but I never really understood what happens behind the scenes.
This week, that changed. 

I just completed my Week 0 DevOps assignment, and here’s what clicked for me:

•ChatGPT : It’s not just a chatbot, but a learning partner
•Networking :The internet isn’t magic… it’s structured (TCP/IP)
•Architecture :Apps are built in layers (2-tier vs 3-tier)
•DNS :The internet’s phonebook
•VS Code :My workspace is finally ready

My biggest realization: Every click,Every app, Every website is powered by systems working together behind the scenes.

And now, I’m starting to understand it.

This is just the beginning  and I’m documenting my DevOps journey as I grow ☁️
#TheCakeTechgirl 

P.S. This post is part of the FREE DevOps Micro Internship Cohort run by Pravin Mishra  You can start your DevOps journey for free from his YouTube Playlist

From baking cakes to building systems…
Turns out both need the right layers 🍰☁️

I used apps everyday, but I never really understood what happens behind the scenes.
This week, that changed. 

I just completed my Week 0 DevOps assignment, and here’s what clicked for me:

•ChatGPT : It’s not just a chatbot, but a learning partner
•Networking :The internet isn’t magic… it’s structured (TCP/IP)
•Architecture :Apps are built in layers (2-tier vs 3-tier)
•DNS :The internet’s phonebook
•VS Code :My workspace is finally ready

My biggest realization: Every click,Every app, Every website is powered by systems working together behind the scenes.

And now, I’m starting to understand it.
This is just the beginning and I’m documenting my DevOps journey as I grow ☁️
hashtag#TheCakeTechgirl 

P.S. This post is part of the FREE DevOps Micro Internship Cohort run by Pravin Mishra You can start your DevOps journey for free from his YouTube Playlist



---

# Reflection – Week 0

### What did you find easy?

Using ChatGPT as a learning tool came naturally to me since I already talk to it daily. Breaking down what a protocol is and how devices communicate wasn't too hard once I had a real-life example like WhatsApp or a phone call to compare it to.

---

### What was difficult?

Understanding the difference between 2-tier and 3-tier architecture took a bit more effort, since it required picturing how the frontend, backend, and database actually separate and communicate with each other, rather than just memorizing definitions. DNS also took a second read before it clicked.

---

### What will you improve next week?

I want to spend more time actually testing concepts hands-on instead of just reading about them, and get faster at setting up my tools so I can move through tasks with less friction.

---

## 📌 About DMI & CloudAdvisory

DevOps Micro Internship (DMI) is a project-based DevOps program run by Pravin Mishra (The CloudAdvisory) focused on real-world execution, systems thinking, and career readiness.

It helps learners build strong DevOps foundations with hands-on experience.


## 📌 Resources

- 🌐 **DMI Official Website:** https://dmi.pravinmishra.com?utm_source=github&utm_medium=readme  
- 🎓 **University:** https://university.pravinmishra.com?utm_source=github&utm_medium=readme  
- 💬 **Discord Community:** https://discord.pravinmishra.com?utm_source=github&utm_medium=readme  
- 📝 **Blog:** https://dmi.pravinmishra.com/blog?utm_source=github&utm_medium=readme  
- ▶️ **YouTube Playlist (DMI Cohort 3):** https://www.youtube.com/playlist?list=PLFeSNDtI4Cho  
- 🔗 **Pravin Mishra (LinkedIn):** https://www.linkedin.com/in/pravin-mishra-aws-trainer/  
- 🏢 **CloudAdvisory (LinkedIn):** https://www.linkedin.com/company/thecloudadvisory/

---

*This submission is part of DevOps Micro Internship (DMI) Cohort 3 — Agentic AI Track*