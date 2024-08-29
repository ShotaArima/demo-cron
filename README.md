# demo-cron

このリポジトリはcronの学習として、自分でcronを設定してみてどのような動作をするのかを検証するものである

## 参考文献
- [【cron】Macでcronを設定してみた](https://qiita.com/suzu12/items/e12b3a8c6cbc3ea81720#%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE)

## cronの設定
1. cronの登録
    ```bash
      crontab -e
    ```
2. cronの内容
    ```bash
    # /usr/bin/php はｐｈｐコマンド
    # シェルスクリプトであれば sh になります。
    # ***のところで毎分実行の設定をしている
    
    * * * * * /usr/bin/php [上で作成したファイルのパス]/sample.php
    * * * * * /usr/bin/php [上で作成したファイルのパス]/sample.php `date '+\%Y\%m\%d\%H\%M\%S'`
    ```
3. 登録しているcronの確認
    ```bash
      crontab -l
    ```
4. logファイルの確認
    - `{pwd}/file/cron.log`
    - `{pwd}/file/error.log`
5. cronの削除
    ```bash
      crontab -r # 削除
      crontab -l # 確認
    ```
