# Laragon Setup, Database Migration, XAMPP Uninstallation, and Laravel Project Execution Guide

## 1.0 Introduction
Laragon is a local development used to develop and test web applications on a computer. It provides tools for running web servers, databases, and web applications locally.

## 2.0 Download Laragon
1. Visit the official Laragon GitHub releases page: [Laragon] (https://github.com/leokhoa/laragon/releases/tag/6.0.0) 
2. Download the appropriate Laragon installer. (Choose laragon-wamp.exe to download it)

   <img width="890" height="361" alt="image" src="https://github.com/user-attachments/assets/ca8e1ded-d9ef-48a3-a193-cf05b3dc906b" />

4. Wait for the download to complete.

## 3.0 Install Laragon
1. Run the downloaded installer.
2. Select English as the setup language and click OK.

<img width="498" height="279" alt="image" src="https://github.com/user-attachments/assets/1b90d6b2-9a66-48ee-95d3-d96ff0aac9dd" />
   
3. Select the Destination Location and click Next. (For example, use `D:\laragon` if you want to avoid using additional space on your C: drive.)

> **Note:** Make sure the selected drive has sufficient free space.

<img width="710" height="544" alt="image" src="https://github.com/user-attachments/assets/12ea258a-45c8-49b6-a81c-b18298b5ad8e" />

4. In Auto start, Auto detect and create virtual hosts window, Tick all the box (Run Laragon when Windows starts, Auto virtual hosts, and Add Notepad++ & Terminal to the Right-Click Menu) and click Next button.

<img width="710" height="541" alt="image" src="https://github.com/user-attachments/assets/9d49b842-da56-4adf-8cba-9e67fe9a196e" />

5. Click Install button.

<img width="712" height="544" alt="image" src="https://github.com/user-attachments/assets/668a57a3-6604-49a7-98d5-e2f8cc1afa17" />

6. Wait until the installation process is complete.

<img width="715" height="547" alt="image" src="https://github.com/user-attachments/assets/7dd70ecf-c6ea-4f99-9b72-dbdf87b78fd2" />

7. Click Finish button.

<img width="711" height="544" alt="image" src="https://github.com/user-attachments/assets/04ed542e-e3dd-46a2-862a-9fe26a9857f5" />

## 4.0 Launch Laragon
1. Open Laragon.
2. Start the database service. Click Start All button.
   
<img width="839" height="559" alt="image" src="https://github.com/user-attachments/assets/c5d2bc83-ab0e-4fd8-b9b9-72566f12a8d6" />

3. Verify that the web server and database services start successfully.

## 5.0 Create a Database
1. Open Laragon
2. Start the database service. Click Database button

<img width="834" height="559" alt="image" src="https://github.com/user-attachments/assets/ee2a625a-3646-41cc-8554-1b7a2392b6c6" />

3. Open the database management tool available in your installation, such as HeidiSQL.

<img width="851" height="594" alt="image" src="https://github.com/user-attachments/assets/b8d5f4a6-0472-4b03-b84b-f2439d0b5a55" />

4. Right click on Laragon.MySQL and create a new database.

<img width="712" height="261" alt="image" src="https://github.com/user-attachments/assets/4b2a53b8-9367-43a8-9b65-a258ba15f805" />

5. Enter a suitable database name and confirm.

<img width="394" height="319" alt="image" src="https://github.com/user-attachments/assets/9f9ece95-7089-4498-96e0-790f59c3e9bf" />

## 6.0 Create a Laravel Project in Laragon
### 6.1 Start Laragon
1. Open Laragon.
2. Click Start ALL button to start the Apache and MySQL services.
3. Make sure the services are running successfully.

### 6.2 Create a Laravel Project
1. Right-click on an empty space inside Laragon.
2. Select Quick App > Laravel

<img width="829" height="555" alt="image" src="https://github.com/user-attachments/assets/e9893e30-7dfc-46a8-af91-7ced6f771079" />

3. Enter your desired project name, for example `my-laravel-app`.
4. Click OK or confirm the project creation.
5. Wait for Laragon to finish creating the Laravel project.

### 6.3 Open the Laravel Project in VS Code
1. Open VS Code
2. Click File -> Open Folder
3. Navigate to your Laragon www directory.

<img width="767" height="540" alt="image" src="https://github.com/user-attachments/assets/ad4618c9-4d19-4cb0-99ba-ecb148677fb3" />

4. Select your Laravel project folder, for example here is `test1`.
5. Click Select Folder button.

### 6.4 Open the Terminal in VS Code
1. In VS Code, click Terminal -> New Terminal.
2. Check that the terminal is inside your Laravel project directory.
   The terminal path should look like this:
   ```bash
   PS D:\laragon\www\test1>
   ```
   If the terminal is in another directory, type:
   ```bash
   cd D:\laragon\wwww\test1
   ```
   Press Enter.
3. Check PHP
   
   Type the following command:
   ```bash
   php -v
   ```
   
   If PHP is configured correctly, its version information will appear.
   > [!Note] If you see an error saying that php is not recognised, use the Laragon Terminal instead, or configure PHP in your windows PATH environment variable.

4. Start the Laravel Development Server

   In the terminal, type:
   ```bash
   php artisan serve
   ```

   Press Enter.

   If successful, the terminal will display a message similar to:

   ```text
   INFO  Server running on [http://127.0.0.1:8000].
   ```

5. Open the Laravel Project in a Browser

### 6.5 Open the Laravel Project in a Browser
1. Copy the link given in the terminal before this.
2. Open Google Chrome or another browser.
3. Paste the link.
4. Click Enter
5. The Laravel welcome page should appear.

<img width="1707" height="940" alt="image" src="https://github.com/user-attachments/assets/9e2de01a-2ba3-4f39-b45c-f3e6749d3e7f" />

### 6.6 Stope the Development Server
When you have finished testing the project:

1. Return to the terminal where Laravel is running.
2. Press Ctrl + C to stop the development server.

You can start it again later by repeating step 4 in **subsection 6.4 Open the Terminal in VS Code.**

## 7.0 Import an Existing Database

To migrate a database from XAMPP to Laragon:

1. Export the database from phpMyAdmin in XAMPP as an SQL file.
2. Start the database service in Laragon.
3. Open HeidiSQL or another compatible database management tool in your Laragon.
4. Create a new database with the required name.
5. Import or execute the exported SQL file.
6. Verify that the tables and records have been imported successfully.

## 8.0 Uninstalling XAMPP

To make sure all your databases in XAMPP not deleted completely and cannot recover back, we need to backup the databases first. Don't delete the XAMPP folder until you've confirmed your databases are safe in Laragon.

1. Open Windows settings ( Press Windows + I -> Select Apps -> Installed Apps )
2. Search for XAMPP, click the three dots beside it, then choose Uninstall if available.
3. Now, XAMPP completely removed from your laptop.

After uninstalling, check whether X://xampp still exists.
- If it contains files you still need, keep them or back them up.
- If your databases are safely transferred and you no longer need XAMPP files, you can delete the remaining folder.
