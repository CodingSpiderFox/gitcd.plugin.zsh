# gitcd.plugin.zsh
👷 [oh-my-zsh plugin] change directory after git clone if not exist

## Installation

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

    ```sh
    git clone https://github.com/viko16/gitcd.plugin.zsh ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/gitcd
    ```

2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

    ```sh
    plugins=(gitcd)
    ```

3. Start a new terminal session.

## Usage

```sh
$ gitcd <repo-url>
```

Example:

```sh
$ gitcd https://github.com/viko16/gitcd.plugin.zsh.git
# => will git clone and cd to "~/Code/github.com/viko16/gitcd.plugin.zsh"
```

If the repository is already cloned to local, it will automatically "[cd](https://en.wikipedia.org/wiki/Cd_(command))" there.

## Config

By default, `gitcd` will git clone under `~/Code/<host>/<path>`.
If you want to change basedir, just set Environmental Variable name `GITCD_HOME`.

Example:
```sh
$ GITCD_HOME=~/myworkspace/ && gitcd https://github.com/facebook/react
# => ~/myworkspace/github.com/facebook/react
```

## Test

```sh
zsh ./test.zsh
```

## Thanks
- https://github.com/goreliu/zshguide
- https://github.com/repo-utils/giturl
- https://github.com/robbyrussell/oh-my-zsh/wiki/Customization

## License

[MIT License](https://opensource.org/licenses/MIT) © [viko16](https://github.com/viko16)

