# Instructions to starting the LectureFeed Web Application

This is an instruction on how to start the LectureFeed Web Application. There are different possibilities for starting the LectureFeed Web Application. For development purposes it is recommended to build and start the application manually to be able to test current changes. For illustration the LectureFeed Web Application can also be started running prebuild artifacts.

## Starting the Web Application Manually

1 - clone the git repositories [LectureFeed-Web](https://github.com/MaximilianLincks/LectureFeed-Web) and [LectureFeed](https://github.com/MaximilianLincks/LectureFeed).

2 - Open the cloned projects in your IDE and open the terminal. Navigate to the root of the LectureFeed project.

3 - The LectureFeed repository does contain the LectureFeed-Web repository as submodule. In order to make sure this as well is pulled when executing a git pull, make sure to run the command <code>git submodule update --init --recursive</code> in the terminal.

4 - To make sure you are operating on the newest version of the project, make sure you are on the branch main and execute the command <code>git pull</code>.
    Tip: You can check what branch you are currently on by running <code>git status</code> and you can change the branch by executing <code>git checkout *branchname*</code>.

5 - Navigate to the root of the LectureFeed-Web project. You can either use the location of the cloned LectureFeed-Web project or the location of the submodule contained in the LectureFeed project.

6 - Execute <code>npm install</code>
    In case you are using the LectureFeed submodule, you will have to delete the folder node-modules after this step

7- Execute <code>npm run start</code>.