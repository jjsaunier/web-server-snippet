Node tools
-----------

# Build image

sudo docker build -t node/tools .

# Bash aliases

### Node

```cmd
alias node="docker run --rm -it -v \$(pwd):/app node/tools node"
```

### NPM

```cmd
alias npm="docker run --rm -it -v \$(pwd):/app node/tools npm"
```
docker
### Bower

```cmd
alias bower="docker run --rm -it -v \$(pwd):/app node/tools bower --allow-root --config.interactive=false"
```

### Gulp

```cmd
alias gulp="docker run --rm -it -v \$(pwd):/app node/tools gulp"
```

### Grunt

```cmd
alias grunt="docker run --rm -it -v \$(pwd):/app node/tools grunt"
```
