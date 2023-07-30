# Malina Bot
This repo is an experiment using retrieval augmented generation to create a chatbot.

# Environment Setup
## Environment Variables
The following environment variables are used to interact with OpenAI API:

|Name | Description |
|---|---|
|OPENAI_API_KEY | Your OpenAI API Key |

## Dependencies
To install locally, you'll need the following:

 * [Homebrew](https://brew.sh)
 * [Pyenv](https://github.com/pyenv/pyenv)
 * [Poetry](https://python-poetry.org)

These instructions assume you are using macOS. For other operating systems, see the [Cloud-based Development](#cloud-based-development) section below.

### Homebrew
Install `homebrew` with the following command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Pyenv
Use `homebrew` to install `pyenv`:

```
brew update
brew install pyenv
```

Add the following to `~/.zshrc` (see [Set up your shell environment for Pyenv](https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv) for other shells):

```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

### Poetry
Install `poetry` with the following command:

```
curl -sSL https://install.python-poetry.org | python3 -
```

Add `poetry` to your path in `~/.zshrc`:

```
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
```

## Set up the project
Clone the repository:

```
git clone git@github.com:jeffdevine/malina-bot.git
cd malina-bot
```

Install the Python version specified in `.python-version`:

```
pyenv install
```

Install the project dependencies:

```
poetry install
```

To start a shell in the project's virtual environment, run the following command:

```
poetry shell
```

## Cloud-based Development
This project supports using Github Codespace (https://github.com/features/codespaces) to develop either in a web browser or locally using Visual Studio Code Remote (https://code.visualstudio.com/docs/remote/containers).

### Creating a CodeSpace

 1. Go to the https://github.com/jeffdevine/malina-bot.
 2. Click `< > Code`, then click `Create codespace on main`.
