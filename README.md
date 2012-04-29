This project adds [DASM] syntax higlight support to the vim editor.

(Upto date with dcpu v1.7)

[DASM]: http://dcpu.com/

### Install from a Zipball

This is the quickest way to get things running.

1. Download the latest zipball from [vim.org][zipball-vim] or
   [github][zipball-github]. The latest version on github is under Download
   Packages (don't use the Download buttons.)

2. Extract the archive into `~/.vim/`:

        unzip -od ~/.vim vim-dasm-HASH.zip

These steps are also used to update the plugin.

[zipball-vim]: http://www.vim.org/scripts/script.php?script_id=3590
[zipball-github]: https://github.com/pksunkara/vim-dasm/downloads

### Install with Pathogen

Since this plugin has rolling versions based on git commits, using pathogen and
git is the preferred way to install. The plugin ends up contained in its own
directory and updates are just a `git pull` away.

1. Install tpope's [pathogen] into `~/.vim/autoload/` and add this line to your
   `vimrc`:

        call pathogen#infect()

    To get the all the features of this plugin, make sure you also have a
    `filetype plugin indent on` line in there.

[pathogen]: http://www.vim.org/scripts/script.php?script_id=2332

2. Create and change into `~/.vim/bundle/`:

        $ mkdir ~/.vim/bundle
        $ cd ~/.vim/bundle

3. Make a clone of the `vim-dasm` repository:

        $ git clone https://github.com/pksunkara/vim-dasm.git

#### Updating

1. Change into `~/.vim/bundle/vim-dasm/`:

        $ cd ~/.vim/bundle/vim-dasm

2. Pull in the latest changes:

        $ git pull


### Tune Vim for DASM

Changing these core settings can make vim more DASM friendly.

#### Two-space indentation

To get standard two-space indentation in DASM files, add this line to
your `vimrc`:

    au BufNewFile,BufReadPost *.dasm,*.dasm16 setl shiftwidth=2 expandtab
