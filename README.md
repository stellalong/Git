# uniform-pricing

#### Pre-requisites:
 - Windows `cmd.exe`, Mac OS X `bash`, or Linux `bash`. 
 - [Python 3.X](https://www.python.org) (add to [PATH](https://en.wikipedia.org/wiki/PATH_(variable)))
   - Modules: [PyYAML](http://pyyaml.org/wiki/PyYAML)
 - [Stata MP](http://www.stata.com/statamp/) (add to [PATH](https://en.wikipedia.org/wiki/PATH_(variable)))
   - Ado files: [`yaml`](https://github.com/sergiocorreia/stata-misc/tree/75a8b251bec02ba590c862cc395c4b95077d8a95), `plotmatrix`, `binscatter`, `labmask`
 - [R](https://www.r-project.org/) (add to [PATH](https://en.wikipedia.org/wiki/PATH_(variable)))
   - Packages: [`yaml`](https://cran.r-project.org/web/packages/yaml/yaml.pdf), `data.table`, `reshape2`, `Matrix`, `foreign`, `Hmisc`, `ggplot2`, `geosphere`, `doBy`, `ggmap`, `sandwich`, `lmtest`
 - [Lyx](https://www.lyx.org/) (add to [PATH](https://en.wikipedia.org/wiki/PATH_(variable)))
 - [SCons](http://scons.org/) (Note that version 2.4.0 or later is best if using the [cache](http://scons.org/doc/2.0.1/HTML/scons-user/c4213.html)).
    - More information about SCons can be found [here](https://github.com/gslab-econ/ra-manual/wiki/SCons).
 - [git-lfs](https://git-lfs.github.com/)
 - [gslab_tools](https://github.com/gslab-econ/gslab_python) version 3.0.3 or later
 - [GSLab-modified Metropolis beamer theme](https://github.com/gslab-econ/mtheme)
 - Setup a `user-config.yaml` at the root of the directory (this file is not versioned):
    - MacOS or Linux minimal working example
    ```
    stata_flavor: statamp
    SLRN_Datasets: /Users/chuanyu/Dropbox/SLRN_Datasets
    ```
    - Windows 10 minimal working example (note the quotation marks)
    ```
    stata_flavor: "%STATAEXE%"
    SLRN_Datasets: C:\Users\chuanyu\Dropbox/SLRN_Datasets
    ```
 - Setup a `temp` folder at the root of the directory (this folder is not versioned)

#### To run:
 - The entire directory: In the root directory, type `scons` in the command line. This should run everything that is flagged as being modified or with dependencies that have been modified.
 - A single directory of targets: `scons build/data` will re-build the `build/data` folder if it is out of sync, without rebuilding other files.
 - A single target file: `scons build/paper/paper.pdf` will re-run only the code needed to update `build/paper/paper.pdf` without rebuilding other files.
 - Making a release: See [here](https://github.com/gslab-econ/gslab_python/tree/master/gslab_scons).
