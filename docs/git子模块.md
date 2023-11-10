# Submodule
使用子模块背后最常见的驱动因素是模块化。

## Preparation

1. Move the subdirectory out of the superproject to be a peer to the superproject
directory. If maintaining repository history is important, consider using
git filter-branch to help extract subdirectory structure.
2. Rename the submodule-to-be directory to more accurately express the nature of
the submodule. For example, a refresh subdirectory might be renamed to client-
app-refresh-plug-in.
3. Create a new upstream hosting for the submodule as a first-class project (e.g., create
a new project on GitHub to host the extracted code).
4. Initialize the now stand-alone plug-in as a Git repo and push the commit to the
newly created project hosting URL.
5. In the superproject, add a Git submodule, pointing to the new submodule project
URL.
6. Commit and push the superproject, which will include the newly cre-
ated .gitmodules file.