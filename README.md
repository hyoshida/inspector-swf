# Inspector.swf

## Installation

Please add [inspector.swf](bin-release/inspector.swf) to your project.

And add this swf to stage by `DisplayObjectContainer#addChild`.

## Usage

```as3
class Main extends Sprite {
  [Embed(source="inspector.swf")]
  private static var Inspector:Class;

  public function Main() {
    addChild(new Inspector);
  }
}
```

or

```as3
var loader:Loader = new Loader;
loader.load(new URLRequest("inspector.swf"));
addChild(loader);
```

## Troubleshooting

Please try to add `-keep-all-type-selectors` to the compiler options, if you got an error like this: `Error: Skin for Inspector.VGroup.CheckBox cannot be found.`
