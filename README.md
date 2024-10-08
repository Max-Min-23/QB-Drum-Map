# QB Drum Map
Studio Oneのドラムマップ管理用エクセルブックです  
![QB Drum Map](https://github.com/user-attachments/assets/20decb0f-e7ad-4e76-84be-6145ede030c6)

### 〇　特徴
- エクセルによる編集機能が存分に使えるため、アプリケーション形式の場合よりも自由に編集が可能です。  

- アーティキュレーション指定により、すべてのドラムマップのピッチ名、並び順、（カラーリング、スコア表示（Studio Oneのみ））が統一できるので、音源を差し替えた場合でも同じ感覚で打ち込み作業をすることができます。

- QB Converterとの併用で、ネット上で配布されているドラムマップ(drm,pitchlist,txt形式)をStudio OneやCubaseで利用可能になります
  
- 各マクロ呼び出し用フォームから以下の機能を呼び出すことができます。  
  - Studio One用ピッチリスト（ドラムマップ）出力  
  - Cubaseドラムマップ変換用CSV出力 ※QB Converterと併用でCubaseのドラムマップ作製が可能です  
  - NoteMapper用テンプレート出力  
  - QB Drummer用テンプレート出力 ※現在、開発中のプラグイン用プリセットファイル出力  

- 以下のドラムマップが初期マップとして入っています
	- GM Custom  
	- Addictive Drums 2  
	- BFD3  
	- MODO DRUM  
	- SSD 5.5 StevenSlateDrums 5.5  
	- MT-Power Drum Kit 2  
	- GA Rock Kit Groove Agent 5  
	- GA Studio Kit Groove Agent 5  
	- GA Vintage Kit Groove Agent 5  
	- EZD3 Bright Room EZdrummer 3  
	- EZD3 Main Room EZdrummer 3  
	- EZD3 Tight Room EZdrummer 3  
	- EZX Jazz EZdrummer 3  
	- EZX Metal! EZdrummer 3  
	- SD3 CORE Superior Drummer 3  
	- SDX Stories - iso A Superior Drummer 3  
	- SDX Stories - iso B Superior Drummer 3  
	- SDX Stories - Main Superior Drummer 3  
	- SDX Hitmaker Superior Drummer 3  
	- StudioDrummer - StadiumKit KONTAKT  

### 〇　ダウンロード  
'QB Drum Map.zip'をクリック後、右側の'Down Load raw file'ボタンを押してダウンロードしてください。  
ダウンロードしたファイルを解凍後、ファイルのプロパティを開き、'セキュリティ'の許可をチェックしてください。

### 〇　使い方  
ショートカットキーCTRL+Eにマクロ呼び出しフォーム表示を割り当ててあります。 

#### 'Pitch Name'ラジオボタン  
- Original：音程名にマップシートの'Name'列が使用されます。
- Articulation：音程名にマップシートの'Articulation'列が使用されます。

#### 'Use Previouse Folder'チェックボックス  
- チェックあり：前回の保存先が記憶されている場合は保存先の選択ダイアログを表示しません。
- チェックなし：保存先の選択ダイアログが毎回表示されます。

#### 1. Studio One用ピッチリスト出力の場合  
'Drum Map'一覧より処理対象を選択し'Go'ボタンを押下します。  

#### 2. Cubaseドラムマップ変換用CSV出力の場合  
'Convert Base'コンボボックスより入力ピッチで使用するマップを選択します。  
'Drum Map'一覧より処理対象を選択し'Exp. CSV'ボタンを押下します。  
※出力されたCSVファイルはQB ConverterでCubase用のドラムマップに変換できます。

#### 3. NoteMapper用テンプレート出力  
'Convert Base'コンボボックスより入力ピッチで使用するマップを選択します。  
'Drum Map'一覧より処理対象を選択し'Exp. NoteMapper'ボタンを押下します。  

#### 4. QB Converter用プリセットファイル出力　※開発中プラグイン  
'Convert Base'コンボボックスより入力ピッチで使用するマップを選択します。  
'Drum Map'一覧より処理対象を選択し'Exp. QB Drummer'ボタンを押下します。  

#### その他のボタン
- System Sheets Visible：システムシートを表示します
- System Sheets Hide：システムシートを非表示にします
- Fix Articulation：マップシートArticulation列の入力規則を修復します

### 〇　マップ定義シート  
新規にマップを作製する場合は、'_template'シートをコピーし名前を変更してください。
- 'Name'列が空白以外の場合出力対象となります。
- 'Articulation'列を指定することで'_Articulation'シートで定義された規則が適用されます。空白の場合、DAWのドラムマップ表示順が下部に移動されます。

#### 'Alias'列の機能は以下の通り  
'Alias'列の文字を指定することで出力される順序を操作することができます。

文字 | 内容
--- | --- 
＊ | 別の音程に同じアーティキュレーションが割当たっている場合、表示を分離したい場合に指定します
＋ | マップ定義はされているが、音源にアーティキュレーションがロードされていないものに指定します（Toon Track社などの音源用）
－ | マップ定義はされているが、使用頻度が少なく、表示を分離したい場合に指定します

#### 'Dup'列  
なにがしかの出力操作を行った場合にチェックが入ります。  
DAW表示した場合に同一アーティキュレーションが並んで表示されてしまうのを防ぐためのチェックです。  
※気にならない方は放置で結構です  
マップ定義シートで同一アーティキュレーションが存在している場合に'＊'がセットされます。
同一アーティキュレーションを持つ不要な行の'Alias'列に'＊'を指定することで表示順を分離することができます。

### 〇　システムシート
システムで使用するシートは、シート名が'＿'アンダースコアで始まります。
よって、マップ定義用シート名の先頭には'＿'アンダースコアを使用しないでください。

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

