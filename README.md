# Linux Foundation Introduction Course Node.js

## URL

## [LF introduction to node](https://training.linuxfoundation.org/training/introduction-to-nodejs-lfw111/)

## Installation

Install fnm  
`$ curl -fsSL ht‌tps://fnm.vercel.app/install | bash`

Check version is correct  
`$ fnm --version`

The expected output should be fnm 1.33.1.  
If, upon restarting the terminal, you encounter a "Command 'fnm' not found"  
`$ export PATH="$HOME/.local/share/fnm:$PATH"`

With the version manager successfully installed, let's proceed to install the latest Long Term Support (lts) Node version.  
`$ fnm install --lts`

For this course we will require v18.16.0.  
` $ fnm install 18.16.0 `

Then:
` $ fnm use 18.16.0 `

To verify that Node is installed and check its version, use the following command:  
`node -v`

---

### .nvmrc File

1. Open a text editor in the root of your project directory.
2. Create a new file and save it as .nvmrc (including the leading dot).
3. In the .nvmrc file, specify the Node version you want to use for your project. You can find the desired version by visiting the official Node.js website and looking for the Long-Term Stable (LTS) or the latest version. For example, you can simply write v18.16.0 in the .nvmrc file.
4. Save the .nvmrc file and close the text editor.

Once you have created the .nvmrc file with the desired Node version, you can use the following command to install and set that specific Node version for your project:

`$ fnm use --version-file-strategy local`

## Quick File Server

Navigate to the directory that contains the static folder within the terminal.
`santi@LAPTOP-RBEKK8IP MINGW64 ~/OneDrive/Escritorio/Coding/lf-intro-node/static (main)
$ cd '../'`

Then use the following command to start the file server:  
`$ npx serve -p 5050 static`

![terminal expected output](/images/server-running.png)

Now, you can open your browser and navigate to http://localhost:5050. You should see the web page with the Fetch Products button.

## Creating NPM Shell Commands

We can aliviate the burden of frequently using shell commands by creating custom NPM shell commands. This commands are defined within the package.json file, specifically under the "scripts" object like so:

`"scripts": {
    "static": "serve -p 5050 static",
    "test": "echo \"Error: no test specified\" && exit 1"
  },`

Once you've defined your commands you can execute the commands in the terminal.

`$ npm run static`

## Mocking a Web Service
