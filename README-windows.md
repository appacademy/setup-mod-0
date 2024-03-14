# Environment Setup for Windows

You'll need to install some basic development tools to complete Module 0. There
are a few different ways to accomplish this, but please use the method below.
It's good practice for how you'll normally install other tools as a developer!

## Operating System

Much of the software you will be using is updated regularly and will eventually
stop working on older versions of operating systems.  You can save yourself many
tears by making sure that you keep your OS up-to-date:

1. Search for "system information" in the Windows Search Bar and open the System
   Information panel.  If you do not have a search bar or your OS Name is not
   some variation of "Windows 10" or "Windows 11", you must update your Windows
   version to Windows 10 or 11 before you continue with these instructions.
2. Search for "update" in the Windows Search Bar.
3. Click "Check for Updates".
4. In the window that opens, click the "Check for Updates" button.
5. Follow the prompts on the screen to install all available updates.

## Required Software for Module 0

To complete the Module 0, you will need to install __Google Chrome__,
__Visual Studio Code__, and __Node.js__.

Please follow the instructions and commands below exactly.  While you are
normally strongly encouraged to experiment with changing parts of the code
examples you learn, this can cause problems during environment setup, and later
on in the course itself.

### Google Chrome

Here at App Academy, our browser of choice is Google Chrome, due to its valuable
suite of developer tools. If you do not already have the Google Chrome browser
installed, you will first need to install it, and then set it as your default
browser.

__If you have Google Chrome installed already, make sure it is updated to the
latest version of Chrome.__

1. Navigate to the [Google Chrome] website and look for the blue "Download
   Chrome" button.
2. Check to make sure the text underneath the button matches your operating
   system (Windows 10 or Windows 11).
   - If it matches, click on the "Download Chrome" button.
   - If it does not match, click on "Other Platforms" at the bottom of the page,
     and click on the link for your version of Windows.
3. Follow the instructions on the Chrome installer to complete the download and
   installation.
4. When prompted at the end of the installation, set Chrome as your default
   browser.

Check that Google Chrome is installed and working properly by finding it in
Windows Explorer, and double-click to open it.

### Visual Studio Code

Visual Studio Code (or VS Code) is a multi-language code editor that can handle
almost any programming language for any platform.

1. Navigate to the [Visual Studio Code] website and look for the blue "Download"
   button towards the middle of the page.
2. Check to make sure the text inside the button matches your operating system
   (Windows).
   - If it matches, click on the "Download" button.
   - If it does not match, click on "other platforms" underneath the button, and
     click on the blue "Windows" button.
3. Follow the instructions on the installer to complete the download and
   installation.
4. Check that Visual Studio Code is installed and working properly by finding it
   in Windows Explorer. Double-click to open it.
5. In VS Code, open the Command Palette (`Ctrl+Shift+P`) and type "shell
   command".
6. Click on `Shell Command: Install 'code' command in PATH command`. This will
   enable you to open projects in VS Code from the Terminal by using the `code`
   command.

   > **Note:** If `Shell Command` does not appear as an option, the installer
   > may have already installed the `code` command. Open a terminal session and
   > run `code -v`. If the command executes without a `command not found` error,
   > you're done installing VS Code!
   >
   > If `code -v` does not work, you can manually add the VS Code __bin__ folder
   > to the path. Search Windows for 'environment variables'. In the results,
   > open `Edit the System Environmental Variables` and click on the
   > `Environmental Variables...` box at the bottom. In the next window, select
   > `Path` under `User variables for <username>`. Note the `<username>` and
   > click `Edit...`. In the resulting window, click to add a `New` line to the
   > variable:
   >
   > `C:\Users\<username>\AppData\Local\Programs\Microsoft VS Code\bin`
   >
   > where `<username>` is the username that you previously noted. Click `OK`.
   > Open a new terminal session and run `code -v`; the version info should now
   > show!

### Node.js

Node.js is a JavaScript runtime environment that you can use to run JavaScript
locally in your terminal.

1. Navigate to the [Node download page], and click on the "Windows Installer"
   button. Make sure you are in the "LTS Recommended for most users" tab.
2. Open the downloaded file and follow the installation menu and keep pressing
   "Next". In the installation menu for "Tools for Native Modules", leave the
   checkbox unchecked. Click "Install" after pressing "Next" all the way.
3. When installation is complete, open Windows PowerShell. PowerShell should
   show a prompt that looks like this: "PS C:\Users\username>" where your name
   will appear instead of "username". In the same line of the prompt, type
   `(Get-Command node).Path` and press Enter. After the prompt, it should show
   the following output:

   ```sh
   PS C:\Users\username> (Get-Command node).Path
   C:\Program Files\nodejs\node.exe
   ```

4. Run the following command in the PowerShell terminal to install some Node.js
   packages that you will be using to complete your assignments:

   ```sh
   npm install -g mocha chai@4.3.10 chai-spies cypress
   ```

   - You will know when the command is finished running because you should see a
     new prompt as a new line:

      ```sh
      PS C:\Users\username> npm install -g mocha chai@4.3.10 chai-spies cypress
   
      changed 264 packages in 8s
      
      49 packages are looking for funding
        run `npm fund` for details
      PS C:\Users\username>
      ```

   - This will globally install the following Node.js packages so that you can
     use them in any project in your machine (you do not need to know what these
     packages actually do right now):
     - [Mocha]
     - [Chai]
     - [Chai-Spies]
     - [Cypress]

> _Note: Every environment is different, so you may need to do some
> troubleshooting to get this setup to work. Reach out to the Prepwork Mentors
> on Discord if you run into any difficulties._

[Google Chrome]: https://www.google.com/chrome/
[Visual Studio Code]: https://code.visualstudio.com/
[Node download page]: https://nodejs.org/en/download/
[Mocha]: https://mochajs.org/
[Chai]: https://www.chaijs.com/
[Chai-Spies]: https://www.chaijs.com/plugins/chai-spies/
[Cypress]: https://www.cypress.io/
