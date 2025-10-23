## 1 – Create a devcontainer via Command Palette

- Use the VS Code Command Palette to generate a base dev container configuration for your favorite language (e.g., Node.js, Python, .NET). Choose the base configuration and add a feature like GitHub CLI.

> Hint: There’s a built-in command that helps you add “Dev Container Configuration Files.”

- When prompted, rebuild or reopen in the container.
- Notice where the new configuration file is created and what it contains.


## 2 – Add a feature to `devcontainer.json`

- Visit https://containers.dev/features and explore available add-ons.
- Pick one (e.g., AWS CLI, Azure CLI, or any that interest you) and integrate it into your devcontainer.json.

> Hint: Compare the structure of your JSON to the example on the site.

- After adding the feature, rebuild and confirm it’s installed using a version check command.


### 3.  Add default editor settings

- Inside your devcontainer.json, Add a settings section. Add an editor setting that changes something visible (like disabling the minimap).
- Rebuild and observe the effect.
- Then replace it with a setting that’s actually useful for your workflow (e.g., a terminal preference or format-on-save rule).

### 4. Install extensions

- In the same file, Create a "customizations.vscode.extensions" section and add extensions relevant to your stack.


### 5 Forward a port

- Use your devcontainer.json to forward at least one port (e.g., 3000 or 8080) for a local web app.
- Label the ports clearly using "portsAttributes" so they’re recognizable in the Codespaces interface.


### 6 Create a postcreate command

- Add a "postCreateCommand" to perform an automatic task when the container finishes building — maybe display a message, install dependencies, or run a setup script.

### 7 Switch to a custom Dockerfile

- Now create your own .devcontainer/Dockerfile.
- Start from a base image and install the tools your project requires (Node.js, Python, etc.).

### 8 Point `devcontainer.json` at your Dockerfile

- Modify your devcontainer.json to use the Dockerfile for builds instead of an image reference.
