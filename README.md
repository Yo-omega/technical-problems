# SolvedProblems
give the solutions of solved problems that I interface randomly. 


- #### How to fix no ethernet adapter in Kali Linux.
1. go to /etc/network/
2. open the file `interfaces`  with text editor.
3. type the following :
   
       auto eth0
       iface eth0 inet dhcp

5. reboot the system

----

- #### Auto commit & push 


1. Create a file `gitpush.sh`.
2. Edit it :
      ```bash
      #!/bin/bash
      
      # Change directory to your Git repository
      cd /path/to/your/repository
      
      # Add all changes to the staging area
      git add .
      
      # Check if a commit message is provided as an argument
      if [ -z "$1" ]; then
          # If no message is provided, use a default message
          commit_message="Auto commit"
      else
          # If a message is provided, use it as the commit message
          commit_message="$1"
      fi
      
      # Commit changes with the provided or default message
      git commit -m "$commit_message"
      
      # Push changes to the remote repository (assuming tremote='origin' and branch='main')
      git push origin main
      ```
3. Save the file and exit the text editor.
4. Make the script executable by running the following command in your terminal:

         chmod +x gitpush.sh
5. Move the script to a directory that is in your system's PATH. 
      ###### For example, you can move it to /usr/local/bin/:

         sudo mv gitpush.sh /usr/local/bin/

   

6. With this modification, you can run the script like this:


         gitpush.sh "your actual commit message"


----

- ## restore file status in last commit Git
   
   1. ### find the commit hash of the last commit that had the file:

            git log -p
   
   3. ### revert:

           git checkout <commit_hash> -- <path_to_file> <other_files>

## Change Remote repos for git:

   1. change remote:
   
         git remote set-url origin <url-here>
   
  2. check it:
  ```
         git remote -v
  ```
  
----

## Push to multiple repositories:

just run this command (do not forget to replace the URL with yours)
```
   git remote set-url --add origin git@github.com:user/repo2.git
```


