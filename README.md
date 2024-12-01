# Linux Foundation Introduction Course Node.js
---
## URL
[LF introduction to node](https://training.linuxfoundation.org/training/introduction-to-nodejs-lfw111/)
---
## Installation
Install fnm
`$ curl -fsSL ht‌tps://fnm.vercel.app/install | bash`
Check version is correct
`$ fnm --version`
The expected output should be fnm 1.33.1.
If, upon restarting the terminal, you encounter a "Command 'fnm' not found" 
`$ export PATH="$HOME/.local/share/fnm:$PATH"`
With the version manager successfully installed, let's proceed to install the specific Node version for this course
`$ fnm install --lts`
This command will install the lates long term support version of Node.
The version used for this course is v18.16.0
To verify that Node is installed and check its version, use the following command:
`node -v`


