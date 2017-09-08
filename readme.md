# **Tamasan**

## -**概要**-
- 夏休み前の授業で行ったyoketoruに似てるように制作  
  違いは平面か立体化の違い
- aseetは今回は使用してないです...
---
## -**ゲームルール**-  

移動は矢印キーで行う
なんとなく緊急回避用としてspaceキーを入力してジャンプ
敵に当たったらゲームオーバー
---
## 制作期間  
企画発案を含め4日ほど
## -**自分で開発を行った箇所**-
基本はyoketoruのスクリプトを参考に開発

  もう一つは[github](https://github.com/unity3d-jp/FirstTutorial/wiki "チュートリアルサイト")を参照して進めていった

そして自分で行った制作箇所はサイトはなかった敵の出現などであるや状態遷移
---
##　-**苦労したところ**-  
1. どのオブジェクトにスクリプトを持たせるか？
1. 英語が読めないからエラーが怖くなった...
---
#＃ -**スクリプト**-

移動やジャンプ
```C
//物理演算機能を使用する際はFixedUpdateのほうがいいらしい
void FixedUpdate()
   {
     //キー入力
       float x = Input.GetAxis("Horizontal");
       float z = Input.GetAxis("Vertical");
       float y = Input.GetAxis("Jump");
       //物理演算機能を追加
       Rigidbody rigidbody = GetComponent<Rigidbody>();
　　　　//速度設定とか
       rigidbody.AddForce(x * speed, y*Jump, z * speed);

   }
   ```
#＃ -**反省点**-
   - 反省点としては
       1. Playerの操作感の悪さ
       1. BGMがよくわからんことになった
       1. ジャンプ連打しまくるとステージ外へ出てしまう
       1. 敵のスポーンを理解できてなかったので敵出現位置固定となってしまった
---

#＃ -**次回目標**-
極力自分の力で制作をする。  
aseetを使用、自分でキャラを用意してさらに質の良い作品を制作する  
