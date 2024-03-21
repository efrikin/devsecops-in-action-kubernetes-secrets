
# `Demo: Viper`

## `Usage`

### `Preparing`

```bash
cd viper
go mod download
echo 'MySecret' > secret.file
```

### `Run`

```bash
DEMO_SECRET__USER=user DEMO_SECRET__PASSWD="secret.file" go run main.go
DEMO_SECRET__USER=user DEMO_SECRET__PASSWD="file://secret.file" go run main.go
```

### `Checking`

```bash
ps e --no-headers -ww -p $(pidof main)

or

strings /proc/$(pidof main)/environ
```

## `References`

- [Decoding custom formats](https://github.com/spf13/viper?tab=readme-ov-file#decoding-custom-formats)
- [Decoding custom formats with Viper](https://sagikazarmark.hu/blog/decoding-custom-formats-with-viper/)

