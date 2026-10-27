# Getting started

### Quick Start (Simple Run)
To run the app locally without any external database requirement, simply run:
```bash
npm install
node src/index.js
```
The app will use a local SQLite database file (`todo.db`) and listen on port 3000.

- PLEASE NOTE: TCP Port **3000** must be enabled in **Security Group**

---

### Install NodeJS on EC2 Ubuntu instance

#### 1. Update and Install Initial Dependencies 
Run these commands first to ensure your new VM is up to date and has the tools needed to download the installers.

```bash
# Update installed packages
sudo yum update -y

# Install curl, CA certificates, and GnuPG
sudo yum install -y curl ca-certificates gnupg2

# Install build tools for native Node.js modules (including SQLite)
sudo yum install -y gcc-c++ make python3

```

#### 2. Install Node.js (Version 24.x) and Git 
The following block adds the NodeSource repository for the latest Active LTS (Long Term Support) version and installs both Node.js and Git.

```bash
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 24

# Verify the Node.js version:
node -v # Should print "v24.14.1".

# Verify npm version:
npm -v # Should print "11.11.0".
```

### To install NodeJS on Windows / MacOS / Linux Distribution 
URL --> https://nodejs.org/en/download

### Verify the Node.js & npm version:
```bash
node -v # Should print "v24.14.1".
nvm current # Should print "v24.14.1".
npm -v # Should print "11.11.0".
```

### Steps to deploy Locally or on DEV environment
1. Make sure we are root user
```jsx
sudo su
```

2. Clone the app
```jsx
git clone https://github.com/amigo-nishant/getting-started.git
```

3. Change the directory
```jsx
cd getting-started
```
```jsx
sudo chown -R ec2-user:ec2-user /home/ec2-user/getting-started
```
4. Deploy the App
```jsx
npm install
node src/index.js
```

5. Test the App Frontend
```jsx
http://public-ip-ec2:3000/
```
