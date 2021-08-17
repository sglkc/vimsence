<p align="center">
  <h1 align="center">VimSence</h1>
</p>

<p align="center">
  <img src="https://i.imgur.com/aL4g3nx.png" width="300">
  <img src="https://i.imgur.com/nrhZj4O.png" width="300">
</p>

## Getting Started
These instructions will get you a copy of the project up and running on your local machine.
More help about the plugin itself can be found [here](doc/vimsence.txt).

### Prerequisites
You need to have Vim/NeoVim with Python3 support

### Installing
#### [Vim-Plug](https://github.com/junegunn/vim-plug)
1. Add `Plug 'sglkc/vimsence'` to your vimrc file.
2. Reload your vimrc or restart
3. Run `:PlugInstall`

#### [Vundle](https://github.com/VundleVim/Vundle.vim) or similar
1. Add `Plugin 'sglkc/vimsence'` to your vimrc file.
2. Reload your vimrc or restart
3. Run `:BundleInstall`

#### [NeoBundle](https://github.com/Shougo/neobundle.vim)
1. Add `NeoBundle 'sglkc/vimsence'` to your vimrc file.
2. Reload your vimrc or restart
3. Run `:NeoUpdate`

#### [Pathogen](https://github.com/tpope/vim-pathogen)
```sh
cd ~/.vim/bundle
git clone https://github.com/sglkc/vimsence.git
```

#### Vim8 packages
```sh
git submodule add https://github.com/sglkc/vimsence.git vimsence
```

## Configuration
You can configure the messages of VimSence in your `.vimrc` with these options:
```vim
let g:vimsence_client_id = '439476230543245312'
let g:vimsence_small_text = 'NeoVim'
let g:vimsence_small_image = 'neovim'
let g:vimsence_editing_text = '{filetype} file'
let g:vimsence_editing_details = 'Editing {filename}'
let g:vimsence_editing_state = 'Working on {directory}'
let g:vimsence_file_explorer_text = 'In NERDTree'
let g:vimsence_file_explorer_details = 'Looking for files'
let g:vimsence_idle_text = 'Idling'
let g:vimsence_terminal_details = 'Bash shell'
let g:vimsence_terminal_state = 'Running {termcmds}'
let g:vimsence_add_timestamp = '600'
let g:vimsence_custom_icons = {'filetype': 'iconname'}
```
### Tags
You can put this inside `editing_text`, `editing_state` and `editing_details`
`{termcmds}` should only put in `terminal_state` and `terminal_details`
- `{filename}` current file name with extension
- `{filetype}` current file extension
- `{filesize}` current file human-readable size (KB, MB, ..)
- `{filesizeb}` current file size in bytes
- `{fileline}` current file lines
- `{filedir}` current file directory
- `{directory}` workspace directory
- `{termcmds}` terminal launch commands

## Development
First create a virtual environment.
If you don’t already have a preferred way to do this,
take some time to look at tools like pew, virtualfish, and virtualenvwrapper.

Install the development dependencies:
```sh
pip install -r requirements-dev.txt
```

To avoid committing code that violates our style guide, we strongly advise you to install [pre-commit](https://pre-commit.com/) hooks:
```sh
pre-commit install
```

You can also run them anytime using:
```sh
pre-commit run --all-files
```

## Authors
| Contributor                                                                                                                         | What has been done    |
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| <img src="https://avatars.githubusercontent.com/anned20" height=30px align=center>   [Anne Douwe Bouma](https://github.com/anned20) | Original work         |
| <img src="https://avatars.githubusercontent.com/hugolgst" height=30px align=center>   [Hugo Lageneste](https://github.com/hugolgst) | Maintaining this fork |

See also the list of [contributors](https://github.com/hugolgst/vimsence/contributors) who participated in this project.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
