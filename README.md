# LaTeX Template

![Logo](.github/latex-logo.svg)

LaTeX Document Template for VS Code with the LaTeX Workshop Extension, featuring automated document compilation and release via GitHub Actions and git tags.

## Usage

Writing the document using VS Code

1. Ensure you have the LaTeX Workshop Extension installed in VS Code and a TeX distribution installed on your system.
2. Open a LaTeX file (e.g. `main.tex`) in VS Code.
3. Make your changes and save the file.
4. The local build process should automatically start, generating a `main.pdf` file in the `out` folder.

To create a new release:

1. Add a git tag at the desired commit using the format `v*` (e.g. `v1.2.3`).
2. Push the tag to your repository.
3. GitHub Actions will compile the document into a PDF and create a new release for the tagged version.
4. Once completed, you can download the PDF document from the release page.

## Document Hierachy

This template follows the hierarchy shown below:

```
├── figures
│   └── painting.png
├── sections
│   └── example-section.tex
├── main.tex
├── references.bib
```

You can customize this hierarchy to suit your preferences, but it's essential to keep the `main.tex` file in the root directory. 
If you choose to rename it, ensure to update the [release.yml](.github/workflows/release.yml) file accordingly to reflect the new main file. 
For further customization of the project structure, refer to the [xu-cheng/latex-action@v2](https://github.com/xu-cheng/latex-action) repository, which is used for compiling the document.


## GitHub Actions

For the automatic document compilation and release GitHub Actions are used.
The workflow is defined in the release.yml file and can be configured there.

The repository automates the document compilation and release using GitHub Actions. 
The workflow is defined in the [release.yml](.github/workflows/release.yml) file and can be customized to suit specific requirements.

The workflow depends on the following:

- [actions/checkout@v2](https://github.com/actions/checkout): Action to checkout the repository
- [xu-cheng/latex-action@v2](https://github.com/xu-cheng/latex-action): Action for compiling LaTeX documents
- [softprops/action-gh-release@v1](https://github.com/softprops/action-gh-release): Action for creating GitHub releases

