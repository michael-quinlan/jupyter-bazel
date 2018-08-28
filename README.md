## JUPYER-BAZEL ##

This is simple example of how to create and launch a jupyter notebook binary that includes local bazel libraries.

Simply execute:

```
bazel run notebooks:jupyter
```

and the binary will built and executed. The browser will start and you can create a notebook as normal. Anything in the notebooks/BUILD deps will be available.

In this case in cell 1 add:
```
from foo.bar import baz
baz()
```
