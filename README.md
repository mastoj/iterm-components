# iterm-components

Custom status bar components for use with iTerm2

![Built-in components and custom components](screenshots/example-setup.png)

## Components

### GitHub stars

Shows the current number of stars for the specified repository.
Clicking on the text takes you to the repo in your default browser.
You can add a personal access token in order to minimize rate limiting or to keep tabs on a private repository.

![GitHub stars component](screenshots/github-stars.png)

### `kubectl` context

Shows the active `kubectl` context.

![kubectl context component](screenshots/kubectl-context.png)

### environment variable (work in progress)

Shows the current value of an environment variable, with the option to show or hide the variable name.

### `pyenv`

Shows the active Python version or virtual environment.

![pyenv component](screenshots/pyenv.png)

### `rvm` gemset

Shows the active gemset.

![rvm gemset component](screenshots/rvm-gemset.png)


## Installation

At the moment, I don't know a better way to do this.
If you know one, I would happily review a pull request!

### Auto-loading the components

iTerm2 expects the custom status bar components that act as long-running processes to be in its `AutoLaunch` folder:

```shell
$ git clone git@github.com:daneah/iterm-components.git
$ cd ${HOME}/Library/Application\ Support/iTerm2/Scripts
$ mkdir -p AutoLaunch && cd AutoLaunch
$ ln -s /path/to/iterm-components/some_component.py .  # For each component you want to install; cp them if preferred
```

With iTerm2 running and selected go to **Scripts > AutoLaunch** and select the scripts you linked or copied into the AutoLaunch folder. You may be prompted to download the Python runtime.

### Configuring the components

After the components you want are present in the `AutoLaunch` folder and selected in the **Scripts > AutoLaunch** menu, iTerm2 should make them available to use.

Read [the instructions for using status bar components](https://www.iterm2.com/3.3/documentation-status-bar.html) and drag them where you like.
