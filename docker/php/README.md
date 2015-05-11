PHP CLI
-------

# Build image

```cmd
docker build -t php/php-cli .
```

# Alias

```cmd
alias php="docker run --rm -it -v \$(pwd):/app -w /app php/php-cli"
```
