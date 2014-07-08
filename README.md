# Shell History Analysis Tool

This little shim helps with fetching the vast trophe of shell history files
found on GitHub and making the data accessible in a python environment
where it is easily visualizable.

## Usage

### 1. Fetch the data

        ./fetchData

This fills `./data/githubHistoryFiles/` with history files found on
GitHub with the help of [ghrabber](https://github.com/cortesi/ghrabber).

There is already a small amount of real sample data in this directory when
you check out this repo so you do not have to bug the GitHub servers each
time you wantb to test your own analysis code.

Every history file follows this naming scheme: `user.repository`.

More information on ghrabber and the idea of shell history file
analysis can be found
[here](http://corte.si/posts/hacks/github-shhistory/index.html).

### 2. Plot and show the data

        ./analysis

This actually plots the data.

### 3. Plug in your own analysis function

Write your own analysis function. It takes the data and the axis as
arguments:

        my_analysis(data, ax)

Modify the data however you wish.

Then plot it as easy as:

        ax.plot(data, '.')

See `analysis` for an example.
