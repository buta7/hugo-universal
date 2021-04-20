# README

## セットアップ

サイト作成

```shell
hugo new site hugo-universal
```

レポジトリ初期化

```shell
cd hugo-universal
git init
echo '*~' >> .gitignore
echo '*.bak' >> .gitignore
echo '*.orig' >> .gitignore
echo '.env' >> .gitignore
echo 'public' >> .gitignore
echo 'resources' >> .gitignore
```

テーマ設定(submoduleはhttpsプロトコルで追加)

```shell
git submodule add https://github.com/devcows/hugo-universal-theme.git themes/universal
```

(参考)submoduleの削除

```shell
git submodule deinit -f themes/universal
git rm themes/universal
rm -fr .git/modules/universal
```

サイト設定

```shell
cp -p themes/universal/exampleSite/config.toml .
cp -pr themes/universal/exampleSite/{content,data} .
```

## Link

* [Hugo Universal Theme \| Hugo Themes](https://themes.gohugo.io/hugo-universal-theme/)
