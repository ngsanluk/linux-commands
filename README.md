# Getting Started with Linux Commands

![](./images/banner.jpeg)

## Cloud Development and Operation

Cloud Development and Operation refers to the day-to-day work involved in developing and operating software applications that run on the cloud. It is widely known as **DevOps**.

- **Dev** = Software Development
- **Ops** = Infrastructure Operations

Linux is widely used for Virtual Machines (VMs) and Containers. To operate cloud servers, users often connect through a Terminal application.

A terminal is a **Command-Line Interface (CLI)**, so becoming familiar with basic Linux commands is an essential skill for cloud developers and operators.

---

# Show System Information

| Command | Function                 | Examples                                   |
| ------- | ------------------------ | ------------------------------------------ |
| `uname` | Print system information | `uname -a`<br>`uname -n`<br>`uname --help` |
| `lscpu` | List CPU information     | `lscpu`                                    |
| `lsusb` | List USB information     | `lsusb`                                    |

---

# Frequently Used Commands

| Command | Function                               | Examples                                                                     |
| ------- | -------------------------------------- | ---------------------------------------------------------------------------- |
| `pwd`   | Show the current working directory     | `pwd`                                                                        |
| `ls`    | List contents of the current directory | `ls`<br>`ls /`<br>`ls /bin`<br>`ls ~/`<br>`ls -l`<br>`ls -la`<br>`ls --help` |
| `cd`    | Change directory                       | `cd Downloads`<br>`cd /`<br>`cd ~`<br>`cd ..`<br>`cd Documents`              |
| `clear` | Clear the terminal screen              | `clear`<br>Shortcut: `Ctrl + K`                                              |
| `mkdir` | Create a new directory                 | `mkdir my_folder_1`<br>`mkdir my_folder_2`                                   |
| `rmdir` | Remove an empty directory              | `rmdir my_folder_2`                                                          |
| `touch` | Create a new file                      | `touch file1.txt`<br>`touch server.conf`<br>`touch .hidden_file`             |
| `rm`    | Remove files                           | `rm file1.txt`<br>`rm server.conf`                                           |
| `ping`  | Test network connectivity to a host    | `ping www.google.com`<br>`ping 192.168.0.1`<br>`ping 192.168.1.1`            |

---

# Linux System Management Commands

| Command                | Function                                   | Examples                                                                   |
| ---------------------- | ------------------------------------------ | -------------------------------------------------------------------------- |
| `hostname`             | Display the hostname                       | `hostname -I`<br>`hostname --help`                                         |
| `cat /etc/os-release`  | Display Linux operating system information |                                                                            |
| `ip address` or `ip a` | Show IP network settings                   |                                                                            |
| `man`                  | Display a command's manual                 | `man ls`<br>`man mkdir`<br>`man rmdir`<br>`man man`                        |
| `info`                 | Show detailed information about a command  | `info ls`<br>`info mkdir`<br>`info rmdir`<br>`info info`                   |
| `uptime`               | Show system uptime                         | `uptime`<br>`uptime -p`<br>`uptime --pretty`<br>`uptime --help`            |
| `whoami`               | Show current user                          |                                                                            |
| `users`                | Show logged-in users                       |                                                                            |
| `echo`                 | Print text or environment variables        | `echo hello`<br>`echo hello from sunny`<br>`echo $USERNAME`<br>`echo $PWD` |
| `>`                    | Redirect output to a file                  | `echo hi there > hi.txt`<br>`ls / > files.txt`                             |
| `cat`                  | Display file contents                      | `cat hi.txt`<br>`cat files.txt`                                            |
| `env`                  | Display environment variables              |                                                                            |
| `su`                   | Switch user                                | `su peter`<br>`sudo su -`                                                  |
| `sudo`                 | Execute commands as root user              | `sudo ls /root`<br>`sudo -i`<br>`sudo -s`                                  |
| `which`                | Show the location of a command             | `which ls`<br>`which ip`                                                   |

---

# System Prompt

## Regular User Prompt

```bash
ubuntu@hostmane:~$
```

## Root User Prompt

```bash
root@hostname:~#
```

---

# Using the TAB Key for Command Completion

Type `ls` and then press **TAB** twice to see all commands that begin with "ls".

---

# Path Name Completion

For long folder or file names, type the first few characters and press **TAB** to automatically complete the name.

Example:

```bash
cd Doc
```

---

# Linux Root Folder Structure

The root folder is represented by:

```bash
/
```

It is the top-level directory in the filesystem.

> **Note:** The root folder (`/`) is different from the root user account (`root`). They simply share the same name.

Common directories:

| Directory | Purpose                         |
| --------- | ------------------------------- |
| `/bin`    | Essential command binaries      |
| `/boot`   | Boot loader files               |
| `/dev`    | Device files                    |
| `/etc`    | System configuration files      |
| `/home`   | User home directories           |
| `/lib`    | Shared libraries                |
| `/media`  | Removable media mount point     |
| `/mnt`    | Temporary mount point           |
| `/opt`    | Optional software packages      |
| `/sbin`   | System administration binaries  |
| `/srv`    | Service data                    |
| `/tmp`    | Temporary files                 |
| `/usr`    | User applications and utilities |
| `/var`    | Variable files such as logs     |
| `/root`   | Root user's home directory      |
| `/proc`   | Process and system information  |

---

# Practical Exercise

You are asked to create a website folder structure with multiple levels of directories and subdirectories.

## Commands Used

| Command | Example                                         |
| ------- | ----------------------------------------------- |
| `mkdir` | Create a folder:<br>`mkdir xxxxxxxx-web`        |
| `rmdir` | Remove an empty folder:<br>`rmdir xxxxxxxx-web` |
| `cd`    | Change directory:<br>`cd xxxxxxxx-web`          |
| `ls`    | List contents:<br>`ls`<br>`ls -l`               |
| `pwd`   | Show current directory:<br>`pwd`                |
| `clear` | Clear the terminal:<br>`clear`                  |
| `touch` | Create a file:<br>`touch index.html`            |

---

## Install and use `tree` command

Use the `tree` command to display your completed directory structure.

Install the `tree` utility with:

```bash
sudo apt install tree
```

Then display your project structure:

```bash
tree
```

## Expected Website Structure

After completing the lab, your project should have the following structure:

```text
xxxxxxxx-web/
├── about.html
├── css/
├── images/
│   ├── high/
│   ├── low/
│   └── mid/
├── index.html
├── products.html
└── videos/
    ├── high/
    ├── low/
    └── mid/
```

---

# `apt` Command – Advanced Package Tool

Below are the most used `apt` sub-commands

- `list` – list packages based on package names
- `search` – search in package descriptions
- `show` – show package details
- `install` – install packages
- `reinstall` – reinstall packages
- `remove` – remove packages
- `autoremove` – remove automatically all unused packages
- `update` – update list of available packages
- `upgrade` – upgrade the system by installing/upgrading packages
- `full-upgrade` – upgrade the system by removing/installing/upgrading packages
- `edit-sources` – edit the source information file
- `satisfy` – satisfy dependency strings

## `apt` Command Examples

| Command                     | What it does            |
| --------------------------- | ----------------------- |
| `sudo apt install tree`     | Install tree package    |
| `sudo apt remove tree`      | Remove tree package     |
| `sudo apt search tree`      | Search for tree package |
| `sudo apt list --installed` | List the packages       |

## `systemctl` Command - System Service Control

systemctl is a Linux command-line utility used to control and manage systemd and services. You can think of systemctl as a control interface for the systemd init service, allowing you to communicate with **systemd** and perform operations.

In **systemd** language, a service or a unit is a resource or an object that systemd is aware of and knows how to address.

## Check System Service Status

```
sudo systemctl status
```

**Note**: executing `systemctl status` displays the current state of services, queued jobs, failed units, session scopes, and the control group (CGroup) process hierarchy.

## Other `systemctl` Commands

### Start a Service

The systemctl command manually starts a service with:

`systemctl start {servicename}`

---

### Stop a Service

To manually stop a service with systemctl, type:

`systemctl stop {servicename}`

---

### Restart a Service

Instead of manually starting or restarting a service, it's faster to simply use the restart subcommand:

`systemctl restart {servicename}`

---

### Enable a Service

Starting and stopping a service only applies to the current runtime. What if admins need to configure the service to start when the system boots? The term for that action is enable:

`systemctl enable {servicename}`

---

### Disable a Service

Likewise, if admins need to configure a service to not start when the system boots, they can type the following command to disable the service:

`systemctl disable {servicename}`

---

## Exercising `apt` and `systemctl` Commands

1. Update Ubuntu repository package lists:

- `sudo apt update`

2. Install **nginx** package:

- `sudo apt install nginx`

3. Start and verify the service running status:

- `sudo systemctl start nginx`
- `sudo systemctl status nginx`

4. Change the website homepage:
   Navigate to the web root directory and open the homepage file in nano:

- `cd /var/www/html`
- `ls`
- `sudo nano index.nginx-debian.html`

5. Modify the HTML file:

- Add your full name inside the page heading tag: `<h1>Welcome to nginx! (SUNNY)</h1>`
- Save and exit nano:
- Press **CTRL + O** to save code changes.
- Press **Enter** to confirm filename.
- Press **CTRL + X** to exit code editor.

6. Verify the change:

- Reload your page in the web browser (navigate to http://your-server-ip).
