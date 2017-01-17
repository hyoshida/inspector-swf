# Inspector.swf

## インストール

Flash Builder の対象プロジェクトに [inspector.swf](bin-release/inspector.swf) を追加してください。

あとはこの swf を `DisplayObjectContainer#addChild` メソッドで stage に追加するだけです。

### 導入例

```as3
class Main extends Sprite {
  [Embed(source="inspector.swf")]
  private static var Inspector:Class;

  public function Main() {
    addChild(new Inspector);
  }
}
```

または

```as3
var loader:Loader = new Loader;
loader.load(new URLRequest("inspector.swf"));
addChild(loader);
```

## キーバインド

- `Shift+Click`: マウス下にある表示オブジェクトを検証する。
- `Tab`: 検証対象を現在の表示オブジェクトの親に変更する。
- `Esc`: 検証をキャンセルする。
- `F12`: インスペクターの表示/非表示を切り替える。

## トラブルシューティング

Q: `Error: Inspector.VGroup.CheckBox のスキンが見つかりません。` というエラーが出ます。

A: コンパイルオプションに `-keep-all-type-selectors` を付け足して再コンパイルしてみてください。
