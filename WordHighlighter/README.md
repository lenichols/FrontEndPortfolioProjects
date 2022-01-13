
# Word/String Highlighter

![View Output](https://github.com/lenichols/FrontEndPortfolioProjects/raw/main/FileExplorer/user.interactions.gif)


### Introduction
In this project, you will create a module that highlights text/words in a string. 

## Getting started
You can use a simple html page or use a framework and create a component out of this feature. To flex your SPA skills, we suggest using REACT.

## Requirements
Render highlighted phrases given a string and an array of highlight objects. If highlights overlap, show the higher-priority highlights over the lower-priority highlights.

You will use a combination of Javascript and Styles munipulation to complete this project. Get creative!

```
const string = 'You will deliver new technology with an adorable puppy. Perfect!'
const highlights = [
    {
        startOffset: 4,
        endOffset: 20,
        color: '#d9f593',
        priority: 0
    },
    {
        startOffset: 17,
        endOffset: 31,
        color: '#e8e8e8',
        priority: 1
    }
]
```

Example Output:

![View Output](https://github.com/lenichols/FrontEndPortfolioProjects/raw/main/WordHighlighter/output-example.png)


Addition Requirements:

It is not necessary to handle any additional formatting or markup on the page other than the highlights. The goal of this project is to develope an independent module.

*Extra Credit hint:*

Add a text field that will allow you dynamically create the string instead of having it static.


### Submitting
If you used any additional NPM dependencies, add and save them to the package.json file

Delete the node_modules folder and zip up the project directory (or use the tar -czvf myInitials-WordHighlighter.tar.gz --exclude="node_modules" . command to archive the current directory)

Submit your code as a zip file (no GitHub links, please!) using the submission link provided by your recruiter. Include your initials in the filename (e.g. myInitials-WordHighlighter.zip or myInitials-WordHighlighter.tar.gz)

## UI Mocks and Assets

None for this project.

### Icons

None for this project.

### Mock backend API

None for this project.

### Rules:

Be creative. For now, use only 2 colors and be sure not to let the colors overlap.
