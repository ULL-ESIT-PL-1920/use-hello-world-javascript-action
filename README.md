# use-hello-world-javascript-action


[![Using hello world](https://github.com/ULL-ESIT-PL-1920/use-hello-world-javascript-action/workflows/Using%20hello%20world/badge.svg?event=push)](https://github.com/ULL-ESIT-PL-1920/use-hello-world-javascript-action/actions)

<!--
[![Actions Status](https://github.com/ULL-ESIT-PL-1920/{repo}/workflows/{workflow_name}/badge.svg)](https://github.com/{owner}/{repo}/actions)
-->

## gh workflow

See gitHub blog [GitHub Actions: Manual triggers with workflow_dispatch](https://github.blog/changelog/2020-07-06-github-actions-manual-triggers-with-workflow_dispatch/)

You can now create workflows that are manually triggered with the new `workflow_dispatch` event.

You will then see a **Run workflow** button on the Actions tab, enabling you to easily trigger a run.

![](images/run-workflow.png) 

```
➜  use-hello-world-javascript-action git:(master) gh help workflow
List, view, and run workflows in GitHub Actions.

USAGE
  gh workflow <command> [flags]

CORE COMMANDS
  disable:    Disable a workflow
  enable:     Enable a workflow
  list:       List workflows
  run:        Run a workflow by creating a workflow_dispatch event
  view:       View the summary of a workflow

FLAGS
  -R, --repo [HOST/]OWNER/REPO   Select another repository using the [HOST/]OWNER/REPO format

INHERITED FLAGS
  --help   Show help for command

LEARN MORE
  Use 'gh <command> <subcommand> --help' for more information about a command.
  Read the manual at https://cli.github.com/manual



A new release of gh is available: 1.9.1 → v1.9.2
To upgrade, run: brew update && brew upgrade gh
https://github.com/cli/cli/releases/tag/v1.9.2
```

### Example


```
gh workflow run manual.yml -f name=PL2021
```

To view a workflow:

```
➜  use-hello-world-javascript-action git:(master) ✗ gh workflow view --help
View the summary of a workflow

USAGE
  gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]

FLAGS
  -r, --ref string   The branch or tag name which contains the version of the workflow file you'd like to view
  -w, --web          Open workflow in the browser
  -y, --yaml         View the workflow yaml file

INHERITED FLAGS
      --help                     Show help for command
  -R, --repo [HOST/]OWNER/REPO   Select another repository using the [HOST/]OWNER/REPO format

EXAMPLES
  # Interactively select a workflow to view
  $ gh workflow view
  
  # View a specific workflow
  $ gh workflow view 0451

LEARN MORE
  Use 'gh <command> <subcommand> --help' for more information about a command.
  Read the manual at https://cli.github.com/manual
```

### Exercise

Add a manual trigger workflow with `workflow_dispatch` to your Egg repo so that you can execute any Egg example with `gh` or in the browser:

```
gh workflow run egg.yml -f program=two.egg
```
