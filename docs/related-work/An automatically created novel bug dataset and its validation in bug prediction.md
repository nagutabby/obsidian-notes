---
title: An automatically created novel bug dataset and its validation in bug prediction
---
## アブストラクト
- ソフトウェア開発においては、頻繁なコード変更や厳しい納期などにより、バグの発生は避けられない
- そのため、このミスを見つけるためのツールが不可欠
- バグを特定する1つの方法としては、過去のバグのあるソースコード要素の特性を分析し、同じ特性に基づいて現在のバグを予測することがある
- BugHunterデータセットを紹介
	- ファイル、クラス、メソッドからなるコード要素、幅広いコードメトリクス、バグ情報を含む自動で構築されたバグデータセット
- 既存のバグデータセットでは、事前に選ばれたリリースバージョンにおけるすべてのソースコード要素の特性が収集されていた
- BugHunterデータセットは、バグの存在を特定できる最も狭い期間において、同じソースコード要素のバグあり状態と修正済み状態を捉える
- 新しいデータセットは、バグ予測モデルにおいてF1スコア0.74を達成
## はじめに
- バグのあるソースコード要素の特性評価は近年注目されている研究分野である
- 未知の欠陥のあるコード要素を識別するには既知の欠陥のあるコード要素の特性評価が必要
- ソフトウェア開発においてプログラマーはバグ追跡、タスク管理、バージョン管理システムなどの様々なツールを使用
- これらのツールのほとんどにバグ追跡機能が含まれているため、この情報を使用してバグのあるソースコードの特徴付けを行える
	- 実際に特徴付けを行うには、ソースコードのホスティングプロバイダーが管理しているバグレポートを適切なソースコードに関連付ける必要がある
	- コミットメッセージに含まれるバグレポートのリンクを使用することで、問題のあるソースコードが追加されたバージョンを特定できる
- バグのあるコードの特性に関する有用な情報を含むデータセットを構築するために、GitHubを選択した
	- GitHubには、定期的にメンテナンスされている複数のプロジェクトがホストされており、自動データ取得ツールを実装するためのAPIも備わっているため
- 対象システムとして15のJavaプロジェクトを選択した
	- これらのプロジェクトは、規模、ドメイン、報告されたバグの数などの様々な点で互いに異なる
- これまでに公開されたデータセットはには、分析対象システムの1つ以上のバージョンからのすべてのコード要素（バグのあるものとないものの両方）が含まれる
- 本研究では、バグの影響を受けたコード要素とその特性の修正前と修正後のスナップショットを収集し、バグの影響を受けなかったコード要素は考慮しないという新しいアプローチを作成した
- このデータセットは、バグ修正時のコードメトリクスの変化を捉えるのに役立つ
- 新しいデータセットはBugHunter Datasetと呼ばれ、無料で入手できる
- この新しいデータセットがバグ予測に適しているかどうかを確認するための実験も行った
## 関連研究#
### バグの特定とソースコード管理
- バグの特性評価と位置特定については、多くのアプローチが発表されている
	- BugLocator: バグレポートとソースコードの間のテキストの類似性を使用して問題が発生しやすいファイルをランク付け
	- ReLink: バージョン管理システムでコミットされたコード変更と修正されたバグとの間の関連性を探索
- これらのツールは、SZZアルゴリズムを使用して要る
	- SZZアルゴリズムはファイルレベルのテキストの特徴を使用してバグとソースコードの間の追加情報を抽出
- バグ追跡システムによって管理されるバグレポートを使用して、ソフトウェアシステム内のバグのあるファイルを迅速に見つける方法が紹介された
### 公開データセット
- PROMISE: オープンソースやクローズドソースの産業用ソフトウェアシステムから収集されたバグが含まれている
- Bug prediction dataset: クラスとバグを関連付けている
- iBUGS: 自動的にソフトウェアの欠陥位置を特定する方法をテストするための環境を提供
- Bugcatchers: 対象システムで検出されたバグとコードの臭いを含んでいる
- ELFF: メソッドレベルのデータセット
- Had-oops!: 連続する8つのHadoopのバージョンを分析し、時系列が欠陥予測のパフォーマンスに与える影響を調査
## データソース
### GitHub
- 最も人気のあるソースコードホスティングサービスの1つ
- バグ追跡システム、イシュー追跡システムなどの共同作業支援サービスも提供
- レポートにバグラベルを追加するとバグレポートとして分類でき、コミットメッセージからバグレポートのIDを参照することでバグとイシューを関連付けられる
- GitHubには、他のシステムのリポジトリを管理したり、それらに関する情報を調べたりするために使用できるAPIがある
### 選ばれたプロジェクト
- Javaで書かれている
- 規模が大きい
- バグとしてラベル付けされたイシューの数が十分である
- コミットメッセージから特定のバグ混入コミットを参照している
- 現在も積極的にメンテナンスされている
- スターとウォッチの数の合計を人気度と定義し、人気度を参考にした
- 選択されたプロジェクト
	- Android Universal Image Loader
		- [https://github.com/nostra13/Android-Universal-Image-Loader](https://github.com/nostra13/Android-Universal-Image-Loader)
	- ANTLR v4
		- [https://github.com/antlr/antlr4](https://github.com/antlr/antlr4)
	- Elasticsearch
		- [https://github.com/elastic/elasticsearch](https://github.com/elastic/elasticsearch)
	- MapDB
		- [https://github.com/jankotek/MapDB](https://github.com/jankotek/MapDB)
	- mcMMO
		- [https://github.com/mcMMO-Dev/mcMMO](https://github.com/mcMMO-Dev/mcMMO)
	- Mission Control Technologies
		- [https://github.com/nasa/mct](https://github.com/nasa/mct)
	- Neo4j
		- [https://github.com/neo4j/neo4j](https://github.com/neo4j/neo4j)
	- Netty
		- [https://github.com/netty/netty](https://github.com/netty/netty)
	- OrientDB
		- [https://github.com/orientechnologies/orientdb](https://github.com/orientechnologies/orientdb)
	- Oryx 2
		- [https://github.com/OryxProject/oryx](https://github.com/OryxProject/oryx)
	- Titan
		- [https://github.com/thinkaurelius/titan](https://github.com/thinkaurelius/titan)
	- Eclipse plugin for Ceylon
		- [https://github.com/eclipse/ceylon-ide-eclipse](https://github.com/eclipse/ceylon-ide-eclipse)
	- Hazelcast
		- [https://github.com/hazelcast/hazelcast](https://github.com/hazelcast/hazelcast)
	- Broadleaf Commerce
		- [https://github.com/BroadleafCommerce/BroadleafCommerce](https://github.com/BroadleafCommerce/BroadleafCommerce)
## メトリクス

## 引用情報
- 著者: Rudolf Ferenc, Péter Gyimesi, Gábor Gyimesi, Zoltán Tóth, Tibor Gyimóthy
- タイトル: An automatically created novel bug dataset and its validation in bug prediction
- 雑誌 / 会議名: Journal of Systems and Software
- 巻号: vol. 169
- ページ: p. 110691
- 出版日: November 2020
- DOI: https://doi.org/10.1016/j.jss.2020.110691
