# Translate Shell

[translate-shell](https://github.com/soimort/translate-shell) and global popup translate, currently translate text to Chinese only, supporting image(OCR) and pure text

### Showcase

|text|image|
|:---:|:---:|
|![text.gif](https://raw.githubusercontent.com/K1ngst0m/translate-shell/develop/res/text.gif)|![img.gif](https://raw.githubusercontent.com/K1ngst0m/translate-shell/develop/res/img.gif)|

image showcase example command, using [flameshot](https://github.com/flameshot-org/flameshot) for screencapture to get images and [tesseract](https://github.com/tesseract-ocr/tesseract) OCR engine
```shell
flameshot gui && xclip -o -sel clip -t image/png > /tmp/test.png && translator "$(tesseract /tmp/test.png stdout)"
```

### Build

``` shell
git clone https://github.com/K1ngst0m/translate-shell 
cd translate-shell 
make -j$(nproc) 
cd build/ && ls
```

### Dependencies
- gawk
- xclip
- flameshot
- dunst
