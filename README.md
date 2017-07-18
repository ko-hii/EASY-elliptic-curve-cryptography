# EASY-elliptic-curve-cryptography  

### 簡単な楕円曲線暗号を用いた鍵交換と総当たり攻撃による解読  
main.py()が実行ファイル。  
Python3で、sympyをインストールしないと動きません。  

### 流れ  
１．法にする素数を決める(mod = p^r？、r=1で考える)  
２．楕円曲線のパラメータをmodの範囲でランダムに決定する(コメントアウトを消して位数が素数になるまで繰り返してもいいが、素数が大きければやめたほうがいい)  
３．楕円曲線暗号を用いてアリスとボブが共通鍵(厳密に言うと座標)を交換する  
４．第三者が盗聴可能な情報から、総当たり攻撃でアリスとボブが秘密裏に交換した共通鍵を解読する  

※大したアルゴリズムは使っていないので、素数は数桁じゃないと時間がかかる  
※4桁なら位数が素数になるまでパラメータを選び直しても、数十秒で終わる  
※6桁になると鍵交換までならすぐに終わるが、解読に下手したら2時間くらいかかる  
