# CollectionViewについて
### CollectionViewを構成する3要素
- Layout
- Datasource
- Delegate
  
#### UICollectionViewLayout
コンテンツの配置を示す。
UICollectionViewFlowLayoutはこれのサブクラス。

#### UICollectionViewDataSource
CollectionViewの内容を提供。
セクションやアイテムの数なども管理。

#### UICollectionViewDelegate
オプショナルなプロトコル。
CollectionViewに対するユーザのアクションに対応。
