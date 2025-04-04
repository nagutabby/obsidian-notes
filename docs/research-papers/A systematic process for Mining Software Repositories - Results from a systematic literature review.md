---
title: "A systematic process for Mining Software Repositories: Results from a systematic literature review"
---
## アブストラクト
- 体系的なMSR研究をどのように実施するかについてのガイドラインがない
	- MSR研究を体系的に行うための枠組みを提供するために、MSR研究がどのように行われているかを評価する必要がある
- リポジトリの選択とデータ抽出に関してMSR研究がどのように実施されているかを明らかにする
- Mianらによって提案されたガイドラインとテンプレートに従い、MSR研究の体系的なレビューを実施
- MSR研究は通常、リポジトリ選択のための体系的な方法に従っておらず、選択手順やデータ抽出手順を報告していない
- さらに、データ抽出の流れに起因する研究の有効性に対する脅威を議論している原稿はほとんどない
	- そのため、体系的なMSR研究をどのように実施するかについてのガイドラインが必要
- 新しいガイドラインとテンプレートが提案された
## はじめに
- MSR研究では、研究者は特定の基準に適合するリポジトリを選択し、そこからデータを抽出し、データを分析して、研究上の疑問に応えるための証拠を得る
- MSR研究はエビデンスに基づく研究と考えられているため、構造化された再現性のある研究を作成するためのガイドラインを持つことが重要
- しかし、プロセス全体を導くための枠組みや方法論について考えたメタ研究は存在しない
- この論文は、MSR研究の信頼性を向上させ、リポジトリがどのように選択されるかを理解し、ソフトウェアリポジトリをマイニングするための体系的なプロセスを定義する必要性に基づくものである
- この研究の主な貢献
	- システマティックレビューを通じて、ソフトウェアエンジニアリングにおけるMSR研究の現在の慣行を評価
## 背景、関連研究、動機
- MSRでは、ソースは、バージョン管理やバグレポートプロジェクトをホストするためのプラットフォーム、メーリングリスト、さらにはStack Overflowなど、さまざまなタイプにすることができる
- 関連研究
	- 研究の目的に焦点を当ててMSR研究を分類したもの
	- マイニングされたデータから情報を抽出するために使用される方法に焦点を当ててMSR研究を分類したもの
	- これらの研究はいずれも、リポジトリの選択、データ抽出、情報マイニングに使用されるプロセスの構造化に焦点を当てていない
	- リポジトリから抽出できるデータはデジタルトレースデータ (DTD) と呼ばれる
	- この品質を高めるためには、7つのWとの関連を明らかにする必要がある
		- 7つのWとは、What (データがに何が取り込まれているか)、When (収集のタイミング)、Where (データ抽出のためのリポジトリがあるソース)、How (リポジトリからデータを収集するプロセス)、Who (収集にかかわる個人)、Which (データを収集するために使用された機器またはアーティファクト)、Why (データを収集する理由や目標) である
	- この原稿で提案されたガイドラインには、テンプレートとプロセス全体にわたって7つのWが含まれている
- この研究は、メタ研究で議論された情報を統合し、分かりやすいテンプレートを提供することによって、体系的なMSRの採用を簡素化することを目指している
## 方法
- RQ1
	- MSRに基づく論文は、リポジトリとデータ抽出を選択するために、明確に定義された特定の流れと手順を使用しているか？
- RQ2
	- どのリポジトリソースが使用され、どのデータが抽出されるか？
- RQ3
	- 体系的なプロセスを定義するために、リポジトリの選択中にどのような条件 (包含/除外基準) が課されているか？
- RQ4
	- MSRに基づく研究は、リポジトリの選択に関して、妥当性に対する脅威を議論しているか？
- 検索式
	- mining software repositories OR repository mining OR msr OR software repository selection) AND (github OR bitbucket OR gitlab OR stackoverflow
- IEEE Xplore, ACM, ScienceDirect, Springer Linkから検索
- 関連研究は、MSR研究のおよそ90%がオープンソースソフトウェアを使用していると結論付けている
## 結果
- RQ1の回答
	- 原稿のおよそ37%はリポジトリの選択プロセスを扱っておらず、選択の流れを詳述していない
	- それにもかかわらず、著者はリポジトリからデータを抽出するために実行された手順と流れを記述する傾向がある
	- 原稿のほぼ70%には、データセット生成専用のセクションがあった
	- 論文のおよそ17%はリポジトリ選択プロセスを記述していなかったが、データ抽出について詳しく説明していた
	- 大規模で事前定義されたリポジトリで作業した原稿はおよそ30%のみである
	- Eclipse, Linux, Apacheが最も使用されている
	- 一部の原稿は、プロジェクトの人気、規模、存続期間を基にリポジトリを選択している
	- 体系的な選択プロセスを提示した原稿はわずか17%である
	- およそ28%が包含/除外基準を明確にした
	- ランダムサンプリングは計算制限や人為的案制限による収集境界であるため、選択基準に従っていれば、体系的であると考えられる
- RQ2の回答
	- 選択された原稿のうち、およそ10%が研究で複数のソースを使用し (例えば、Stack OverflowとGitHubのデータを組み合わせる)、残りは単一のソースに焦点を当てていた
	- 最も一般的なソースはGitHubで67%であり、次いでSourceForgeで8%、Bugzillaで7.5%である
	- 原稿の16%が選択されたリポジトリの数に言及しておらず、最近ではこの傾向が強まっている
	- ソースの選択は、収集する必要があるデータの種類によって決められる
		- 例えば、バグデータにはBugzillaやJIRAリポジトリを選択する必要があるが、バージョン管理にはGitHub, Azure, BigBucketを選択できる
	- 1つのソースが複数の種類のデータを提供できるため (例えば、GitHubはユーザーデータ、バージョン管理データ、メタデータ、ソースを同時に提供できる)、原稿のおよそ27%が複数のターゲットを持っている
	- バージョン管理データ、ソースコード、メタデータが最も一般的な種類のデータである
- RQ3の回答
	- リポジトリを選択するための包含/除外基準で最も一般的なものはプログラミング言語である
	- 他の一般的な選択肢は、特定のファイル (Readmeファイル、Mavenのpom.xmlなど) の検索と、コントリビューターの数や特定のバージョン管理イベントによるフィルタリングである
	- バージョン管理イベントには、分岐、コミット、マージ、リバートが含まれる
	- 9つの原稿は、リポジトリがオリジナルであるか、別のリポジトリから分岐しているかを考慮している
	- しかし、ターゲットリポジトリが何回分岐したか (フォークの数) を考慮していたのは5つの原稿のみである
	- いくつかの論文は英語専用の自然言語処理を扱っていたにもかかわらず、プロジェクト言語 (すなわち自然言語) に明示的に言及した論文はほとんどなかった
- RQ4の回答
	- 妥当性の脅威についての議論は、実証研究の鍵である
	- しかし、およそ69%の原稿が2つの基本的な妥当性の脅威に対処していないことは問題である
		- 1つ目は、リポジトリの選択から生じるバイアスや問題である
		- 2つ目は、データ抽出プロセスやソースから提供されたデータによって引き起こされるバイアスである
	- 両方の場合について議論した原稿はわずか13%で、残りの17.8%はどちらか一方について議論している
## 体系的なMSR研究のためのガイドライン
- G1.1. 疑問の焦点の定義
	- 関心のあるMSRの焦点、すなわち研究目的を定義
- G1.2. 疑問の質と広さの定義
	- MSRが提要される状況を明確にするために、研究課題を定義
	- 特に、以下の情報が含まれていなければならない
		- 疑問
			- MSR研究を通じて回答される研究上の疑問
		- 介入
			- 計画されたMSRの文脈で何が観察されているか
		- 制御
			-　研究者が利用できるベースラインや初期データセット
			- 例: リポジトリ、データテンプレートすなわち対象とするフォーマット、以前の研究からの情報サンプル
		- 効果
			- MSR研究の終了時に予想される結果の種類
			- これにより、結果から情報、それに必要なデータ、それをホストするリポジトリ、およびソースへの流れを参照できる
		- 結果を測定するための指標
			- 効果を測定するために使用される指標
			- 達成される効果の種類に依存
		- 集団
			- 研究で観察されたグループを定義
			- MSR研究では、このグループは、選択され、その後に研究で使用される特定データを抽出するためにマイニングされるリポジトリを意味する
		- 実験計画
			- 実施されるメタ分析
			- データから情報に移動し、その結果を解釈するための分析方法を定義
- G2.1. ソース選択基準の定義
	- リポジトリの種類の定義
		- 選択するリポジトリの種類を定義
			- 抽出するデータの種類を考慮する必要があり、例えば、ソースコードのみを要求すると、Bugzillaが除外される可能性がある
			- Whereに該当するもの
		- 目的の定義
			- データを収集するための一連の理由や目標を提供する
			- Whyに該当するもの
- G2.2. ソースの特定と説明
	- MSRを実行するためのソースの選択について説明
	- 以下の内容が含まれる
		- ソースの検索方法
			- Webエンジンを介してソースを検索する方法を説明
			- これには、特定のリポジトリダウンロード/マイニングツール (GHTorrentやGitHub Archiveなど) の使用が含まれる場合がある
			- 検索の制約 (GitHub検索の戻り値の制限、Stack Overflowの毎日のクエリ制限など) については、ここで説明する必要がある
		- 選択言語
			- リポジトリやコードを文書化する必要がある言語を定義
				- 研究が自然言語 (コメント、コミットメッセージ、Readmeファイルなど) に依存してデータを評価する場合は、研究がデータを読み、処理ツールを適用するためにデータを制限する必要がある場合があるため
			- ソースの一覧
				- MSR研究が実行される最初のソースの一覧
- G2.3. ソースの選択
	- ソースが全ての基準に適合する場合は、それを最終的なソースの一覧に含める
- G2.4. 参照事項の確認
	- 1人以上の専門家が、前の項目から取得したソースの一覧を評価する必要がある
	- この過程には、アクセス権限とデータ転送クォータのテストと確認、ドキュメントの確認、熟練者や専門家との対話が含まれる
	- バイアスを最小限に抑えるように設計されたピアレビューが含まれ、内部または外部で実施される
- G3.1. リポジトリの定義
	- リポジトリの選択方法を定義
	- 以下の内容が含まれる
		- リポジトリの説明
			- リポジトリの性質と、リポジトリが必要なデータを生成できる理由を説明することで、Whatに回答
		- リポジトリのタイミング
			- Whenに回答
			- 同じ基準で実行された場合であっても、リポジトリの選択は、異なる時間に実行されると異なる結果をもたらす可能性がある
			- これは、リポジトリの選択とダウンロードが行われた日付である
		- 包含/除外基準の定義
			- リポジトリを選択する必要があるかどうかを決めるために、リポジトリを評価する基準を示す
		- リポジトリの選択手順
			- リポジトリを取得し、除外/包含基準に従って評価する手順を説明
			- プロセスに複数のフィルタリングステップがある場合は、全ての段階を説明する必要がある
		- 検索文字列
			- ソースの検索エンジンで使用されるキーワード
			- この項目では、検索エンジンから最も多くの関連するリポジトリが取得されるように配置されたキーワードを組み合わせた論理式のセットを提示する必要がある
			- MSRでは、多くのソースが検索によって提供される結果に関して異なる制限を持っている (例えば、GitHubはクエリごとに最大1000個のリポジトリしか返さない)
			- 適用できる検索方法の例
				- 同じソースで複数の検索を実行し、後続の検索文字列の場合は検索結果から、すでに収集されたリポジトリを除外
				- NOT検索を利用してデータ収集に必要な時間を短縮し、包括的なサンプルを確保
- G4.1. 選択の実行
	- リポジトリの選択手順を実施し、評価の結果を報告
	- 以下の内容が含まれる
		- リポジトリの初期選択
			- 研究者が検索を実行し、さらに評価するために全てのリポジトリを一覧にする
		- リポジトリの品質評価
			- リポジトリの品質は、取得される結果に影響を与える可能性があるため、ある程度の品質を確保する必要がある
			- フィルタリングの段階を記録し、それぞれの段階で破棄または追加されたリポジトリの数を詳細に記録する必要がある
			- サンプリングに偏りがないことを確認
			- 結果をある程度一般化できるようにする
			- 研究に必要なデータを提供できるようにする
			- 利用できる場合は、研究に関連する適切な外部の品質測定を使用
				- 例: GitHubでの人気やフォーク数、CRANやPyPiでのインストール数
		- 選択のレビュー
			- リポジトリの選択において、関連するリポジトリが除外されなかったことを保証するためにレビューする必要がある
- G5.1. データ抽出
	- リポジトリからデータを抽出するためのマイニング手順を記述
	- 以下の内容が含まれる
		- データの包含/除外基準の定義
			- 取得したデータから新たなデータを抽出するための基準
			- 必要なデータの種類が定義される
			- 以下の内容が含まれる
				- デジタルトレースデータの性質とその品質、それが疑問とどのように関連しているかについての説明 (Whatに回答)
				- 抽出と解析の日付 (Whenに回答)
		- 抽出の実行
			- Howに回答するために、データ収集とマイニングの正確な手順を記述
			- これには、マイニングアルゴリズム、データベース間のデータの交差などに必要な手順、リスクを最小限に抑えるためのヒューリスティッククリーニングなどが含まれる
			- さらに、データの収集に使用された機器またはアーティファクトを詳細に記述する必要がある
			- マイニングアルゴリズムを実行するための言語とツール、前処理と構造化、手順に含まれるハードウェア、処理時間を具体化
		- データ抽出フォーマット
			- データの表現方法を標準化し、リポジトリからデータを収集するためのフォームを作成する必要がある
- G6.1. 情報基準の定義
	- データから得られた情報を評価する際の基準
- G6.2. 情報抽出の実行
	- 取得する情報に応じて2つの異なるプロセスを実行できる
		- 手動プロセス
			- 教師あり学習に必要
			- 以下のことを説明する必要がある
				- 手動評価を完了するために必要な手順
				- ゴールドデータ (訓練データおよびテストデータ) がどのように定義され、取得されるか (サンプルサイズやゴールドデータを決定するために使用される統計的手順を含む)
				- 情報を表すために使用される形式を標準化するための情報抽出フォーム
				- 誰が (Who) 手動ステップを完了したか、彼らの作業の妥当性に対する潜在的な脅威、それがどのように対処されたか、ステップに含まれるレビュー担当者
		- 自動プロセス
			- G3.3. (データ抽出) と同様の詳細が含まれる How (情報を収集し、交差し、検証するための正確なプロセスを記述する) やWhich (このプロセス中に使用されるツールを含める)
- G6.3. 情報抽出フォーマット
	- 情報の表現方法を標準化
- G6.4. 感度分析
	- 結果の頑健性を検証する必要がある
	- つまり、特定のリポジトリやデータの包含・除外における不確実性を調査することを意味する
- G7.1. 結果の提示
	- 分析から得られた結果を、容易に分析できるように表示
- G7.2. 最終コメント
	- 以下の項目について議論
		- マイニング数
			- データ抽出に関連する最終的な量 (イシューの数、コミットメッセージの数など)
			- これには、情報を生成するためにリポジトリから抽出されたデータのみが含まれ、リポジトリに含まれる全てのデータは含まれない
		- 検索・選択・抽出バイアス
			- 結果を無効にする可能性があるバイアスを記述
			- 以下の3種類の脅威に対処する必要がある
				- リポジトリバイアス
					- リポジトリの選択がデータ抽出に影響を与える可能性がある
				- データバイアス
					- リポジトリから抽出されたデータの有効性に問題がある可能性がある
				- 情報バイアス
					- 一部のアルゴリズムにはバイアスがかかっていたり、結果に影響を与える固有の問題があったりする可能性がある
## 影響
- MSRはEBSE (Evidence-Based Software Engineering) の一種
## 結論
- MSRとSLRは手順が似ているため、SLRの手順を基にMSRの手順を提案した
## 引用情報
- 著者: M. Vidoni
- タイトル: A systematic process for Mining Software Repositories: Results from a systematic literature review
- 雑誌 / 会議名: Information and Software Technology
- 巻号: vol. 144
- ページ: p. 106791
- 出版日: April 2022
- DOI: https://doi.org/10.1016/j.infsof.2021.106791
