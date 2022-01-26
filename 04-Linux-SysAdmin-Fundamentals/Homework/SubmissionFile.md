## Week 4 Homework Submission File: Linux Systems Administration

Please edit this file by adding the solution commands on the line below the prompt.

Save and submit the completed file for your homework submission.


### Step 1: Ensure/Double Check Permissions on Sensitive Files

1. Permissions on `/etc/shadow` should allow only `root` read and write access.

    - Command to inspect permissions: ls -l /etc/shadow

    - Command to set permissions (if needed): sudo chmod 600 /etc/shadow

2. Permissions on `/etc/gshadow` should allow only `root` read and write access.

    - Command to inspect permissions: ls -l /etc/gshadow

    - Command to set permissions (if needed): sudo chmod 600 /etc/gshadow

3. Permissions on `/etc/group` should allow `root` read and write access, and allow everyone else read access only.

    - Command to inspect permissions: ls -l /etc/group

    - Command to set permissions (if needed): sudo chmod 644 /etc/group

4. Permissions on `/etc/passwd` should allow `root` read and write access, and allow everyone else read access only.

    - Command to inspect permissions: ls -l /etc/passwd

    - Command to set permissions (if needed): sudo chmod 644 /etc/passwd

### Step 2: Create User Accounts

1. Add user accounts for `sam`, `joe`, `amy`, `sara`, and `admin`.

    - Command to add each user account (include all five users): 
   sudo useradd joe (repeat)
   amy
   sara
   admin
   sam


2. Ensure that only the `admin` has general sudo access.

    - Command to add `admin` to the `sudo` group: sudo usermod -g sudo admin

### Step 3: Create User Group and Collaborative Folder

1. Add an `engineers` group to the system.

    - Command to add group: sudo addgroup engineers

2. Add users `sam`, `joe`, `amy`, and `sara` to the managed group.

    - Command to add users to `engineers` group (include all four users):
    - sudo usermod -g engineers sam (repeat command with diff names)
    - joe
    - amy
    - sara

3. Create a shared folder for this group at `/home/engineers`.

    - Command to create the shared folder: sudo mkdir /home/engineers

4. Change ownership on the new engineers' shared folder to the `engineers` group.

    - Command to change ownership of engineer's shared folder to engineer group: sudo chown :engineers /home/engineesr

### Step 4: Lynis Auditing

1. Command to install Lynis: sudo apt install Lynis

2. Command to see documentation and instructions: man Lynis

3. Command to run an audit: sudo Lynus audit system

4. Provide a report from the Lynis output on what can be done to harden the system.

    - Screenshot of report output: screenshot included
   
![image](https://user-images.githubusercontent.com/95587197/151196324-edc91451-26d7-401b-a2ff-4456077f4ff5.png)



### Bonus
1. Command to install chkrootkit: apt install chkrootkit-y

2. Command to see documentation and instructions: man chkrootkit 

3. Command to run expert mode: sudo chkrootkit -x

4. Provide a report from the chrootkit output on what can be done to harden the system.
    - Screenshot of end of sample output:  ![image](https://user-images.githubusercontent.com/95587197/151196385-3affbdf5-01ff-4062-8438-87dddb6b1489.png)


---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
