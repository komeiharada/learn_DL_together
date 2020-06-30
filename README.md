# learn_DL_together 個人ノート

JTPA みんなでやろうDL オンライン勉強会 https://github.com/JTPA/learn_DL_together

Nocnoc: https://nocnoc.ooo/app#/chat/A1B6CDAC-637F-4455-9582-D086AC289268

何か自分でまとめないと学習しないのでGithubに載せてみました。まだ初心者の練習レベルなのでこのページ自体はシェアはしないで下さい。（以下に引用したリンクはご自由にシェアして下さい。）

## オーディオ認識

もともと画像認識の方が興味があるのですが、写真技術のチュートリアルビデオ（MLとは関係なし）を見ていたら、シャッターの音がする度に講師が撮影した写真が画面に出るというビデオがあって、シャッター音を認識して画像フレームをセーブできないかというところからオーディオ認識の勉強を始めました。シャッター音のタイムスタンプがわかれば、そこの画像フレームをビデオから抽出するのは簡単です。

音声のスペクトル ([MFCC](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum)) を取って画像のようにCNNをかければいいみたいです。以下のサイトはスピーチ音声等の認識ですが、シャッター音検出のために他にもっと良い方法があれば教えて下さい。

### 見つけたサイト

* https://medium.com/manash-en-blog/building-a-dead-simple-word-recognition-engine-using-convnet-in-keras-25e72c19c12b
**Building a Dead Simple Speech Recognition Engine using ConvNet in Keras** by Manash Kumar Mandal
  * Code: https://github.com/manashmandal/DeadSimpleSpeechRecognizer

Colabに持ってきて実行
https://colab.research.google.com/drive/1WEFVUwM76hgqMMvHFDU_73hlWjQP3RQG?usp=sharing

* https://medium.com/@mikesmales/sound-classification-using-deep-learning-8bc2aa1990b7
**Sound Classification using Deep Learning** by Mike Smales

  * Code: https://github.com/mikesmales/Udacity-ML-Capstone
  今のところエラーが起きてうまく動かない（詳細後日）

## 画像認識

* https://colab.research.google.com/github/google/automl/blob/master/efficientdet/tutorial.ipynb#scrollTo=V8-yl-s-WKMG
**EfficientDet Tutorial: inference, eval, and training**
(https://github.com/JTPA/learn_DL_together のREADME.mdの中にリンクあり）
My copy: https://colab.research.google.com/drive/1O9zETdRbCL-HlfwHtSrRl7QotiBqMPI-#scrollTo=fHU46tfckaZo

inference.pyの最後の関数inferenceに犬とかバイク・車の絵をモデルに喰わせると、Bounding Boxやラベルの配列を返してくれる模様。
