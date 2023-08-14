# translate-spells

This tool translates English text into Japanese with `translate-shell`.  
It also reads out the English text naturally using Google Cloud `text-to-speech AI`.  
This tool is designed to run on Mac.

-----

本ツールは `translate-shell` により、英文を日本語訳します。  
また英文を、Google Cloud の `text-to-speech AI` により、自然に読み上げます。  
本ツールは Mac 上での動作を想定しています。

## Features

1. This tool caches `text-to-speech AI` executions in a directory called `spells` to suppress billing (Free up to 4 million characters per month .. As of Aug. 2023). You can delete the cache at any time.

1. This tool allows you to pass `translate-shell` arguments directly, as follows

   ```bash
   # -- followed by the translate-shell argument
   echo 'hello' | ./translate-spells -- -b
   ```

-----

1. 本ツールは `spells` というディレクトリに `text-to-speech AI` の実行結果をキャッシュし、課金を抑制しています。（月あたり400万文字まで無料 .. 2023/08 時点）キャッシュは、任意のタイミングで削除してください。

1. 本ツールは、以下のように `translate-shell` の引数を直接渡すことができます。

   ```bash
   # -- followed by the translate-shell argument
   echo 'hello' | ./translate-spells -- -b
   ```

## Requirement

- [text-to-speech AI](https://cloud.google.com/text-to-speech)
- curl
- base64
- translate-shell

## Installation

Refer to [this section](https://cloud.google.com/text-to-speech/docs/before-you-begin) and proceed to the "Set environment variables for authentication information" section.

```bash
brew update && brew upgrade
brew install curl base64 translate-shell
```

## Usage

```bash
git clone https://github.com/cresson-cat/translate-spells.git
cd ./translate-spells
chmod x+u ./translate-spells
echo 'hello' | ./translate-spells
```

## Author

- aider
 
## License
 
"translate-spells" is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).
