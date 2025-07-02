# 1UP しりとり

CPUと交互にしりとりを行うゲームです。  
特徴は「単語が1文字ずつ増えていく」ルールです。

---

## 概要

- ターンごとに単語が1文字ずつ長くなります  
- 例: `あ` → `あい` → `いかい` ・・・  
- 普通のしりとりにHP・制限時間を加えた**バトル形式しりとり**  
- 語尾が続いていない、文字数不足、時間切れでペナルティ  
- CPUと交互にバトルし、ハートが無くなった方が負け  

---

## DEMO

### スタート画面

![スタート](https://github.com/user-attachments/assets/9437da56-d2fc-4e25-b416-3475ec27cab5)  
難易度を選択して、シーンを移動します。

---

### ゲーム画面

![ゲーム中](https://github.com/user-attachments/assets/77671726-b7bc-4729-bb6c-a9ed5dd1a15a)  
シーン移動後、最初の語が出力され、しりとり開始。


## Features

✅ しりとり単語が1文字ずつ増加  
✅ 語尾ミス・字数不足・時間切れでペナルティ  
✅ CPUとHPバトル形式  
✅ タイムリミット搭載  
✅ 「戻るボタン」で簡単にホームへ戻れる  

---

## Requirement

Unity環境・以下の主要スクリプト構成：

```csharp
using System.Collections;
using UnityEngine;
using TMPro;
using UnityEngine.UIElements;
using System.Linq;
using System.Collections.Generic;
using UnityEngine.SceneManagement;

##Installation
Visual Studio を使用する場合は、必要なusingをスクリプト冒頭に記述してください。
Unity内で各スクリプトをGameObjectに紐付けることで動作します。

##Usage
スタート画面で難易度選択

シーン移動と同時に単語が表示

しりとりバトル開始

ターンごとに単語が1文字ずつ増加

ハートが無くなる、または時間切れで勝敗が決定

勝敗後、ボタンでホームに戻る


---

### 難易度選択

![難易度選択](https://github.com/user-attachments/assets/e8bb896c-0ce1-48a8-b912-1aa823b9b0bb)

---

### ターン例・進行

![しりとり中](https://github.com/user-attachments/assets/65865abb-751b-440d-ad2a-40c561d9fec2)  
CPUと交互に単語を出し合い、ターンが進む。

---

### ゲーム終了・戻るボタン

![ゲーム終了](https://github.com/user-attachments/assets/a0666f45-e215-49fb-bdbb-7f5970af534f)  
ゲームオーバーまたは勝利時に停止し、ボタンでホームに戻る。

---

Note
⚠ スコアアタック機能は未実装
⚠ 「ー」の後に濁音・半濁音が続く場合、処理が正しく動作しないことがあります
⚠ 現在、PC向けにローカル・WebGLでのビルドを想定しています

Author
川村 草生太

高知工業高等専門学校 4年 Iコース

d61049@gm.kochi-ct.jp
