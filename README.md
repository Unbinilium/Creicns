## A light png to icns converter written in shell for macOS

## How it works?
The `.icns` file format is *Apple Icon Image* used on macOS, it may contained the icons of `16×16`, `32×32`, `48×48`, `128×128`, `256×256`, `512×512`, and `1024×1024` pixels in `.png` format.

Firstly we load raw icon image from the path you specialized, then use `sips` convert the raw icon image to `.png` format if it not a png originally. Secondly we use `sips` to resize the raw icon image into multiple png files with different sizes which meets the size requirements by `iconutil`, and store the resized png files in `.iconset`. Lastly the `.icns` could be created by using `iconutil`.

## Usage

Please download the script first by running this command below  in your `Terminal`:

```shell
curl https://raw.githubusercontent.com/Unbinilium/Creicns/master/creicns.sh --output creicns.sh
```

Then run `creicns.sh` in `Terminal` with raw images path augmented:

```shell
bash creicns.sh <raw image path>
```

For example:

```shell
bash creicns.sh /Desktop/Icon.png
```
