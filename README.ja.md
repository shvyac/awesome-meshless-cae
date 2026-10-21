# Awesome Meshless CAE(メッシュレスCAE) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English](README.md) | **日本語**

> **従来のメッシュ生成を必要としない(または大幅に簡略化できる)** CAEツールのキュレーションリストです。粒子法、格子ボルツマン法、MPM、ペリダイナミクス、アイソジオメトリック解析、ボクセル / イマーシブ境界法、AIサロゲートを扱います。

## 目次

- [粒子法(SPH / MPS)](#粒子法sph--mps)
- [格子ボルツマン法(LBM)](#格子ボルツマン法lbm)
- [メッシュフリー固体力学(EFG / ペリダイナミクス / MPM)](#メッシュフリー固体力学efg--ペリダイナミクス--mpm)
- [ボクセル / イマーシブ境界法](#ボクセル--イマーシブ境界法)
- [アイソジオメトリック解析(IGA)](#アイソジオメトリック解析iga)
- [AI / サロゲートモデル](#ai--サロゲートモデル)
- [選び方の目安](#選び方の目安)
- [注意点](#注意点)
- [関連リスト](#関連リスト)
- [コントリビュート](#コントリビュート)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

凡例: 🆓 オープンソース(GitHub / GitLab) · 💼 商用

## 粒子法(SPH / MPS)

自由表面、飛散、スロッシング、潤滑、大変形に向いています。

- 🆓 [DualSPHysics](https://github.com/DualSPHysics/DualSPHysics) - GPU対応のSPHソルバー。
- 🆓 [SPlisHSPlasH](https://github.com/InteractiveComputerGraphics/SPlisHSPlasH) - SPH流体シミュレーションライブラリ。
- 🆓 [PySPH](https://github.com/pypr/pysph) - SPH用のPythonフレームワーク。
- 💼 [Particleworks](https://prometech.co.jp/en/) - MPS法ベースの粒子ソルバー(プロメテック・ソフトウェア)。
- 💼 [Altair nanoFluidX](https://help.altair.com/hwcfdsolvers/nfx/topics/nanofluidx/overview_nanofluidx_r.htm) - パワートレイン / eモーターの潤滑向けGPU SPH。
- 💼 [LS-DYNA (SPH)](https://www.ansys.com/products/structures/ansys-ls-dyna) - 流体構造連成や高速衝突向けのSPH。

## 格子ボルツマン法(LBM)

複雑形状の外部空力・空力音響に向いており、前処理が速いのが特長です。

- 🆓 [Palabos](https://gitlab.com/unigespc/palabos) - 並列格子ボルツマンソルバー。
- 🆓 [waLBerla](https://www.walberla.net) - 大規模並列LBMフレームワーク。
- 🆓 [OpenLB](https://www.openlb.net) - オープンソースのLBMライブラリ。
- 🆓 [Sailfish](https://github.com/sailfish-team/sailfish) - GPU向けLBM(現在は積極的に保守されていません)。
- 💼 [Dassault PowerFLOW](https://www.3ds.com/products/simulia/powerflow) - 自動車の空力・空力音響。
- 💼 [Simcenter XFlow](https://plm.sw.siemens.com/en-US/simcenter/fluids-thermal-simulation/xflow/) - LBMベースのCFD(シーメンス)。

## メッシュフリー固体力学(EFG / ペリダイナミクス / MPM)

破壊・亀裂の進展、土砂・粉体の流れ、極端な大変形に向いています。

- 🆓 [Peridigm](https://github.com/peridigm/peridigm) - ペリダイナミクスのコード(Sandia)。
- 🆓 [PeriPy](https://github.com/alan-turing-institute/PeriPy) - Python製ペリダイナミクス。
- 🆓 [Taichi MPM](https://github.com/yuanming-hu/taichi_mpm) - Taichi上の高性能MPM。
- 🆓 [Taichi](https://github.com/taichi-dev/taichi) - 多くのMPM / 粒子コードが使う並列プログラミング言語。
- 🆓 [Anura3D](https://www.anura3d.com) - 地盤工学向けMPM。
- 💼 [LS-DYNA (EFG)](https://www.ansys.com/products/structures/ansys-ls-dyna) - 大変形固体向けのElement-Free Galerkin法。

## ボクセル / イマーシブ境界法

CADから直接、設計初期の素早い評価を行う用途に向いています。

- 💼 [Altair Inspire](https://altair.com/inspire) - CAD形状から始めるシミュレーション駆動設計。
- 💼 [Ansys Discovery](https://www.ansys.com/products/3d-design/ansys-discovery) - 対話的なモデリングとリアルタイムシミュレーション。

## アイソジオメトリック解析(IGA)

CADのNURBS形状をそのまま使い、メッシュ化による幾何近似を排除します。

- 🆓 [igakit](https://github.com/dalcinl/igakit) - IGA用のPythonツールキット。
- 🆓 [GeoPDEs](https://github.com/rafavzqz/geopdes) - Octave / MATLAB用のIGAパッケージ。
- 🆓 [G+Smo](https://github.com/gismo/gismo) - C++製のIGAライブラリ。
- 💼 [LS-DYNA (IGA)](https://www.ansys.com/products/structures/ansys-ls-dyna) - アイソジオメトリック要素。

## AI / サロゲートモデル

学習後は瞬時に予測できます。教師データは、通常メッシュを使う従来のCAEで作成します。

- 🆓 [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) - 物理ML(機械学習)フレームワーク。
- 🆓 [neuraloperator](https://github.com/neuraloperator/neuraloperator) - Fourier Neural Operator などの実装。
- 🆓 [DeepXDE](https://github.com/lululxvi/deepxde) - 物理情報ニューラルネットワーク(PINN)。
- 💼 [Ansys SimAI](https://www.ansys.com/products/ai/simai) - クラウド型のAIサロゲート。
- 💼 [Altair physicsAI](https://altair.com/physicsai) - HyperWorks内のAIサロゲート。
- 💼 [Neural Concept](https://www.neuralconcept.com) - エンジニアリング向けディープラーニングプラットフォーム。

## 選び方の目安

| 用途 | 手法 |
|------|------|
| 大変形、自由表面、飛散 | SPH / MPS |
| 外部空力、空力音響 | LBM |
| 破壊、亀裂の進展 | ペリダイナミクス / EFG |
| 土砂、粉体、極端な大変形 | MPM |
| 設計初期の高速評価 | ボクセル / AIサロゲート |
| 規格対応が必須の構造強度 | 従来のFEM(現状は主流) |

## 注意点

- メッシュレスは前処理が楽ですが、境界条件の扱い、計算コスト(粒子数)、妥当性確認(validation)は課題として残ります。
- OSSの研究用コードの多くは、検証済み・規格対応の妥当性確認が弱く、実務の自動車CAEでは商用ツールが主流です。
- メンテナンスが止まったOSSもあります。採用前に最終コミットを確認してください。
- リンクは変わることがあります。リンク切れを見つけたら、PRでお知らせください。

## 関連リスト

CAE・シミュレーション全般のキュレーションリストです(メッシュレス手法に特化したものは見つかっていません)。

- [qd-cae/awesome-CAE](https://github.com/qd-cae/awesome-CAE) - CAEのフレームワーク・ライブラリ・ソフトウェア全般。
- [kimimgo/awesome-ai-cae](https://github.com/kimimgo/awesome-ai-cae) - AI対応のCAEツール(CFD、FEA、SPH、DEM、ニューラルオペレータ、PINN、MCPサーバー)。
- [anlijun/awesome-CAE-software](https://github.com/anlijun/awesome-CAE-software) - AIを含む、CAEワークフロー全体のソフトウェア。
- [shvyac/awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) - CAD / CAE 関連(同じメンテナー)。
- [tkoyama010/awesome-lattice-boltzmann-method](https://github.com/tkoyama010/awesome-lattice-boltzmann-method) - 格子ボルツマン法のリソース(説明文はまだありません)。
- [tkoyama010/awesome-open-source-cae](https://github.com/tkoyama010/awesome-open-source-cae) - オープンソースCAE(2023年から更新なし)。

## コントリビュート

PR(Pull Request)を歓迎します。1行1ツールで短い説明を付け、🆓 または 💼 を付けてください。詳細は [CONTRIBUTING.md](CONTRIBUTING.md)(英語)をご覧ください。

## ライセンス

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
