# Environment Setup for MacOS

You'll need to install some basic development tools to complete Module 0. There
are a few different ways to accomplish this, but please use the method below.
It's good practice for how you'll normally install other tools as a developer!

## Operating System

Much of the software you will be using is updated regularly and will eventually
stop working on older versions of operating systems. You can save yourself many
tears by making sure that you keep your OS up-to-date:

1. Click the Apple Menu in the upper left
2. Select "About this Mac"
3. Click the "Software Update" Button
4. Follow the instructions in the "Software Upgrade" window and complete all
   available updates and/or upgrades.

## Required Software for Module 0

To complete the Module 0, you will need to install __Google Chrome__,
__Visual Studio Code__, __Homebrew__, and __Node.js__.

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
   system (Mac).
   - If it matches, click on the "Download Chrome" button.
   - If it does not match, click on "Other Platforms" at the bottom of the page,
     and click on the link for your version of Mac.
3. Follow the instructions on the Chrome installer to complete the download and
   installation.
4. When prompted at the end of the installation, set Chrome as your default
   browser.

Check that Google Chrome is installed and working properly by finding it in your
Applications directory, and double-clicking to open it.

### Visual Studio Code

Visual Studio Code (or VS Code) is a multi-language code editor that can handle
almost any programming language for any platform.

1. Navigate to the [Visual Studio Code] website and look for the blue "Download"
   button towards the middle of the page.
2. Check to make sure the text inside the button matches your operating system
   (Mac).
   - If it matches, click on the "Download" button.
   - If it does not match, click on "other platforms" underneath the button, and
     click on the blue "Mac" button.
3. Follow the instructions on the installer to complete the download and
   installation.
4. Check that Visual Studio Code is installed and working properly by finding it
   in your Applications directory. Double-click to open it.
5. In VS Code, open the Command Palette (`Cmd+Shift+P`) and type "shell
   command".
6. Click on `Shell Command: Install 'code' command in PATH command`. This will
   enable you to open projects in VS Code from the Terminal by using the `code`
   command.

### Homebrew

Homebrew is a piece of software for macOS that lets you install extra unix
software on your Mac.

1. Select "Terminal" to start Terminal.
2. Open your Chrome browser and navigate to https://brew.sh.
3. Copy the command to install Homebrew to be pasted into the Terminal by
   clicking on the clipboard icon.
4. Paste the command into Terminal and press Enter.
5. Press Enter when prompted.
6. Enter your password when prompted. _Wait...this could take a long time!_
7. You can check that Homebrew was installed by running `brew -v` in the
   Terminal. You should see an output of "Homebrew" followed by a version
   number. (Here's an example of a valid output: "Homebrew 4.1.11") If you don't
   see this output, you will have issues in the next installation.

### Node.js

Node.js is a JavaScript runtime environment that you can use to run JavaScript
locally in your terminal.

To install Node.js, first you will install a Node version management system
using Homebrew called NVM.

1. Select "Terminal" to start Terminal or open a new terminal.
2. Open your Chrome browser and navigate to
   https://formulae.brew.sh/formula/nvm.
3. Copy the command to install nvm to be pasted into the Terminal by clicking on
   the clipboard icon.
4. Paste the command into the terminal and press Enter.
5. Press Enter when prompted.
6. Enter your password if prompted.
7. Determine what your shell startup file is by running `echo $SHELL` in the
   terminal.
   - If the terminal output displays `bin/zsh`, your shell startup file is
     `~/.zshrc`.
   - If the terminal output displays `bin/bash`, your shell startup file is
     `~/.bashrc`.
   - If your terminal output doesn't display any of the outputs above, ask for
     help.
8. Determine whether or not you have an Apple Silicon Mac. To find out what type
   of Mac you have, go to the Apple menu and choose `About This Mac`. If you see
   `Chip: Apple`, then you have an Apple Silicon Mac; if you don't see that
   line, then you likely have an Intel Mac. (The Apple M1 Silicon chip was
   introduced in late 2020, so the date of your Mac can also serve as a guide.)
9. Run `code "$HOME/.${SHELL#*/bin/}rc"` to open your shell startup file in your
   VS Code editor to edit the file.
10. You need to add some code to the end of the file, but what you add will
    depend on whether or not you have an Apple Silicon Mac.

    If you have an Apple Silicon Mac, add these lines to the end of the file:

    ```shell
    export NVM_DIR="$HOME/.nvm"
    [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
    [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
    ```
 
    Otherwise, add these lines to the end of the file:

    ```sh
    export NVM_DIR="$HOME/.nvm"
    [ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
    [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
    ```

11. Save and close the file.
12. Open a brand new terminal.
13. Run `nvm install node` to install Node.js
14. Then type the next command in your terminal: `nvm -v` and press Enter.
    - It should print out the current LTS version of NVM a version manager for
      Node.js. (Here's an example of a valid output: "0.39.5")
15. When installation is complete, open your terminal and type: `which node`
    and press Enter.
    - It should print out the path of the installed Node.js application. Make
      sure it includes `.nvm` in the path. (Here's an example of a valid path:
      "/Users/username/.nvm/versions/node/v18.17.0/bin/node")
16. Run the following command in the terminal to install some Node.js packages
    that you will be using to complete your assignments.

    ```shell
    npm install -g mocha chai@4.3.10 chai-spies cypress
    ```

    - This will globally install the following Node.js packages so that you can
      use them in any local JavaScript project in your machine (you do not need
      to know what these packages actually do right now):
      - [Mocha]
      - [Chai]
      - [Chai-Spies]
      - [Cypress]

> _Note: Every environment is different, so you may need to do some
> trouble-shooting to get this setup to work. Reach out to the Prepwork Mentors
> on Discord if you run into any difficulties._

[Visual Studio Code]: https://code.visualstudio.com/
[Google Chrome]: https://www.google.com/chrome/
[Mocha]: https://mochajs.org/
[Chai]: https://www.chaijs.com/
[Chai-Spies]: https://www.chaijs.com/plugins/chai-spies/
[Cypress]: https://www.cypress.io/
