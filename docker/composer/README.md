Docker composer
---------------

# Build image

Create `auth.json` from `auth.json.dist`, [create a github token](https://github.com/settings/tokens/new) and replace `GITHUB_TOKEN` by your token. (This token only need `repo` and `public_repo` right)

Then

```cmd
docker build -t composer/composer .
```

# Bash alias

```cmd
alias composer="docker run --rm -it -v \$(pwd):/app -w /app composer/composer
```