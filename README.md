# How to use

1. Create .pre-commit-config.yaml in code repo with the following contents

""" 
repos:
  - repo: https://github.com/FraserSingh/pre-commit-setup
    rev: v1.0.4 # update this to latest tag on GitHub 
    hooks:
      - id: black
      - id: ruff
      - id: nbstripout
      - id: bandit
      - id: detect-secrets
      - id: sqlfluff-lint
      - id: sqlfluff-fix
"""
2. In CLI: cd <project repo dir> ; pre-commit clean ; pre-commit install ; pre-commit run --all-files
3. (Optional) If you want to customise hook behaviour, copy pyproject.toml from this repo to project repo and alter args / flags




# Contributing

1. Alter pre-commit=hooks.yaml
1. Commit changes and tag with new version number
1. push tag and commit
1. Advise users to change tag number in their yaml files