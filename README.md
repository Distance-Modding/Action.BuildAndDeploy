# Build VisualStudio solution and deploy artifacts
Composite GitHub action to build and deploy a MSBuild solution using settings from a .env file

# Using the action
In your git repository, create a `.env` file with the following content:
```ini
SOLUTION=<your msbuild .proj or .sln file>
ARTIFACTS=<list of files to upload in the release separated by semicolons>
RELEASE_BODY=<mardown representing the description of the automated releases>
```

Example:
```ini
SOLUTION=src/MyProject.sln
ARTIFACTS=build/app.zip;build/version.txt
RELEASE_BODY=This is an automated release made from a github workflow
```
