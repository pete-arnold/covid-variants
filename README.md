# covid-variants
Exercise in the use of git version control in the exploration and mapping of Covid-19 variant data.

## PMIM102/PM272 Github session

_Dr Pete Arnold, 6 December 2021-27 January 2022_

### Instructions
1. __Create a repository from the repository on github.__
	If git is not installed, install it – see installation HTML page.
	If there is not github account register for one – see installation HTML page.
If there is a problem setting the –global parameters, you may need admin rights and a git 
bash prompt that is not in RStudio.
Locate my (pete-arnold) covid-variants repository on github (https://github.com/pete-arnold/covid-variants).
Get the https URL from the green code button into your PC clipboard.
Open RStudio and create a new project using the Version Control option, select Git, paste the URL into the box and call the project e.g. covid-variants. Choose a suitable project directory using Browse.

1. __Look at the code and the framework that has been created.__
The code you now have in your repository is the skeleton code you will need for this 
exercise. The main code is in the file covariants.R. The functions you need to implement are provided as outlines with instructions in the other R scripts.
We’ll start by looking at the code up to ‘Task 1’ as this sets the scene.
Install the mapping code. Look at the data. Plot the population data.
One of us will make the change to their local repository and then push to the github 
repository. The rest of us can then pull the changes.

1. __Next we’ll get some Covid data.__ Find the websites, download and view the data.
Create a data directory in your covid-variants project. Go to WHO website, locate and download the Covid data and save it in a data directory.
Have a look at the WHO dashboard (this kind of output is quite straightforward – we could create similar maps as we are today for online presentation using, for example, Tableau). Once you have downloaded the data, have a good look at it.

1. __For the next three exercises, work through the version control process__ of modifying the code, staging and committing to git (your local repository) and pushing and pulling to the online, shared github repository. Add the functions in one-by-one as they become available. 

	* __Complete covid.R.__ Add the plot code for Case_rate. Test and once working, commit and push to the repository. Let us know that you have pushed and the rest of us can pull your code (or attempt to push our own version – please don’t overwrite anyone else’s code, but feel free to make slight adjustments or corrections).

	* __Complete variants.R #1 for a single variants.__ Locate the covid variant data on the GISAID website and download – create files with the suggested names to make it easier. Implement and test code to extract the variant counts and add to the main data frame. Once working, add the code to the repository, push and let us know we can pull

	* __Complete variants.R #2 for multiple variants.__ Likewise with the code to extract a list of multiple variants.

1. __Work through the process of branching.__ For the final two exercises, before you make any changes to the code, create a git branch (with your name and feature e.g. pete-plot). Then proceed as above. Once we have a number of options in place, we can attempt to merge the code back to the main branch.

	* __Implement the plot function (create_map()).__ Create a branch with user’s name and feature. Complete plot.R and commit. Switch back 
to the main branch and make a random change. Commit. Look at the history. Push the branch to the origin repository. Decide that the branch is better – checkout the main branch as the merge destination and merge (use git merge pete-plot). Fix conflicts and push. Make sure you refresh the history.

	* __Undertake the same process to implement the layout_maps() code.__

1. Create the final map. Everyone should now be able to pull the github repository and complete the covariants file to produce a plot page with several maps showing the distribution of various covid variants. Commit and push this.

![Typical maps output at the end of the exercise](https://github.com/pete-arnold/covid-variants/blob/main/images/maps.png?raw=true)

### Functions to be created in the exercises
1. Create a map showing the data from a specified variable (may require advanced code).
1. Get the world Covid data and add to the map data frame.
1. Get and add variant data to the world Covid data frame. Two of these – one to get a single variant dataset and the other to get a list of variants specified in a named vector.
1. Produce a layout with several maps with specified data.
