
## 1. Set up a Prebuild

1. Navigate to the GitHub repository in the web browser
2. Click on the "Settings" tab
3. In the left sidebar, click on "Codespaces"
4. Click "Set up prebuild"
5. Configure the following settings:
   a. **branch**:
      Select the main branch
   b. **Prebuild triggers**:
      Choose on configuration change
   c. **Region availability**:
      - West europe

6. Click "Create" to set up the prebuild configuration

>After creating the configuration, GitHub will start creating the first prebuild
>You can monitor the status of prebuild creation in the GitHub Actions of the repository
>The initial prebuild might take several minutes to complete

Once prebuilds are available:
7. Click on the "Code" button in your repository
8. Select the "Codespaces" tab
9. Click "Create codespace on [branch]"
10. You should notice a significantly faster startup time with a message indicating the codespace was created from a prebuild

## Find all GitHub Codespaces Settings
1. Navigate to GitHub and click on the hamburger menu (three horizontal lines) in the top-left corner
2. Click on "Codespaces"
3. Here, you can find 
    - The current list of your Codespaces
    - Create a new Codespace
    - Access various settings for each Codespace

4. Go to your profile picture in the top-right corner and click on it
5. Select "Settings" from the dropdown menu
6. In the left sidebar, click on "Codespaces"
7. Navigate all the settings available here

8. In the left sidebar, click on "Billing & licensing" 
9. Under "Metered Usage", select "Codespaces"
10. Click "Show details" to view your Codespaces usage and billing information