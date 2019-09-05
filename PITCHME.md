# Space Shooting

---

#### 作品について
岩を如何に多く撃ち壊してスコアを取れるか


---

#### 操作方法
矢印左右キー(←→)で移動  
スペースキーで発射
   
####開発環境
Unity2019 1.5f
Web GL
960x600pixel
    
#### ルール
岩を壊してどれくらいスコアを稼げるか

---

オリジナル要素
- シーン追加
- 岩生成の変更
+++
```cs
public class RockGenerator : MonoBehaviour
{
    public GameObject rockPrefab;
    float count,time;
    void GenRock()
    {
        Instantiate(rockPrefab, new Vector3(-2.5f + 5 * Random.value, 6, 0), Quaternion.identity);
    }
    private void FixedUpdate()
    {
        count -= Time.fixedDeltaTime;
        if(count<0)
        {
            GenRock();
            time = time-0.01f;
            count = time;
        }
    }
}
```
---

#### 参考元
[【Unity入門】60分で作るシューティングゲーム](http://nn-hokuson.hatenablog.com/entry/2016/07/04/213231)   
[甘茶](https://amachamusic.chagasi.com)


#### 自分で加えた箇所
- タイトルシーン
- ゲームオーバーシーン

---

#### お借りした物・利用したアセット
- SampleShooting_Material
- Explosive Toon VFX Texture Free
- BGM   
[夏の霧](https://amachamusic.chagasi.com/music_natsunokiri.html)   
[夏休みの探検](https://amachamusic.chagasi.com/music_natsuyasuminotanken.html)
---
     以上です。    
ありがとうございました。
