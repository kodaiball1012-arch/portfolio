## 1. Machine Learning: 生体信号解析とSVMを用いた要除細動波形識別システム
複雑な時系列データ（ECG波形）から特徴量を抽出し、機械学習を用いてショック適応波形（VF：心室細動）と非適応波形（PEA：無脈性電気活動）を高精度に識別・分類するアルゴリズムをMATLABで実装しました。

Language & Tools: MATLAB, Python

Algorithms: Continuous Wavelet Transform (CWT), Support Vector Machine (SVM), Recursive Feature Elimination (SVM-RFE), ANOVA

Implementation Details:

特徴量抽出: ノイズの多い生体信号に対し、連続ウェーブレット変換（CWT）および擬似微分作用素（PDO）を用いて時間・周波数領域の特徴量を抽出。

特徴量選択（フィルター法 vs ラッパー法）: 計算コストの低いフィルター法（Python: ANOVA）での初期スクリーニングに加え、予測精度に直結するラッパー法（MATLAB: SVM-RFE）を実装し、最適な特徴量サブセットを探索。

厳密なモデル評価: 過学習を防ぎ、未知のデータに対する汎化性能を正しく評価するため、Nested Cross-Validation（入れ子型交差検証）を独自に実装。

Achievement:
本実装および検証結果に基づき、学部4年次の卒業論文発表にて優秀賞を受賞。また、本研究内容をシステム制御情報学会（SCI）にて論文として提出。
