# VPS SETUP

### STEP 1

<pre><code id="example-code">ssh root@your_ip_adress</code></pre>

Then enter your password

### STEP 2

Updated backdated packages

<pre><code id="example-code">sudo apt update</code></pre>
<pre><code id="example-code">sudo apt upgrade</code></pre>

### STEP 3

Enabling and Configuring UFW (Uncomplicated Firewall)

<pre><code id="example-code">sudo ufw enable</code></pre>
<pre><code id="example-code">sudo ufw allow 22</code></pre>

Check allow port status

<pre><code id="example-code">sudo ufw status</code></pre>

### STEP 3 Install NodeJs

Download and install nvm:

<pre><code id="example-code">curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash</code></pre>
<pre><code id="example-code">nvm -v</code></pre>
<pre><code id="example-code">nvm install 22</code></pre>

Note: If you get any error then  try this

<pre><code id="example-code">export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # Loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # Loads nvm bash_completion
</code></pre>



## STEP 4

GitHub connection

<pre><code id="example-code">ls -al ~/.ssh</code></pre>
<pre><code id="example-code">ssh-keygen -t rsa -b 4096 -C "yourGithubemail"</code></pre>
<pre><code id="example-code">eval "$(ssh-agent -s)"</code></pre>
<pre><code id="example-code">cat ~/.ssh/id_rsa.pub</code></pre>

Then copy the ssh key and paste it on your SSH and GPG keys on your GitHub, click new SSH key, write project name and paste the key

<pre><code id="example-code">ssh -T git@github.com</code></pre>

### STEP 5

Setup nginx

<pre><code id="example-code">sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw reload</code></pre>


### Start your app with pm2


<pre><code id="example-code">pm2 start npm --name "nextjs-app" -- start</code></pre>
