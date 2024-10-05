# QB Drum Map
Studio Oneのドラムマップ管理用エクセルブックです  

### 特徴
・エクセルによる編集機能が存分に使えるため、アプリケーション形式の場合よりも自由に編集が可能です。  
  
・各マクロ呼び出し用フォームから以下の機能を呼び出すことができます。  
1.Studio One用ピッチリスト（ドラムマップ）出力  
2.Cubaseドラムマップ変換用CSV出力 ※QB Converterと併用でCubaseのドラムマップ作製が可能です  
3.NoteMapper用テンプレート出力  
4.QB Drummer用テンプレート出力 ※現在、開発中のプラグイン用プリセットファイル出力  

### インストール  

### 使い方  
ショートカットキーCTRL+Eにマクロ呼び出しフォーム表示を割り当ててあります。  

1.Studio One用ピッチリスト出力の場合  
'Drum Map'一覧より処理対象を選択し'Go'ボタンを押下します。  

2.Cubaseドラムマップ変換用CSV出力の場合  
'Drum Map'一覧より処理対象を選択し'Exp. CSV'ボタンを押下します。  

3.NoteMapper用テンプレート出力  
'Convert Base'コンボボックスより入力ピッチで使用するマップを選択します。  
'Drum Map'一覧より処理対象を選択し'Exp. NoteMapper'ボタンを押下します。  

4.NoteMapper用テンプレート出力  
'Convert Base'コンボボックスより入力ピッチで使用するマップを選択します。  
'Drum Map'一覧より処理対象を選択し'Exp. QB Drummer'ボタンを押下します。  

### システムシート
システムで使用するシートは、シート名が'_'アンダースコアで始まります。
よって、マップ定義用シート名の先頭には'_'アンダースコアを使用しないでください。

シート名 | 内容
--- | --- 
_Keyboard | 
_Pitch | 音程番号と音程名の対応データ（ヤマハ式）
_NoteHead | スコアビューの符頭表示データ
_Techniq | スコアビューのテクニック表示データ
_Kit | ドラムキットのカテゴリ分類データ
_Kit Piece | ドラムキットのキットピースデータ
_Articulation | キットピースのアーティキュレーションデータ
_work | 各種テキストファイル編集一時ワーク
_ArticulationMap | 各種テキストファイル編集一時ワーク
_template | 新規マップ作製用テンプレートシート

