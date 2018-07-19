# i18n

[![GoDoc](https://godoc.org/github.com/gookit/i18n?status.svg)](https://godoc.org/github.com/gookit/i18n)

use `ini` files, simple i18n manager implement.

## Godoc

- [godoc for gopkg](https://godoc.org/gopkg.in/gookit/i18n.v1)
- [godoc for github](https://godoc.org/github.com/gookit/i18n)

## Usage

```text
conf/
    lang/
        en.ini
        zh-CN.ini
        ...
```

- init

```go
    import "github/gookit/i18n"

    languages := map[string]string{
        "en": "English",
        "zh-CN": "简体中文",
        // "zh-TW": "繁体中文",
    }

    i18n.Init("conf/lang", "en", languages)
```

- usage

```go
    // translate from special language
    str := i18n.Tr("en", "key")

    // translate from default language
    str = i18n.DefTr("key")
```

## dep packages

- [gookit/ini](https://github.com/gookit/ini) ini 解析管理

## License

MIT
