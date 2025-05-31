# llm-shell


## 概要

`llm-shell`は、Simon Willison氏の[llm](https://github.com/simonw/llm)コマンドラインツールをzshと連携させ、ターミナル上でAIの力をより活用するためのシェルです。
gitやdockerのコマンドを忘れた際に、LLMをターミナルから呼び出し候補のコマンドを選択して使う事でUIでLLMに聞くより効率化出来ます

## 機能

- **候補の取得**: タスクの説明からコマンド候補を提案
- **クリップボード**: 選択結果を自動的にクリップボードにコピー

## 前提条件

- zsh
- [llm](https://github.com/simonw/llm)
- [fzf](https://github.com/junegunn/fzf)
- macOS（pbcopyコマンド使用）または適切なクリップボードツール

## 動作環境

**注意**: このツールは以下の環境でのみ動作確認をしています：
- macOS Sequoia 15.3.2
- iTerm2
- zsh


## インストール

1. llmのインストール
2. このリポジトリのコードを自身の .zshrc にコピー
3. 欲しいエイリアスを.zshrcに追加
4. llm keys set openai で、OpenAI APIキーを設定

## 使い方
```sh
$ gllm commitした後にファイル追加したけど、前のコミットに含めたい
```
候補が出るので選択肢、Cmd+Vでペースト