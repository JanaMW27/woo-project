# 👋 Welcome to the WooCommerce Store Health Widget Project!

This guide is for new team members joining the project. Read this first — it will get you up and running in no time, even if you've never worked with code before.

---

## 🗂️ What Are We Building?

We're building a **WooCommerce widget** called the **Store Health Widget**. It lives inside the WordPress admin dashboard and helps store owners understand how their shop is performing — and what they can do to improve it.

The widget covers 4 areas:

| Area | What it does |
|---|---|
| 🔍 **Visibility** | Checks if the store is easy to find on Google |
| ⚡ **Performance** | Checks if the store loads fast |
| 🛒 **Conversion** | Checks if the store is set up to turn visitors into buyers |
| 💰 **Profit** | Shows which products perform best and how to earn more |

---

## 📁 Where Is the Project?

The project lives on GitHub at:

👉 **https://github.com/JanaMW27/woo-project**

GitHub is where all the project files are stored and where the team collaborates. Think of it like a shared Google Drive, but for code.

---

## 🧑‍💻 Who Is on the Team?

We are a small team of **2–3 designers**. Nobody on the team is a developer — and that's totally fine! We use **Claude (AI)** to help us write and understand all the code. You don't need to know how to code to contribute.

---

## 🤖 How Do We Work With Claude?

Claude is our coding assistant. Here's how to use it:

1. Go to **https://claude.ai**
2. Start a new conversation
3. Paste the contents of `CLAUDE.md` (from the repo) at the start of the conversation — this gives Claude the full context of our project
4. Describe what you want in plain English, e.g. *"Add a section that shows the number of products without images"*
5. Claude will write the code and explain what it does

> 💡 **Tip:** Always reference `CLAUDE.md` when starting a new Claude session. It ensures Claude understands our project, our stack, and our coding rules.

---

## 🚀 Getting Started — Step by Step

### Step 1: Get access to the repo

Ask the project owner (Jana) to add you as a collaborator on GitHub:
👉 **https://github.com/JanaMW27/woo-project**

You'll need a free GitHub account. Create one at https://github.com/signup if you don't have one.

### Step 2: Clone the repo to your computer

Once you have access, download the project to your computer. Open a terminal and run:

```bash
git clone https://github.com/JanaMW27/woo-project.git
cd woo-project
```

> 💡 Don't know what a terminal is? On Mac, search for "Terminal" in Spotlight. On Windows, search for "Git Bash" (install Git first from https://git-scm.com).

### Step 3: Set up your local environment with Docker

We use **Docker** to run a local WordPress + WooCommerce site on your computer.

1. Install **Docker Desktop**: https://www.docker.com/products/docker-desktop
2. Start Docker Desktop and wait for it to be running
3. In your terminal, navigate to the project folder and run:

```bash
docker-compose up
```

4. Open your browser and go to **http://localhost:8080** — you should see a WordPress site!
5. Log in to WP Admin at **http://localhost:8080/wp-admin** and activate the plugin under **Plugins → Installed Plugins**

### Step 4: Read the project context

Open **`CLAUDE.md`** in the repo. This is the main reference document that explains the tech stack, folder structure, and coding guidelines.

---

## 📂 Project File Structure
woo-project/
├── woo-health-widget.php          ← Main plugin file (entry point)
├── includes/
│   ├── class-health-checker.php   ← Logic that checks store health
│   └── class-widget.php           ← Registers the widget in WP Admin
├── assets/
│   ├── css/widget.css             ← Visual styling
│   └── js/widget.js               ← Interactive behaviour
├── templates/
│   └── widget-dashboard.php       ← The HTML layout of the widget
├── CLAUDE.md                      ← AI context document (read this!)
├── ONBOARDING.md                  ← You are here 👋
├── .gitignore                     ← Files Git should ignore
└── README.md                      ← Project summary

---

## 🌿 How We Use Git

- `main` — the stable version. Never work directly here.
- Feature branches — create one whenever you start something new.

```bash
# Create a new branch
git checkout -b my-feature-name

# Save your work
git add .
git commit -m "Describe what you changed in plain English"
git push origin my-feature-name
```

Then open a **Pull Request** on GitHub so the team can review before merging.

---

## ❓ FAQ

**I don't know how to code. Can I still contribute?**
Yes! Use Claude to write the code. Describe what you want, paste the result into the right file, and commit it.

**Something broke. What do I do?**
Don't panic! Ask Claude to help debug — paste the error message and describe what you were trying to do.

**How do I know what to work on?**
Check the **Issues** tab: https://github.com/JanaMW27/woo-project/issues

**Who do I ask for help?**
Reach out to Jana (project owner) or ask Claude!

---

## 🔗 Useful Links

| Resource | Link |
|---|---|
| GitHub Repo | https://github.com/JanaMW27/woo-project |
| Claude AI | https://claude.ai |
| Docker Desktop | https://www.docker.com/products/docker-desktop |
| WordPress Docs | https://developer.wordpress.org |
| WooCommerce Docs | https://developer.woocommerce.com |
| Git Basics | https://docs.github.com/en/get-started |

---

*Welcome to the team! 🎉 You've got this.*
