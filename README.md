***************************
  IPython Magic Functions
***************************

# Installation

Install:
```python
%install_ext https://raw.githubusercontent.com/bornio/ipython-magic/master/gvmagic.py
%load_ext gvmagic
```

* Graphviz Magics (`gvmagic.py`):
  `%dot`, `%dotstr`, `%dotobj`, `%dotobjs`

## Usage

* `%dot` - line/cell magic converts raw input to Graphviz `dot` SVG output.
* `%dotstr` - line magic converts string input to Graphviz `dot` SVG output.
* `%dotobj` - line magic converts object with `to_dot` method to Graphviz `dot` SVG output.
* `%dotobjs` - line magic converts sequence of objects with `to_dot` method to Graphviz `dot` SVG output.

Examples:

```python
%dot digraph G { a -> b; a -> c }

%%dot digraph G {
  a -> b;
  b -> c;
}

%dotstr "digraph G { a -> b; a -> c }"

%dotobj dotobj.to_dot()

%dotobjs dotojb[0].to_dot(), dotobj[1].to_dot(), ...
```
