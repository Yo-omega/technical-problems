# GIT repository:

## Status and time machines:

1. ### Restore file status in the last commit Git
   
   1.  find the commit hash of the last commit that had the file:

            git log -p
   
   2.  revert:

           git checkout <commit_hash> -- <path_to_file1> <path_to_file2> <path_to_file3..etc>

       
2. ### Change Remote repos for git:
    - if you want to change where you are pushing/pulling from. 
         1. change remote:
         
                  git remote set-url origin <url-here>
         
        2. check it:
        
                  git remote -v
        
   - if you want to Push to multiple repositories:
   
     ```
            git remote set-url --add origin git@github.com:user/repo2.git
     ```
   
     
