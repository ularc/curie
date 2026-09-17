Getting Started
###############

.. _usage-agreemet:

Usage Agreement
===============

Please ensure that you have read :ref:`Curie's System Use Policies <curie_system_use_policies>`
and have agreed to it before requesting an account.

Connecting to Curie
======================

There are a couple of ways to connect and utilize the Curie system. Please note, that you must be connected to either the University of Louisville campus network or the UofL Global Protect VPN using a NIST 800-171 secured system.

SFTP
----

**Client - Preferred**

  #. Open your preferred SFTP client (e.g., CyberDuck and Filezilla)
  
  #. Enter the following information in the client
  
      .. list-table:: SFTP Client Info
          :header-rows: 1

          * - Key
            - Value
          * - Host
            - curie.rc.louisville.edu
          * - Username
            - your ULINK ID (i.e., fmlast01)
          * - Password
            - Your University of Louisville Password
          * - Port
            - 22
      
      .. note::
        
        If your client needs a URL rather than ``host`` + ``port`` then you can try ``sftp://curie.rc.louisville.edu`` instead
  
  #. Follow the DUO prompt

**Command Line**
  
  #. Open a terminal session

  #. Type the command:
  
      .. code-block::
  
          sftp ${USER}@curie.rc.louisville.edu
  
  #. Enter your UofL password, and follow the DUO instructions.

  This will start an SFTP session, and after login you will be in a private directory on Curie. You can use the following commands to interact with the session:
  
  .. list-table:: SFTP commands
      :header-rows: 1

      * - Command
        - Meaning
      * - ls
        - List files and directories
      * - cd
        - Change directory
      * - pwd
        - Display current directory
      * - get
        - Download a file from the Data Store
      * - put
        - Upload a file to the Data Store
      * - mkdir
        - Create a directory
      * - rmdir
        - Remove an empty directory
      * - rm
        - Delete a file

  Example

  .. code-block:: bash

    C:\Users\fmlast01> sftp fmlast01@curie.rc.louisville.edu
    This system is the property of the University of Louisville.

    Use of the system is for authorized users only. It is the policy of the
    University to protect and safeguard the protected health information,
    created, acquired and maintained in accordance with the Privacy
    Regulations promulgated pursuant to the Health Insurance Portability
    and Accountability Act of 1996 and all applicable state laws.

    Use of your account constitutes your approval and acceptance of this
    agreement. Acceptance of this agreement is a condition of use.

    IMPORTANT!

    USER DOCUMENTATION: https://ularc.github.io/rosalind/

    Please type your University of Louisville password.
    REMARK: Even if you don't see any characters in the
    prompt, your input is recorded.

    AFTER TYPING YOUR PASSWORD, check your phone for a
    DUO prompt.

    (fmlast01@curie.rc.louisville.edu) password:
    (fmlast01@curie.rc.louisville.edu) Duo two-factor login for fmlast01

    Enter a passcode or select one of the following options:

    1. Duo Push to XXX-XXX-4927
    2. Phone call to XXX-XXX-4927
    3. SMS passcodes to XXX-XXX-4927

    Passcode or option (1-3): 1
    Success. Logging you in...
    Success. Logging you in...
    Authorized users only. All activity may be monitored and reported.
    Last login: Thu Sep 17 12:19:08 2026 from 136.165.91.166
    sftp> 
    sftp> pwd
    Remote working directory: /home/fmlast01
    sftp> 
    sftp> ls
    sftp> 
    sftp> put C:\Users\fmlast01\Downloads\Image.jpg .
    Uploading C:/Users/fmlast01/Downloads/Image.jpg to /home/fmlast01/./Image.jpg
    Image.jpg                                                                                                                        100% 7912KB   1.5MB/s   00:05
    sftp> 
    sftp> get /home/fmlast01/./Image.jpg .\mytestimage.jpg
    Fetching /home/fmlast01/./Image.jpg to ./mytestimage.jpg
    Image.jpg                                                                                                                        100% 7912KB 517.7KB/s   00:15
    sftp> 
    sftp> ls
    Image.jpg
    sftp> 
    sftp> pwd
    Remote working directory: /home/fmlast01
    sftp> 
    sftp> exit

SSH
---
  #. Open your SSH client of choice (or a terminal session)
  
  #. Use the following information to connect
      .. list-table:: SSH Information
          :header-rows: 1
          
          * - Key
            - Value
          * - Host
            - curie.rc.louisville.edu
          * - Username
            - your ULINK ID (i.e. fmlast01)
          * - Password
            - Your University of Louisville Password
          * - Port
            - 22
  
  #. Follow the DUO prompt
  
.. note::
    
  Upon connecting to Curie, by default, you will be in your private directory.