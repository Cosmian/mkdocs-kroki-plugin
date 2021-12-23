# mkdocs-kroki-plugin

This is a MkDocs plugin to embed Kroki-Diagrams into your documentation.

> ⚠️ This is a modified fork
The main difference from the original repo is that it removes the `kroki-`prefix in the makdown.

## Setup

Install the plugin using pip:

`pip install git+https://github.com/Cosmian/mkdocs-kroki-plugin.git`

Activate the plugin in `mkdocs.yml`:

```yaml
plugins:
  ...
  - kroki:
```

## Config

* `ServerURL` - URL of your kroki-Server, default: <https://kroki.io>
* `EnableBlockDiag` - Enable BlockDiag (and the related Diagrams), default: True
* `Enablebpmn` - Enable BPMN, default: True
* `EnableExcalidraw` - Enable Excalidraw, default: True
* `EnableMermaid` - Enable Mermaid, default: True
* `DownloadImages` - Download diagrams from kroki as static assets instead of just creating kroki links, default: False
* `DownloadDir` - The asset directory to place downloaded svg images in, default: images/kroki_generated

## Usage

Example for BlockDiag:

````markdown
```blockdiag
blockdiag {
  blockdiag -> generates -> "block-diagrams";
  blockdiag -> is -> "very easy!";

  blockdiag [color = "greenyellow"];
  "block-diagrams" [color = "pink"];
  "very easy!" [color = "orange"];
}
```
````

## See Also

Diagram examples can be found [here](https://kroki.io/examples.html).

More information about installing a self-manged Kroki-Service [here](https://docs.kroki.io/kroki/setup/install/).

More Plugins for MkDocs can be found [here](http://www.mkdocs.org/user-guide/plugins/)

## Pre-Release-Versions

Install the newest pre-release version using pip:

`pip install -i https://test.pypi.org/simple/ mkdocs-kroki-plugin`
