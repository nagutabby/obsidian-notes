---
title: "AutoODC: Automated generation of orthogonal defect classifications"
---
## アブストラクト
- ソフトウェア欠陥の分類と分析において最も影響力のあるフレームワークであるOrthogonal defect classification（ODC）は、システム開発と保守に貴重なフィードバックを提供
- 既存のODC分類は人的リソースを必要とし、ODCとシステムドメインの両方に関する専門家の知識が必要
- この論文では、ODC分類を教師ありテキスト分類問題として捉え、自動化する手法であるAutoODCを紹介
- 標準的な機械学習フレームワークをこのタスクに単に適用するのではなく、新しい関連性アノテーションフレームワークを提案することで、専門家のODC経験とドメイン知識を学習プロセスに統合し、より優れたODC分類システムの構築を目指す
- この論文では、ナイーブベイズとサポートベクターマシンを用いてAutoODCを学習し、ソーシャルネットワークドメインの産業欠陥レポートと、オープンソースシステムであるFileZillaの欠陥追跡ツールから抽出した大規模な欠陥リストの両方で評価
- 産業欠陥レポートではナイーブベイズで82.9%、サポートベクターマシンで80.7%の精度を達成
- オープンソース欠陥リストではナイーブベイズで77.5%、サポートベクターマシンで75.2%の精度を達成

## 引用情報
- 著者: LiGuo Huang, Vincent Ng, Isaac Persing, Mingrui Chen, Zeheng Li, Ruili Geng, Jeff Tian
- タイトル:  AutoODC: Automated generation of orthogonal defect classifications
- 雑誌 / 会議名: Automated Software Engineering
- 巻号: vol. 22
- ページ: pp. 3-46
- 出版日: June 2014
- DOI: https://doi.org/10.1007/s10515-014-0155-1
