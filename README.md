# VS Code remote Java development container
Develop Java in VS Code with a Debian based development container

## Devcontainer settings
Please find the devcontainer settings in [devcontainer.json](.devcontainer/devcontainer.json)

Mandatory: replace debian:stable-slim with a Debian based Java image of choice before opening the project in a container.
```json
"DOCKER_IMAGE": "debian:stable-slim"
```
Optional: add an url to an Eclipse based Java style guide.
```json
"java.format.settings.url": ""
```
Optional: replace the lines below with: `vscjava.vscode-java-pack` if you want all the extensions below including the IntelliCode extension.
```json
    "redhat.java",
    "vscjava.vscode-java-debug",
    "vscjava.vscode-java-test",
    "vscjava.vscode-maven",
    "vscjava.vscode-java-dependency"
```