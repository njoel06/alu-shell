Processes and Signals
This repository contains a series of Bash scripts that demonstrate various aspects of process management and signal handling in Linux systems. The scripts cover fundamental concepts such as Process IDs (PIDs), process listing, signal trapping, and daemon management.

Learning Objectives
By completing this project, you should be able to explain:

General Concepts
What a PID (Process ID) is

What a process is in Linux

How to find a process's PID

How to kill/terminate a process

What signals are in Linux

The two signals that cannot be ignored

Practical Skills
Writing Bash scripts that manage their own processes

Handling different types of signals (SIGTERM, SIGINT, SIGQUIT)

Creating and managing daemon processes

Implementing init scripts for process management

Script Descriptions
0. 0-what-is-my-pid
Displays its own Process ID (PID) using the special variable $$.

1. 1-list_your_processes
Shows a hierarchical list of all currently running processes for all users, including those without a TTY.

2. 2-show_your_bash_pid
Displays processes containing "bash" in their command line, making it easy to identify Bash process PIDs. Uses ps with a grep filter.

3. 3-show_your_bash_pid_made_easy
Displays PID and process name for processes containing "bash" using pgrep.

4. 4-to_infinity_and_beyond
An infinite loop that prints "To infinity and beyond" every 2 seconds. Can be terminated with Ctrl+C.

5. 5-dont_stop_me_now
Kills the 4-to_infinity_and_beyond process using pkill.

6. 6-stop_me_if_you_can
Stops the 4-to_infinity_and_beyond process without using kill or killall commands.

7. 7-highlander
An enhanced version of 4-to_infinity_and_beyond that traps SIGTERM signals and responds with "I am invincible!!!" instead of terminating.

8. 8-beheaded_process
Kills the 7-highlander process.

9. 10-process_and_pid_file
Creates a PID file, runs indefinitely, and handles multiple signals:

SIGTERM: Prints "I hate the kill command" and exits

SIGINT: Prints "Y U no love me?!"

SIGQUIT: Cleans up PID file and exits

10. manage_my_process & 11-manage_my_process
A daemon management system:

manage_my_process: A daemon that writes "I am alive!" to a file every 2 seconds

11-manage_my_process: An init script that manages the daemon with start, stop, and restart functions

Key Concepts Demonstrated
PID (Process ID)
Every process in Linux has a unique numerical identifier called a Process ID. Scripts like 0-what-is-my-pid demonstrate how to access this.

Signals
Signals are software interrupts sent to processes. These scripts demonstrate:

SIGTERM (15): Termination signal

SIGINT (2): Interrupt from keyboard (Ctrl+C)

SIGQUIT (3): Quit from keyboard

Signal Handling
The trap command is used to catch signals and execute specific actions. Two signals that cannot be ignored or trapped are:

SIGKILL (9)

SIGSTOP (19)

Process Management
These scripts show various ways to:

List processes (ps, pgrep)

Kill processes (pkill, kill)

Create background processes (daemons)

Manage processes with PID files

Daemon Processes
Daemons are background processes that run independently of a terminal. The manage_my_process script demonstrates creating a simple daemon, while 11-manage_my_process shows how to implement an init script to manage it.

Technical Requirements
All scripts are written for Ubuntu 20.04 LTS

Scripts are executable and pass Shellcheck validation

Each script starts with #!/usr/bin/env bash

Each script has a descriptive comment on the second line

All files end with a newline character
