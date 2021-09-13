[dotbot_repo]: https://github.com/anishathalye/dotbot

## Dotbot ```pamac``` Plugin

Plugin for [Dotbot][dotbot_repo], that adds ```pamac``` directive, which allows you to install pamac packages 

## Installation

1. Simply add this repo as a submodule of your dotfiles repository:
```
git submodule add https://github.com/skwinnik/dotbot-pamac.git
```

2. Pass this folder (or directly pamac.py file) path with corresponding flag to your [Dotbot][dotbot_repo] script:
  - ```-p /path/to/file/pamac.py```

  or

 - ```--plugin-dir /pato/to/plugin/folder```

## Supported task variants
```yaml
...
- pamac: 
    - app 1
    - app 2
    - app 3
    ...
```

## Usage

### Example config
```yaml
...
- pamac:
    - firefox
    - rofi
    ...
...
```

### Execution
```bash
"~/.dotfiles/bin/dotbot" -d "~/.dotfiles" -c "~/.dotfiles/packages.yaml" -p "~/.dotfiles/plugins/dotbot-pamac/pamac.py"
```
