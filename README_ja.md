<!-- @head-content@ -->
# laplacian/project.schema-model

このモデルは*Laplacian*プロジェクトの論理構造を表します。


*Read this in other languages*: [[English](README.md)] [[简体中文](README_zh.md)]
<!-- @head-content@ -->

<!-- @toc@ -->
## Table of contents
1. [概要](#概要)
1. [使用方法](#使用方法)
1. [インデックス](#インデックス)


<!-- @toc@ -->

<!-- @main-content@ -->
## 概要


### モデル概要


以下の図は、このモジュールに含まれる各エンティティの内容とそれらの間の関係を表しています。
![](./doc/image/model-diagram.svg)
### エンティティ一覧


- [**Document**](<./doc/entities/Document.md>)
document
- [**Section**](<./doc/entities/Section.md>)
section
- [**Module**](<./doc/entities/Module.md>)
module
- [**Project**](<./doc/entities/Project.md>)
project
- [**ProjectType**](<./doc/entities/ProjectType.md>)
project_type
- [**Script**](<./doc/entities/Script.md>)
script
- [**ScriptOption**](<./doc/entities/ScriptOption.md>)
script_option
- [**SourceRepository**](<./doc/entities/SourceRepository.md>)
source_repository

## 使用方法

この modelモジュールを適用するには、プロジェクト定義に以下のエントリを追加してください。
```yaml
project:
  models:
  - group: laplacian
    name: project.schema-model
    version: 1.0.0
```

下記のコマンドを実行すると、このモジュールの適用によって影響を受ける資源の一覧とその内容を確認できます。

```console
$ ./script/generate --dry-run

diff --color -r PROJECT_HOME/.NEXT/somewhere/something.md PROJECT_HOME/somewhere/something.md
1,26c1,10
< content: OLD CONTENT
---
> content: NEW CONTENT
```

内容に問題が無ければ、下記コマンドを実行して変更を反映してください。

```console
$ ./script/generate --dry-run

```


## インデックス


### ソースコード一覧


- [model/project.yaml](<./model/project.yaml>)
- [src/entities/document_section.yaml](<./src/entities/document_section.yaml>)
- [src/entities/document.yaml](<./src/entities/document.yaml>)
- [src/entities/module.yaml](<./src/entities/module.yaml>)
- [src/entities/project/examples.yaml](<./src/entities/project/examples.yaml>)
- [src/entities/project_type.yaml](<./src/entities/project_type.yaml>)
- [src/entities/project.yml](<./src/entities/project.yml>)
- [src/entities/script_option.yaml](<./src/entities/script_option.yaml>)
- [src/entities/script.yaml](<./src/entities/script.yaml>)
- [src/entities/source_repository.yaml](<./src/entities/source_repository.yaml>)


<!-- @main-content@ -->