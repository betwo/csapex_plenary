# How to contribute

If you are maintainer of a public plugin package, please feel free to add it as a submodule.
Please also add all dependencies and make sure it builds in separation.


# How to add a submodule

## CS::APEX plugin package

Use the following command to add a new package:

    git submodule add <git-remote> src/csapex_plugins/<desired-folder-name>
    cd src/csapex_plugins/<desired-folder-name>
    git checkout <branch or sha1>

For example:

    git submodule add https://github.com/cogsys-tuebingen/csapex_core_plugins.git src/csapex_plugins/core_plugins 
    cd src/csapex_plugins/core_plugins 
    git checkout devel

Then commit everything in the plenary repository, once it builds on itself.


## Dependencies

For dependencies, please add them to 

    src/deps/...

by using

    git submodule add <git-remote> src/deps/<desired-folder-name>
    cd src/deps/<desired-folder-name>
    git checkout <branch or sha1> 

For example:

    git submodule add https://github.com/cogsys-tuebingen/cslibs_vision.git src/deps/cslibs_vision 
    cd src/deps/cslibs_vision 
    git checkout 47a4b6dd1500c866a3d8fc1a46ca90f88eed6ede

Then commit everything in the plenary repository, once it builds on itself.



## Updating a submodule

Switch to the submodule and checkout the desired version, e.g.

    cd src/csapex_plugins/core_plugins
    git fetch
    git checkout origin/master
    
Then commit everything in the plenary repository, once the repository builds.
