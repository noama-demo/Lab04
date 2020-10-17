# Lab-04
## Exercise 1 - Handling Conflicts
### Overview
In this exercise, we will handle merge conflicts  

#### <u>Cloning a repo </u>
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL C:\GitServer\labs\Lab03-ex1 and choose clone
- Right click inside/on the folder and select 'GitExt open repository'

#### <u>Setting Beyhond Compare or other diff / merge tool </u>
1. On the Button Bar, click the <i>Settings</i> cog/wheel
2. On the left pane, go to Git -> Config
3. Change mergetool to whichever tool you use
4. Press OK

#### <u>Merging with conflict - Abort </u>
- On the left pane, right click <i>Remotes -> Origin -> feature</i> branch and select <i>Fetch & Checkout</i>. Select <i>checkout</i> if required.
- On the left pane, right click <i>Remotes -> Origin -> master</i> branch and select <i>Fetch & Checkout</i>. Select <i>checkout</i> if required.
- On the left panel, right click <i>feature</i> and choose <i>merge</i>
- Select <i>always create new merge commit</i> and <i>merge</i>
- Conflicts occure - read the message and Click OK
- Click 'No' to avoid solving conflicts
- On the upper part - Click 'Abort'
- You are back to state before the merge

#### <u>Conflict origin </u>
- Compare the <i>master</i> and <i>feature</i> branch
    - Select <i>master</i> branch commit
    - Also select <i>feature</i> branch commit
    - Check <i>Split View -> Diff</i> for the conflicts
        - Check the <i>demo-script.ps1</i> file
        - Ignore <i>Readme.md</i> file. It is irrelevant for this exercise
        - Ignore <i>Unique diff BASE</i>. It is irrelevant for this exercise

#### <u>Merging with conflict - Resolve </u>
- On the left pane, right click <i>Remotes -> Origin -> feature</i> branch and select <i>Fetch & Checkout</i>. Select <i>checkout</i> if required.
- On the left pane, right click <i>Remotes -> Origin -> master</i> branch and select <i>Fetch & Checkout</i>. Select <i>checkout</i> if required.
- On the left panel, right click <i>feature</i> and choose <i>merge</i>
- Select <i>always create new merge commit</i> and <i>merge</i>
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

#### <u>Mail the results </u>
- To: <TBD>
- Topic: conflicts
- Body: demo-script.ps1 content (not file, since its ps1 and will be blocked)
