# Inspector.swf

## Usage

Please add `inspector.swf` to your project.

And add this swf to stage by `DisplayObjectContainer#addChild`.

### Use in Flex

```as3
class Sample extends UIComponent {
  [Embed(source="inspector.swf")]
  private static var Inspector:Class;

  public function Sample() {
    super();
    addChild(new Inspector);
  }
}
```

### Use in ActionScript3

```as3
var loader:Loader = new Loader;
loader.load(new URLRequest("inspector.swf"));
addChild(loader);
```

## Troubleshooting

Please try to add `-keep-all-type-selectors` to the compiler options, if you got an error like this: `Error: Skin for Inspector.VGroup.CheckBox cannot be found.`
