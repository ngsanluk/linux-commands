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

# Expected Website Structure

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

# Install and use `tree` command

Use the `tree` command to display your completed directory structure.

Install the `tree` utility with:

```bash
sudo apt install tree
```

Then display your project structure:

```bash
tree
```
