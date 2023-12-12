<h1>File Permissions in Linux</h1>

<h2> Project Description</h2>
The file permissions for certain files and directories within the projects directory need to be updated. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep the system secure. 
<br />


<h2>Program steps </h2>
To complete this task, I performed the following tasks:
<p align="left">
<h3>Check file and directory details</h3> 
The first line of the screenshot displays the command I entered, and the other lines display the output. The code lists all contents of the projects directory. I used the ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named drafts, one hidden file named .project_x.txt, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory. <br/> <br />
<img src="https://imgur.com/B4QEoZJ.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
 <h3>Describe the permissions string</h3> 
The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows: <br/><br/>
   - <b>1st character:</b> This character is either a d or hyphen (-) and indicates the file type. If it’s a d, it’s a directory. If it’s a hyphen (-), it’s a regular file.<br/>
   - <b>2nd-4th characters:</b> These characters indicate the read (r), write (w), and execute (x) permissions for the user. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.<br/>
   - <b>5th-7th characters:</b> These characters indicate the read (r), write (w), and execute (x) permissions for the group. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.<br/>
   - <b>8th-10th characters:</b> These characters indicate the read (r), write (w), and execute (x) permissions for other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.
<br />
<br />
  
  <h3>Change file permissions</h3> 
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The chmod command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the project_k.txt file. After this, I used ls -la to review the updates I made. <br/> <br/> 
<img src="https://imgur.com/Mp3SDWh.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
  <h3>Change file permissions on a hidden file</h3> 
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I know .project_x.txt is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r.   <br/> <br />
<img src="https://imgur.com/T1lyFlQ.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
<h3>Change  directory permissions</h3> 
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I previously determined that the group had execute permissions, so I used the chmod command to remove them. The researcher2 user already had execute permissions, so they did not need to be added.  <br/> <br />
<img src="https://imgur.com/S7RMgbN.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />



<h2>Summary of the project </h2>

The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories.
