# Environment Setup for Linux

You'll need to install some basic development tools to complete these
activities.  We've provided brief instructions, but if you are using Linux, it's
up to you to find and use the correct method to set up the software for your
specific implementation and settings.

## The responsibility of choosing Linux

With great power (and a price tag of zero) comes great responsibility.  __If you
choose to use Linux as your development platform, you're taking on complete
responsibility to figure out and make the specific configurations necessary to
get everything working on your device.__

If you don't know what that means and don't already have an approach in mind, it
is best to use Windows or Mac for this experience.  Learning to be a developer
is extremely challenging and struggling with Linux environment issues will add
to that.

You'll notice that our instructions for Linux are much briefer than for other
operating systems.  This is because many steps need to be adjusted to work on
different implementations of Linux.  There may be different commands, different
files, or additional steps.

## Required Software for Module 0

To complete the Module 0, you will need to install __Google Chrome__,
__Visual Studio Code__, and __Node.js__.

Please follow the instructions and commands below exactly.  While you are
normally strongly encouraged to experiment with changing parts of the code
examples you learn, this can cause problems during environment setup, and later
on in the course itself.

Visit the sites below for guidance on installing this software for your Linux
environment.

- [Visual Studio Code]
- [Google Chrome] - If you have Google Chrome installed already, make sure it is
  updated to the latest version of Chrome
- [Installing the latest Node.js version using NVM]

> _Note: You may need to do some trouble-shooting to get your setup to work.
> Keep in mind that Linux is not officially supported at App Academy. If you
> struggle with your Linux setup, you are strongly encouraged to switch to a Mac
> or Windows environment so you can benefit from Prepwork Mentor and Instructor
> support with your environment setup._

After you have installed VS Code, launch the program. Open the Command Palette
(`Ctrl+Shift+P`) and type "shell command". Click on `Shell Command: Install
'code' command in PATH command`. This will enable you to open projects in VS
Code from the Terminal by using the `code` command.

After installing Node.js, run the following command in the terminal to install
some Node.js packages that you will be using to complete your assignments:

```shell
npm install -g mocha chai@4.3.10 chai-spies cypress
```

This will globally install the following Node.js packages so that you can use
them in any project in your machine (you do not need to know what these packages
actually do right now):

- [Mocha]
- [Chai]
- [Chai-Spies]
- [Cypress]

[Visual Studio Code]: https://code.visualstudio.com/
[Google Chrome]: https://www.google.com/chrome/
[Installing the latest Node.js version using NVM]: https://github.com/nvm-sh/nvm
[Mocha]: https://mochajs.org/
[Chai]: https://www.chaijs.com/
[Chai-Spies]: https://www.chaijs.com/plugins/chai-spies/
[Cypress]: https://www.cypress.io/
