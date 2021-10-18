# Communicate Data Findings
## Project no. 3 in FWD Advanced Data Analysis course under Udacity
## Problem using output-toggle.tpl template

### Problem Description
1. The project requires creating slide decks presentation of a notebook using a specific template called output-toggle.tpl. This template helps in hiding the code cell of a graph in the slide decks presentation.
2. The problem is that this template is compatible only with nbconvert (dependency package of jupyter) versions up to 5.6.1. Beyond this version and starting from version 6.0, there is a major change in the way nbconvert templates are structured or written. As such, we couldn't generate the slide decks using the provided template.
3. A workaround for this is to create a new virtual environment, install jupyter in this new virtual environment, and then downgrade nbconvert to version 5.6.1.
4. With that done, you can use the provided template and successfully run the slide decks.


### Execution Steps
1. Open Anaconda Prompt
2. Create new virtual environment `conda create --name slides` (Here I am naming the new environment as slides)
3. Activate the created virtual environment `conda activate slides'
4. The prompt in Anaconda should now show the activated environment `(slides) <some_path> >`
5. Install jupyter again in this environment `pip install jupyter` . This installs latest jupyter with its dependencies (specifically of interest here is that 
6. After installation if your try `jupyter --version`, you will have list of jupyter dependencies and their versions. What of interest here is that you will find `nbconvert  :xxx` where `xxx > 5.6.1`. This is the whole problem. The file `output-toggle.tpl` is supported only up to `nbconvert 5.6.1`. Starting `nbconvert 6.0` the templates are written differently, and as such you cannot use this template as is.
7. Downgrade `nbconvert` to the supported version using `pip install nbconvert==5.6.1`
8. Now browse to the project folder in Anaconda prompt where your both `presentation.ipynb` and `output-toggle.tpl` files are located. (I assumed the slides file is called presentation.ipynb).
9. Now use the command as given in the course: `jupyter nbconvert presentation.ipynb --to slides --template output-toggle.tpl --post serve`
