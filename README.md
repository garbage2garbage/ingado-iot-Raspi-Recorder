Inga-Do Type IoT Raspi-Recorder

♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯  
♯  Inga-Do Type IoT ♯  
♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯♯  

　　　ヘヘヘ  
　＜（・∀・）＞  
　　　ＶＶＶ  
 Piyo-Piyo Fortress  


*説明  
ラズベリーパイにカメラユニットを取り付け、起動すると自動で録画してくれるレコーダーです  
インターネットに接続されている場合、録画ファイルに自動で録画日時をつけてくれます  
Gmailと連動して、録画開始や動作異常についてメール通知する機能も備えています  
Raspbian Stretchでこのレポジトリをクローンして、「00_initial_copy.sh」を実行すれば、すべての設定ファイルの配置が行われます。  

*動作要件  
 ハードウェア
  Raspberry PI Zero/Zero W およびカメラユニット  
  32GB以上のMicroSDカード  
 ソフトウェア  
  オフィシャルイメージのRaspbian Stretch  

*セットアップ方法  
Raspbian StretchをクリーンインストールしたRaspberry PIで、任意のディレクトリにこのレポジトリをクローンするか  
ZIPファイルでダウンロードして、/tmpなどに解凍してください。  
次に以下のコマンドを実行してください  

$ sudo chmod 755 ./00_initial_copy.sh  
$ sudo ./00_initial_copy.sh  

OS設定ファイルも含めて上書きしますので、他の用途に使用中のRaspberry PIではセットアップしないでください  

*使い方  
以下の資料を参照してください。これはコミケ95で頒布した際の資料です  
https://www.slideshare.net/IngaSakimori/c95raspberry-pi-zero-w  

基本的には起動するだけで勝手に録画が始まります  
初期設定では720p/3Mbpsで録画が行われます  
録画中はH264フォーマットで録画が行われ、数十分ごとにMP4ファイルへのコンバートプロセスが自動で走ります  

手動で録画ファイルを回収する場合は、/opt/ingado-iot-camera/rec にMP4が保存されています  
自動で転送する場合はボリュームラベルを「RASPI」（半角大文字）に設定した「FAT32」形式のUSBメモリを接続してください  
数十分ごとに自動転送プロセスが走ります。また起動開始時にも録画中ファイルをコンバートした上で、自動転送プロセスが走ります  
（「exFAT」にも対応していますが、「FAT32」がオススメです。なお、フォーマットはWindowsやMACのフォーマッターではなく、SD Associationよりフリーで配布されている「SD Card Formatter」でフォーマットしてください）  

*おまけ  
画質設定を変えたい場合は、デスクトップのリンクをクリックするか、/opt/ingado-iot-camera/commom.confを編集してください  
サンプル動画はこちら  
https://twitter.com/IngaSakimori/status/1076787382295261184  
開発模様はこちら  
https://togetter.com/li/1291301  
開発元のWebSiteはこちら（随時更新予定です）  
https://iot.inga-do.com/  

*ライセンス  
本ソフトウェアはすべて無保証です  
制作者が許可した場合を除き、商用利用を禁じます  
犯罪に使用することを禁じます  
普遍的自由を侵害し、第三者を抑圧する用途での利用を禁じます  

