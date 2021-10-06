# structurizr-dev-container

devcontainer setup for vscode to use structurizr lite locally

usefull links

- https://code.visualstudio.com/docs/remote/containers
- https://structurizr.com/
- https://structurizr.com/help/lite

To get started with structurizr lite you can create a file called workspace.dsl in the root of the project with the following example content:

```
workspace {

    model {
        user = person "User"
        softwareSystem = softwareSystem "Software System"

        user -> softwareSystem "Uses"
    }

    views {
        systemContext softwareSystem "Diagram1" {
            include *
            autoLayout
        }

        theme default
    }

}
```

after you have saved the workspace file open a browser at http://localhost:8080/ and accept the EULA.
