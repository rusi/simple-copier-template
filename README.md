[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-purple.json)](https://github.com/copier-org/copier)

# Simple Copier Template

A simple template for creating new projects with Copier.

## Instantiate the Template

To instantiate the template for the first time:

1 Generate a project: Navigate to a directory where you want to instantiate
  the template and run:

```sh
copier copy gh:rusi/simple-copier-template my-project
```

2. Provide inputs: You will be prompted for the inputs defined in copier.yaml
   (e.g., `project_name`). Once done, the project will be generated.

```sh
cd my-project
```

## Update the Template

When you want to update the template:

1. Modify the template files: For example, add new features or update existing
   ones in the template, like adding new files or altering the existing ones.

2. Version the template: Ensure you version the template using Git tags or
   other version control methods. Example:

```sh
git tag v1.1.0
git push origin --tags
```

3. Update your project: In the project directory that was created from this
   template, run:

```sh
copier update
```

This will update your project with the latest changes from the template while
preserving your customizations.

## Apply Template to an Existing Project

You can apply a template to an existing project by first instantiating the template and then copying over relevant files or using Copier’s `--force` option if you want to overwrite.

1. **Copy template over an existing project**:
   Ensure you’re in the root of the project you want to update, and run:

   ```sh
   cd /path/to/your/project
   copier copy gh:rusi/simple-copier-template .
   ```

2. **Resolve conflicts**:
   Copier will identify any conflicts between the existing files and the template, and you can resolve them during the update process.

With this setup, your template is ready to evolve over time, and you can easily propagate changes to instantiated projects using the `copier update` command.
