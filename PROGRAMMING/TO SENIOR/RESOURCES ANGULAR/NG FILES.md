.vscode — The folder was created and replaced with e2e by the Visual Studio Code when the codebase was opened in the VS Code editor. It holds your project workspace settings.

node_modules/ — Provides npm packages to the entire workspace. We can open the folder and see the packages available.

Src/ — Contains all of the application’s code.

.editorconfig — Holds configuration for code editors.

.gitignore — Specifies intentionally untracked files that Git should ignore.

angular.json — Holds your angular app configuration.

package-lock.json — Records the exact version of every installed dependency, including its sub-dependencies and their versions.

package.json — Contains descriptive and functional metadata about a project, such as a name, version, and dependencies.

README.md — A Markdown file for documentation of the application.

tsconfig.app.json — It’s just an additional config file that allows you to adjust your configuration on an app basis. It is useful when we have multiple apps in the same Angular CLI workspace.

tsconfig.json — A general file that contains general typescript configuration. It’s beneficial where there are multiple Angular subprojects, each with its tsconfig.app.json configuration.

tsconfig.spec.json — It holds the TypeScript configuration for the application tests.