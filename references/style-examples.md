# Style Examples: Good vs. Bad

Common patterns with before/after examples.

---

## Titles

❌ **Avoid** (tool-focused):
> How To Use Nginx on Ubuntu 22.04

✅ **Prefer** (goal-focused):
> How To Host a Website with Nginx on Ubuntu 22.04

---

## Avoiding Condescending Words

❌ **Avoid**:
> Simply run this command to easily configure your server. It's straightforward and just takes a moment.

✅ **Prefer**:
> Run the following command to configure your server:

---

## Command Explanations

❌ **Avoid** (command with no context):
> ```bash
> sudo ufw allow OpenSSH
> sudo ufw enable
> ```

✅ **Prefer** (explain before running):
> Next, you'll enable UFW (Uncomplicated Firewall) to restrict which ports can accept connections. First, allow SSH connections so you don't lock yourself out of the server:
> ```bash
> sudo ufw allow OpenSSH
> ```
> Then enable the firewall:
> ```bash
> sudo ufw enable
> ```
> UFW will ask you to confirm. Type `y` and press `ENTER`. You'll see output like this:
> ```
> [Output]
> Command may disrupt existing ssh connections. Proceed with operation (y|n)? y
> Firewall is active and enabled on system startup
> ```

---

## Introduction — Outcome Focus

❌ **Avoid** (learning-focused):
> In this tutorial, you will learn how to install and configure the Nginx web server.

✅ **Prefer** (outcome-focused):
> In this tutorial, you will install the Nginx web server and configure it to serve a static website on Ubuntu 22.04.

---

## Prerequisites — Specific vs. Vague

❌ **Avoid** (vague):
> - Familiarity with JavaScript
> - A server with Node.js installed

✅ **Prefer** (specific with links):
> - Familiarity with JavaScript. To build your skills, check out the [How To Code in JavaScript](link) series.
> - Node.js installed on your server, which you can set up by following [How To Install Node.js on Ubuntu 22.04](link).

---

## Person and Voice

❌ **Avoid** (first person singular):
> I recommend using the `-y` flag here to avoid being prompted for confirmation.

✅ **Prefer** (second person):
> Use the `-y` flag here to avoid being prompted for confirmation.

❌ **Avoid** (passive, impersonal):
> The file should be opened and edited.

✅ **Prefer** (direct, second person):
> Open the file with your preferred text editor:

---

## Explaining Configuration Files

❌ **Avoid** (dump config, trust us):
> Add the following configuration to `/etc/nginx/sites-available/default`:
> ```nginx
> server {
>     listen 80;
>     server_name example.com;
>     root /var/www/html;
> }
> ```

✅ **Prefer** (explain each part):
> Open the default Nginx configuration file:
> ```bash
> sudo nano /etc/nginx/sites-available/default
> ```
> Update the file with the following configuration. The `listen 80` directive tells Nginx to accept HTTP traffic on port 80. The `server_name` directive should match your domain name. The `root` directive points to the directory where your website files will live:
> ```nginx
> server {
>     listen 80;
>     server_name your_domain;  # Replace with your actual domain
>     root /var/www/html;
> }
> ```
> Save and close the file when you're done.

---

## Conclusion

❌ **Avoid** (vague):
> In this tutorial, you learned about Nginx. There is much more to explore.

✅ **Prefer** (specific accomplishment + next steps):
> In this tutorial, you installed Nginx on an Ubuntu 22.04 server and configured it to serve a static website over HTTP. Your server is now ready to handle web traffic.
>
> As a next step, you might want to:
> - Secure your site with HTTPS by following [How To Secure Nginx with Let's Encrypt on Ubuntu 22.04](link)
> - Learn to configure server blocks to host multiple sites: [How To Set Up Nginx Server Blocks on Ubuntu 22.04](link)
