# foundry-tf-app-multi-env

[Cookiecutter](https://www.cookiecutter.io/) template to generate boilerplate for an application to be deployed as a multi-environment Terraform project.

## Pre-requisites

Install [cookiecutter](https://cookiecutter.readthedocs.io/en/stable).

We recommend using [uv](https://docs.astral.sh/uv/) to manage the Python environment. Below is one way to get started for [Homebrew](https://brew.sh) users. Follow the [cookiecutter installation instructions](https://cookiecutter.readthedocs.io/en/stable/installation.html) for other methods.

```sh
brew install uv
```

```sh
# uv python install ## (Optional) if you haven't installed python with uv yet
uv venv
source .venv/bin/activate
uv pip install cookiecutter
```

## Run

```sh
cookiecutter gh:Particle41/foundry-tf-app-multi-env
```

## Configurations

See the configuration options in [cookiecutter.json](cookiecutter.json).

## Structure

This cookiecutter will generate the following project skeleton:

```txt
.
├── .editorconfig
├── .envrc
├── .git-hooks
│   └── pre-commit
├── .gitignore
├── .ls-lint.yml
├── .terraform-docs.yml
├── .tflint.hcl
└── terraform
    ├── modules
    │   └── .gitkeep
    └── root
        ├── dev
        │   ├── backend.tf
        │   ├── dev.s3.tfbackend
        │   ├── main.tf
        │   ├── outputs.tf
        │   ├── providers.tf
        │   ├── README.md
        │   ├── variables.tf
        │   └── versions.tf
        └── live
            ├── backend.tf
            ├── live.s3.tfbackend
            ├── main.tf
            ├── outputs.tf
            ├── providers.tf
            ├── README.md
            ├── variables.tf
            └── versions.tf
```

## Authors

The Particle41 DevOps team.

Copied from the original copyleft: <https://github.com/andreswebs/tf-app-multi-env>

## License

This project is licensed under the [Unlicense](UNLICENSE.md).
