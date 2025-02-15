#GIT repository:

## Status and time machines:

1. ### Restore file status in the last commit Git
   
   1.  find the commit hash of the last commit that had the file:

            git log -p
   
   2.  revert:

           git checkout <commit_hash> -- <path_to_file1> <path_to_file2> <path_to_file3..etc>
