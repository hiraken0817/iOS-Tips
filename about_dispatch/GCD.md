# GCDまとめ

## GCDについて
GCDとはGrand Central Dispatchの略。
ディスパッチキューにタスクを詰めると、タスクを実行してくれる。

## キューのタススク処理について
キューのタスク処理の方法は2種類ある。

- Serial(直列)
- Concurrent(並列)

`Serial`は、前のタスクが完了次第、次のタスクが実行される。そのため、同時に実行されるタスクは1つ。
`Concurrent`は、前のタスクの処理状況に関わらず、次のタスクが実行される。

## キューの種類

- main Queue
  Serial(直列)
- Global Queue
Concurrent(並列)
- Private Queue
  Serial, Concurrent

このうち、Main QueueとGlobal Queueはシステムによってすでに作成されている。
Private Queueでは開発者が自由に設定したQueueを作成することができる。

## タスクの実行
タスクの実行をする際には同期か非同期かを指定します。

- sync(同期)
- async(非同期)
  
`sync`を使う場合には、呼び出し元のスレッドをブロックするため、デッドロックが発生することがあるので注意が必要です。

## Globalの優先度

Global Queueを使用する際には優先度を指定することができます。
以下が優先度の一覧で、上に位置するほど、優先度が高くなります。

- userInteractive
- userInitiated
- default
- utility
- background
- unspecified
