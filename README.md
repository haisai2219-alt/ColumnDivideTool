# CSVをカラムの値ごとにファイル分割して出力するツール

CSVファイルを、指定したカラムの値ごとに自動で分割するWindowsツールです。

## 動作環境

- Windows 10 / 11
- Java 11 以上（[ダウンロードはこちら](https://adoptium.net/)）

## インストール

ZIPをダウンロードして、任意のフォルダに解凍するだけです。インストール作業は不要です。

## 使い方

1. `input/` フォルダに分割したいCSVファイルを置く
2. `config.txt` を開いて `targetColumnName` に分割基準のカラム名を書く
3. `columnDivide.bat` をダブルクリックして実行
4. `output/` フォルダに結果が出力される

## 設定項目（config.txt）

| 項目               | 説明
| targetColumnName   | 分割基準のカラム名（必須）
| maxRecordsPerFile  | 1ファイルの最大行数（空欄で無制限） 
| exactMatchValue    | 完全一致フィルタ（空欄で無効）
| partialMatchValue  | 部分一致フィルタ（空欄で無効）
| includeHeader      | ヘッダー行を出力するか   
| originalName       | 出力ファイル名に元ファイル名を付けるか

## 注意事項

- 実行のたびに `output/` フォルダの中身は全削除されます
- 入力CSVはUTF-8形式のみ対応しています
- カラム名は大文字・小文字を区別します
- カラム値が空のレコードは `00__EMPTY.csv` に出力されます

<img width="1707" height="621" alt="image" src="https://github.com/user-attachments/assets/fa42e875-cb2d-44d0-9b02-50f8543fd385" />
