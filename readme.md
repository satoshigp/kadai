# **Tamasan**

## -**概要**-
- 単純操作でやりやすい  
- 夏休み前の授業で行ったyoketoruに似てるように制作  
  違いは平面か立体化の違い

- aseetは今回は使用してないです...
---
## -**操作方法**-  
矢印キーで前後左右の動き  
なんとなく緊急回避用としてspaceキーを入力してジャンプ
---

## -**ゲームルール**-  
アイテムをすべて回収でクリア
敵に当たったらゲームオーバー
※コースアウトでゲームオーバージャンプ連打で起こってしまう
---
## 制作期間  
企画発案を含め4日ほど
## -**自分で開発を行った箇所**-
基本はyoketoruのスクリプトを参考に開発

  もう一つは[github](https://github.com/unity3d-jp/FirstTutorial/wiki "チュートリアルサイト")を参照して進めていった  
そして自分で行った制作箇所はサイトはなかった敵の出現や状態遷移  
---  
## -**苦労したところ**-  
1. どのオブジェクトにスクリプトを持たせるか？
1. 英語が読めないからエラーが怖くなった...  
1. 当たり判定  
---  
## スクリプト  
```
 void FixedUpdate()
    {
        if (transform.position.y < 0)
        {
            GameManager.NextScene = "GameOver";
        }
      

        //キー入力。

        float x = Input.GetAxis("Horizontal");
        float z = Input.GetAxis("Vertical");
        float y = Input.GetAxis("Jump");
        Rigidbody rigidbody = GetComponent<Rigidbody>();

        rigidbody.AddForce(x * speed, y*Jump, z * speed);
        

    }
```
## -**反省点**-  

       1. Playerの操作感の悪さ
       1. BGMがよくわからんことになった
       1. ジャンプ連打しまくるとステージ外へ出てしまう
       1. 敵のスポーンを理解できてなかったので敵出現位置固定となってしまった
       1. 敵の出現位置のランダム化ができなかった
---

## -**次回目標**-
極力自分の力で制作をする。  
aseetを使用、自分でキャラを用意してさらに質の良い作品を制作する  
