## 1.  Connecting to GitHub Codespaces in VS Code

1. Open VS Code
2. Click on the Extensions icon in the Activity Bar (or press `Ctrl+Shift+X`)
3. Search for "GitHub Codespaces"
4. Click "Install" on the GitHub Codespaces extension
5. In VS Code, click on the account icon in the bottom-left corner of the window
6. Select "Sign in to GitHub" from the menu
7. Follow the authentication prompts to sign into your GitHub account
8. Once authenticated, you'll see your GitHub username in the status bar
9. Click on the Remote Explorer icon in the Activity Bar (looks like a monitor)
10. From the dropdown at the top, select "GitHub Codespaces"
11. You'll see a list of available Codespaces. If you don't have any open, you can create one from here.
12. Click on the Codespace you want to connect to

13. Once connected:

- VS Code will reload and connect to your Codespace
- The bottom-left corner will show "Codespace: [name]"
- Your files and terminal will now operate within the Codespace environment

## 2. Set Up Settings Sync for GitHub Codespaces

1. Open a Codespace, in VSCode or in the Web
2. In your Codespace, click on the gear icon in the lower-left corner of VS Code
3. Select "Backup and Sync Settings..."
4. A dialog will appear allowing you to select what to synchronize. Keep all options selected and click "sign in"
5. Choose GitHub as your account. Authenticate if prompted.
6. Change the color scheme in your Codespace
7. Open another Codespace to see if your settings are applied automatically
(if it doesn't work, try waiting a bit and try again. There could be a delay)


## 3. Turn off Settings Sync
1. Go to [Github.com/settings](https://github.com/settings/codespaces)
2. Uncheck: ![alt text](/images/module3-image-1.png)

## 4. Set up a Dotfiles repository for Codespaces 

GitHub Codespaces allows you to automatically apply your personal settings and configurations to every codespace you create by setting up a dotfiles repository.

>**What Are Dotfiles?**  
>Dotfiles are configuration files that start with a dot (.) in Unix-like systems. They're used to customize your environment. Common examples include:
> - `.bashrc` - Bash shell configuration
> - `.gitconfig` - Git configuration
> - `.vimrc` - Vim editor configuration


1. Create a new repository for your dotfiles (or use an existing one if you have it).Call the repository "dotfiles". It can be public or private.
2. Add a file called '.bashrc'
3. Add the following lines to the `.bashrc` file:

```bash
# Show a custom prompt
export PS1="💻 [Codespace] \w $ "

# Source aliases if they exist
if [ -f ~/.aliases ]; then
  source ~/.aliases
fi

echo "🎉 Your custom dotfiles are loaded!"

   ```

4. add a file called ".aliases" and add the following content:

```bash
# Custom Aliases for demo

alias gs='git status'
alias greet='echo "👋 Hello from your customized Codespace!"'
```
5. Commit and push your changes to GitHub. 

## 5. Configure GitHub to use your dotfiles repository

1. Go to [GitHub Codespaces Settings](https://github.com/settings/codespaces)
2. Under "Dotfiles", select this repository from the dropdown
3. Go Back to the lab-repositoy
4. Open a new Codespace
5. Wait untill the dotfiles are loaded. You should see the custom prompt and the message from your `.bashrc` file.
6. Verify that your aliases are working by running `greet` in the terminal. 
