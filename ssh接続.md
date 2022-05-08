# WSLへの接続
* ipアドレスの確認(On WSL)
  ip a show dev eth0
* port22 の開放(セキュリティ考慮なし)
  * /etc/ssh/sshd_configの編集
    * 22ポートの開放<br>
      「# Port 22」→「Port 22」    コメントをはずす
    * パスワード認証の設定<br>
      「PasswordAuthentication no」→「PasswordAuthentication yes」
    * sshサービスの起動<br>
      「sudo service ssh start」
    * 確認<br>
      「ssh XXXX@localhost
* 鍵認証
  * ~/.ssh/authorized_keys に公開鍵を置く
  
