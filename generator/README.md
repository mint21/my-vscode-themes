# Generator

We use the generator from [microsoft/vscode-generator-code](https://github.com/microsoft/vscode-generator-code).
Run this from the project's root directory to create the generator image and run a generator container.

```bash
podman build -t vscode-generator-code ./generator
podman run -it -v $(pwd):/usr/src/app vscode-generator-code
```

