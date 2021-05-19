# My Document Index
This is a short, handy, bash script for quickly opening documents from the
command line.
## Features
* Open any local file with with a short terminal command.
* Decide what program to open with depending on the file-extension.
* Auto-completion

## Setup
1. Clone or download this repository.
2. Create a config file.
    * Use `my-document-index-config-example` and fill in with your own
      documents.
    * Rename the file (remove '-example').
    * If you want to, that file can be moved to another location. If so,
      remember to change the `config_path` variable in the `my-document-index`
      file.
3. Create an alias.
    * Add an alias in `.bashrc` or similar to easy reach the `my-document-index`
      script.
    * For example:
      ```bash
      alias index="~/git/my-document-index/my-document-index"
      ```
4. Setup the auto-completion
    * Make sure the `completion/index` file is run on shell startup. I recommend
      putting it in a separate directory, for example `~/.bash_completion` and
      then running all files in that folder by adding the following to `.bashrc`.
      ```bash
      # Bash completion
      for f in $HOME/.bash_completion/* ; do source $f ; done
      ```
5. Update shell environment
    ```
    source ~/.bashrc
    ```


## Usage
With the configurations done in the setup example, to open
`~/Documents/my_cool_document.odf` with the system default program, do:
```
index my-cool-document
```
