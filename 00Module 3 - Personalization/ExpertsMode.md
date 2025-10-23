## 1.  Connecting to GitHub Codespaces in VS Code

You’ll connect Visual Studio Code (the desktop app) to GitHub Codespaces, sync your environment, and customize it using your own configuration.

1. Enable GitHub Codespaces Support in VS Code

*You’ll need the GitHub Codespaces extension to connect to your cloud environments.
*

2. Connect your local VS Code instance to your GitHub account.
3. Access Your Codespaces from VS Code
4. Confirm You’re Connected

Once connected, Check the following indicators to confirm you’re working inside your Codespace:

- The environment indicator in the bottom-left corner
- Your terminal path (is it local or remote?)

## 2. Set Up Settings Sync for GitHub Codespaces

Your goal now is to keep your editor preferences consistent across all Codespaces.

- Find where VS Code lets you sync settings and connect it to your GitHub account.
- Change the color scheme 
- Open another Codespace to see if your settings are applied automatically

## 3. Turn off Settings Sync
Find the GitHub Settings to disable Settings Sync for Codespaces.


## 4. Set up a Dotfiles repository for Codespaces 

Dotfiles allow you to carry your favorite configuration into every Codespace automatically.

- Create a repository named something like dotfiles.
- Add a .bashrc or .zshrc file that customizes your prompt or adds startup messages.
- Add a second file for custom aliases or shortcuts.
- Commit and push your changes.

## 5. Configure GitHub to use your dotfiles repository

Now, connect your dotfiles to GitHub Codespaces. Do this from the GitHub Codespaces Settings page.
Then create a new Codespace to test it.
