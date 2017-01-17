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

## Key Bindings

- `Shift+Click`: Inspect a DisplayObject under the cursor.
- `Tab`: Inspect the parent of the current target.
- `Esc`: Stop the inspection.
- `F12`: Toggle Inspector.

## Troubleshooting

Please try to add `-keep-all-type-selectors` to the compiler options, if you got an error like this: `Error: Skin for Inspector.VGroup.CheckBox cannot be found.`
