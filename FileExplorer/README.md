
###File Explorer App

![View What You Will be Building](https://drive.google.com/file/d/1o6fBiUzHlDeKni4ng4FrkIv4k4Ragus8/view?usp=sharing)



###Introduction
Today, you will be building a file explorer, similar to ones you're used to seeing in the left panel of your favorite code editor. File explorers typically show the directory structure of your project as a "tree" of folders and files nested within other folders.

Here is what the final product will look like:

Your file explorer will use a mocked backend API (provided to you) to read/write the file system.

##Getting started
To help you get started, we’re providing some boilerplate scaffolding code to start with. Here’s how to get this up and running:
Download and extract one of the boilerplate packages included with these instructions:
file-explorer-boilerplate.zip (JavaScript)
file-explorer-ts-boilerplate.zip (TypeScript)
Follow the instructions in the README to install Node and Yarn and launch the app.

##Requirements
DO fetch the directory tree from the mock backend (see src/api.js). See API details below.
DO display all files in the project, with files nested inside of folders as needed.

*DO allow folders to be collapsed and expanded.
*DO display the appropriate icon next to each file. There is a "default file" icon () you can use as a fallback for unknown file types.
*DO display a "delete" () button when hovering over a file or folder. Clicking on the delete button should delete the file or folder. You must persist changes to the mock backend using the removeById(id)  API wrapper. See API details below.
*DO match the provided mocks as closely as possible, time permitting. See detailed mocks below. 
*DO prioritize functionality over visual fidelity.

- You MAY add unit or integration tests as needed, but we do not expect you to provide test coverage.
- You MAY use lodash or similar pure-JS utility libraries
- You MAY use CSS, SASS, or styled-components for styling
- You MAY use TypeScript

DO NOT rely on third-party hook libraries. We want to see how you write React code and manage state!

This project could take 5-6 hours depending on how detailed you get!

###Submitting
If you used any additional NPM dependencies, add and save them to the package.json file

Delete the node_modules folder and zip up the project directory (or use the tar -czvf myInitials-FileExplorerApp.tar.gz --exclude="node_modules" . command to archive the current directory)

Submit your code as a zip file (no GitHub links, please!) using the submission link provided by your recruiter. Include your initials in the filename (e.g. myInitials-FileExplorerApp.zip or myInitials-FileExplorerApp.tar.gz)

##UI Mocks and Assets
###Full UI

File hover states (default = top, hover = bottom):

Folder hover states (default = top, hover = bottom):

Folder collapse states:

###Icons
You can find icon assets in the src/assets/icons directory. The following icons are available:

###Mock backend API
You can import the mock API wrappers from src/api.js. There are only two methods:

`getDirectoryTree(): Promise<DirectoryTree>`

Use this method to get a tree-like data structure that represents the project directory structure.

This is the data format:

`let directoryTree = {
   id: "[project id]",
   type: "project",
   name: "[project name]",
   children: [
     {
       id: "[folder id]",
       type: "folder",
       name: "[folder name]",
       children: [
         { id: "[folder id]", type: "folder", name: "[folder name]", children: []},
         { id: "[file id]", type: "file", name: "[file name]"},
         ...
       ],
     },
     { id: "[file id]", type: "file", name: "[file name]" },
     ...
   ],
 };`

###Rules:

There are three types of nodes in a directory tree: project, folder, and file.
Directory tree always starts with a project node. Only the top node can be a project node.

project and folder nodes have a children: [...] array:

children array can only contain folder or file nodes.

children array can be empty (e.g. empty project or empty folder).

file nodes do not have children.

Every node has a unique id: UUID.

There is no limit to how deeply the tree can be nested.

Inspect the src/api.js file to see the kind of data you will be rendering.

`removeById(id: UUID): Promise<DirectoryTree>`

Use this method to remove a single file or folder by its node id: UUID. After removal, the method returns an updated directory tree.
