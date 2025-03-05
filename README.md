# project-name

## Setup
If you haven't setup cryptobib yet, do it now. Either once per project as a submodule using
```
git submodule add https://github.com/cryptobib/export_crossref paper
```
or once for all projects by ...
1. cloning into an external folder, e.g. by executing `git clone https://github.com/cryptobib/export_crossref cryptobib` in `~/Documents`, and
2. adding the `cryptobib` folder permanently to your PATH by editing `~/.bashrc` adding the following line.
`export BIBINPUTS=".:~/Documents/cryptobib"`.

Otherwise, rename the `project-name.tex` file and eventually the title of this README and you're done.


## LaTeX Stuff

### Features

- [cryptobib](https://cryptobib.di.ens.fr/) bibliography
- [cryptocode](http://mirrors.ibiblio.org/CTAN/macros/latex/contrib/cryptocode/cryptocode.pdf) macros
- `anonynmous{foo}{bar}` to hide/show information during submission/after
- `tikzexternalizemaybe` to enable `tikzexternalize` depending on value of `buildexternal`
- [.dir-locals.el](https://www.gnu.org/software/emacs/manual/html_node/emacs/Directory-Variables.html) according to my taste
- [.projectile](https://github.com/bbatsov/projectile) according to my taste
- Extensive `.gitignore`

### Assumptions

- The paper is in `paper`.
- Code goes into `code`.
- Data goes into `data`.
- Cryptobib is in a directory pointed to by `BIBINPUTS=.:/path-to/cryptobib`
- Scripts write to `paper/constants.tex` for use with [pgfkeys](https://ctan.org/pkg/pgfkeys?lang=en).

### Local Changes 

If you want to do local modification to `.dir-locals.el` which is under version control, you can use
```sh
git update-index --assume-unchanged .dir-locals.el
```
to tell git to ignore changes to that file. Use
```sh
git update-index --no-assume-unchanged .dir-locals.el
``` 
to undo.
