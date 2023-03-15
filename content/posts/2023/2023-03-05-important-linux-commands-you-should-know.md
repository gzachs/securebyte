---
title: "Important Linux Commands You Should Know"
date: 2023-03-05T17:49:18+04:00
draft: false
categories: Linux
tags:
  - Linux Fundamentals
ShowToc: true
TocOpen: true
author: Gino
---

Here are some notes on [Luke Smith's quick overview](https://www.youtube.com/watch?v=Gl4DKyicKKg) of some basic Linux commands to get file and system information.
As always, the best way to remember these commands is to set up a [Linux VM](https://www.virtualbox.org/wiki/Downloads) and practice.

## date
Shows the current date and time on the system.

## cal
Displays the calendar for the current month, with the current day highlighted. Try out different variations (man cal) like: 
cal -3
cal february 313

## df -h
Displays disk usage statistics for all partitions and mounted file systems including total size, used space, and available space. -h makes the output more human-readable.

## du -h {path to file/directory}
Useful for showing the disk usage of a particular file or directory in human-readable format.

## ps aux
Outputs a list of all running processes on the system including process ID (PID), CPU and memory usage, and start time.

## ps aux | grep {process name/PID}
Basically pipes the ps aux output into grep. Searches the process list for a specific process name or PID and displays detailed information for any matching processes.

## pidof {process name}
Displays the process ID (PID) of a running process by its name.

## kill {PID}
Terminates a process, if it's running, based on the input PID.

## htop
Displays a sophisticated system resource monitor and process viewer. 

## uname -a
Shows all OS and kernel version.

## ip addr
Prints the network configuration information for all network interfaces on the system, including IP addresses, netmasks, and broadcast addresses.