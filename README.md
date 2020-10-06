# Lab-04
## Exercise 1 - Handling Conflicts

#### Cloning a repo
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL https://github.com/noama-demo/Lab04-ex1.git and choose clone

#### Setting Beyhond Compare or other diff / merge tool
1. On the Button Bar, click the 'Cog' wheel
2. On the left pane, go to Git -> Config
3. Change mergetool to whichever tool you use
4. Press OK

#### Merging with conflict - Abort
- Checkout master branch
- Right Click the feature branch and merge it to master
- Conflicts occure - read the message and Click OK
- Click 'No' to avoid solving conflicts
- On the upper part - Click 'Abort'
- You are back to state before the merge

#### Conflict origin
- Compare the master and feature branch
    - Select master branch commit
    - Also select feature branch commit
    - Check Split View Diff for the conflicts

#### Merging with conflict - Resolve
- Checkout master branch
- Right Click the feature branch and merge it to master
- Conflicts occure - read the message and Click OK
- Click 'Yes' to resolve conflicts
- View the file list and open demo-script1.ps in BC
    - Make the file look like this:
        ```
        function Create-GreenMessage
        {
            param
            (
                [Parameter(Mandatory=$true)]
                $Message
            )

            Write-Host $Message -ForegroundColor Blue
        }

        Create-GreenMessage -Message "My Message"
        Create-GreenMessage -Message "Master Message"
        Create-BlueMessage -Message "Feature Message!"
        ```
- Press CTRL+S to save and exit BC
- Press 'Yes' to commit now
- The commit window will open:
    - Review your commit and changes
    - Complete the merge commit by pressing 'Commit'
- Review the master demo-script.ps1 file

#### Mail the results
- To: <TBD>
- Topic: conflicts
- Body: demo-script.ps1 content (not file, since its ps1 and will be blocked)
