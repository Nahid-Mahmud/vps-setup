# VPS SETUP

### STEP 1
<pre>
  <code id="example-code">
   ssh root@your_ip_adress
  </code>
</pre>
Then enter your password

### STEP 2
Updated backdated packges
<pre>
  <code id="example-code">
   sudo apt update
  </code>
</pre>
<pre>
  <code id="example-code">
   sudo apt upgrade
  </code>
</pre>

### STEP 3
Enabling and Configuring UFW (Uncomplicated Firewall)

<pre>
  <code id="example-code">
   sudo ufw enable
  </code>
</pre>

<pre>
  <code id="example-code">
   sudo ufw allow PORT
  </code>
</pre>

Check allow port status 

<pre>
  <code id="example-code">
   sudo ufw status
  </code>
</pre>

### STEP 3
Install NVM

<pre>
  <code id="example-code">
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
  </code>
</pre>

