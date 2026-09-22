# Name of the GitHub Actions workflow
name: My First CI Pipeline


# 'on' defines when the workflow should run
on:

  # Automatically run the workflow when code is pushed
  # push:

  #   # Only run automatically when code is pushed to the main branch
  #   branches:
  #     - main

  # Allows us to manually run the workflow
  # GitHub → Actions → Run workflow
  workflow_dispatch:


# 'jobs' defines the work that GitHub Actions will perform
jobs:

  # Name of our job
  check-website:

    # Run this job on a temporary Ubuntu Linux machine
    runs-on: ubuntu-latest
    #github runner 

    # 'steps' contains the individual tasks of the job
    steps:

      # Step 1: Get/download our repository code
      # The runner is a fresh machine, so we need our project files
      - name: Checkout Code
        uses: actions/checkout@v4


      # Step 2: Check whether index.html exists
      - name: Check index.html

        # 'run' means execute Linux/Bash commands
        run: |

          # Check whether index.html exists
          if test -f index.html; then

            # If index.html exists, print Hello World
            echo "Hello World"

          # If index.html does not exist
          else

            # Print an error message
            echo "index.html not found"

            # Exit with error code 1
            # This makes the GitHub Actions step FAIL
            exit 1

          # 'fi' means the end of the Bash if statement
          fi