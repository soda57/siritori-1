# 1UP しりとり

CPUと交互にしりとりを行うバトル形式のゲームです。  
特徴は「単語が1文字ずつ増えていく」独自ルールを採用しています。

![Unity](https://img.shields.io/badge/Unity-2022.3%20LTS-blue)  
![Platform](https://img.shields.io/badge/Platform-PC%20%7C%20WebGL-green)  

---

## 概要

- ターンごとに単語が1文字ずつ長くなります  
  例: `あ` → `あい` → `いかい` → ...  
- 普通のしりとりに **HP・制限時間** を加えた「バトル形式しりとり」  
- 語尾が続いていない、文字数不足、時間切れでペナルティ発生  
- CPUと交互に単語を出し合い、ハート（HP）が無くなった方が負け  

ゲーム公開ページ: [Unityroom - 1UPしりとり](https://unityroom.com/games/1up_shiritori)

---

## DEMO

### スタート画面
![スタート画面](https://github.com/user-attachments/assets/5128d9a3-598c-47b7-9529-b2a959b3947e)

難易度を選択してゲーム開始。

---

### ゲーム画面
![ゲーム中](https://github.com/user-attachments/assets/84ccc5b9-eb90-402e-96f2-8673c0703301)

シーン移動後、最初の単語が表示されしりとりスタート。

---

### ターン例・進行
![しりとり中](https://github.com/user-attachments/assets/ecbb3d51-ee29-451b-ba27-97fb142eafa7)
)

CPUと交互に単語を出し合い、ターンごとに単語が1文字ずつ増加。

---

### ゲーム終了・戻るボタン
![ゲーム終了](https://github.com/user-attachments/assets/5f22c8f3-f078-4f10-9794-85c2ec99c00b)

勝敗が決まると停止し、ホームに戻るボタンが表示。

---

## Features

✅ 単語がターンごとに1文字ずつ増加  
✅ 語尾ミス・文字数不足・時間切れでペナルティ  
✅ CPUとの HP バトル形式  
✅ 制限時間ありの緊張感  
✅ 「戻るボタン」で簡単にホームに戻れる  

---

## Requirement

- Unity (2022.3 LTS 推奨)  
- Visual Studio（推奨）  

---

## Installation

- スクリプトの冒頭に必要な `using` を記述してください  
- Unity内で各スクリプトを GameObject にアタッチしてください  
- 現在、PC 向け・WebGL ビルドを想定しています  

---

## Usage

1. スタート画面で難易度を選択  
2. シーン移動と同時に単語が表示され、しりとりバトル開始  
3. ターンごとに単語が1文字ずつ増加  
4. 語尾ミス・時間切れ・HP 0で敗北  
5. 勝敗後、ボタンでホームに戻る  

---

## Note

⚠ スコアアタック機能は現在未実装です  
⚠ 「ー」の後に濁音・半濁音が続く場合、しりとり判定処理が正しく動作しない場合があります  
⚠ PC 向けローカル実行・WebGL ビルドを推奨  

---

## Author

川村 草生太  
高知工業高等専門学校 4年 I コース  

📧 d61049@gm.kochi-ct.jp  
💻 GitHub 活用を意識しています  

---

## 補足

本プロジェクトのコード制作では、ChatGPT を活用し、  
主に以下のような手順で開発を進めました。

- 関数・要件のリストアップ  
- 実際のコードの提案・修正依頼  
- Unity 実装例の確認と微調整  

