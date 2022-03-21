# copier-template-example

## System requirements
 - Python >= 3.6
 - Git >= 2.24

## Usage

### New project
1. Install `copier` with the help of `pipx`:
    - If you don't have it, install `pipx` according to https://github.com/pypa/pipx
    - Install `copier`:
      ```
      pipx install copier
      ```
    - Now you should be able to check its version:
      ```bash
      copier --version
      # copier 5.1.0
      ```
2. Generate the project files from the template (change the path below accordingly):
    ```bash
    copier git@github.com:bugra-yilmaz/copier-template-example.git <path/to/project_folder>
    ```
    This will start a questionnaire which you'll need to fill in the details for your project. Some questions have a default value already filled (for which you can just press Enter to accept).
    After the questionnaire is done, the files are generated.
3. Review the generated files and commit the changes.

### Update existing project
1. Make sure you have `copier` installed.
2. Enter into the *root folder of the project* to be updated and run:
   ```bash
   copier update
   ```
   This will go through the questionnaire again. You can simply press Enter to accept the already answered questions – be careful with the possibility of new questions though!
3. After the questionnaire, `copier` will ask to overwrite the templated files that contain changes. You should most likely accept all the overwrites, unless you're sure about why something could be skipped.
4. Review the files and commit the changes.

### Update to specific version
If you don't want to update to the latest available version, maybe the project is too out-of-date and you want to go step by step, specify an explicit version using the `-r` option to copier:
```bash
copier -r 0.0.5 update
```
