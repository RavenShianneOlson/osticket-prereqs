<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- **Microsoft Visual C++**: Required for certain components of the setup process.

- **MySQL Server**: Used as the database backend for osTicket.

- **IIS (Internet Information Services)**: Needed for hosting the web application.

- **PHPManager**: Used for managing PHP configurations within IIS.

- **osTicket**: The support ticket system being installed.

- **HeidiSQL**: Optional but recommended for managing MySQL databases.




# Gear Up! A Step-by-Step Guide to Installing osTicket

Get ready to conquer the world of help desk systems! This guide will be your trusty companion as we walk through setting up osTicket on your Windows 10 machine. Let's dive in!

## Step 1: Enabling the Essentials

First things first, we need to activate some key features in your Control Panel. Think of them as the building blocks for your awesome new help desk! Here's how to unlock their power:

1. Open the Control Panel (Search for it in the Start menu if you need help finding it).
2. Select "Programs and Features."
3. Click on "Turn Windows features on or off."
4. Navigate to "World Wide Web Services" and then "Application Development Features."
5. Check the box next to "CGI" and head over to "Common HTTP Features."
6. Make sure all the boxes here are checked for maximum functionality.

### Success Check!

Let's see if everything worked as planned. Open your web browser and type in "localhost" in the address bar. Hit enter, and if you see a webpage titled "Internet Information Services," you're golden!

## Step 2: Creating a PHP Playground

Now, let's create a dedicated space for PHP to work its magic. We'll make a new folder on your C drive just for it, following these simple steps:

1. Open your Downloads folder.
2. Navigate to "This PC" and then open the Windows (C:) drive.
3. Right-click anywhere in the blank space and select "New Folder."
4. Name the new folder "PHP" – clear and concise!

## Step 3: Downloading Microsoft Visual C++ (Optional but Important)

This little helper program might be needed down the line, so let's grab it just in case. Head over to [Microsoft's website](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170) and download the appropriate version for your system.

## Step 4: Installing Your Database (MySQL Server)

Here comes the brain of your help desk! We'll set up a MySQL server to store all your important ticket information. Just follow the prompts and choose a strong password – this keeps your data safe. Here's a breakdown:

1. Download the MySQL server from [MySQL's website](https://www.mysql.com/) (make sure to choose the appropriate version for your system).
2. Run the downloaded installer and follow the on-screen instructions.
3. When prompted, select "Typical install" for a smooth setup.
4. Leave the "Launch the MySQL configuration wizard" box checked (it's essential for setting a password).
5. Click "Finish" and then "Next" to finalize the setup.
6. Select "Standard Configuration" when prompted and click "Next" again.
7. Ensure "Install as Windows Service" is checked (it keeps things running smoothly).
8. Leave the server name as "MySQL" and click "Next."
9. Now comes the important part – choose a secure password and remember it well! This will be used to access your database.
10. You won't be prompted for a username, but it will be "root" by default.
11. Click "Execute" and "Finish" once the installation is complete.

## Step 5: Configuring PHP in IIS

This step involves introducing IIS (your web server) to PHP. We'll use a handy tool called PHP Manager to make things smooth. Here's how to get it done:

1. Locate the Internet Information Services (IIS) icon and right-click on it. Select "Run as administrator" to ensure we have the necessary permissions.
2. Open PHP Manager within IIS. You might see a warning about PHP not being registered yet – no worries, we'll fix that!
3. Click "Register New PHP Version."
4. Use the "Browse" button to navigate to the "PHP" folder we created on your C drive in Step 2.
5. Within the folder, locate the file named "php-cgi" and select it.

**Important Note:** If you don't see the file, make sure the dropdown menu above the "Open" and "Cancel" buttons says "PHP executable."

### Let's Restart!

While still within IIS, select the server name in the top left corner under "Connections." Navigate to the upper right-hand section under "Actions" and select "Manage Server" followed by "Restart." This ensures the changes we just made take effect.
