## JUPYTER-BAZEL ##

This is simple example of how to create and launch a jupyter notebook binary that includes local bazel libraries.

Simply execute:

```
bazel run notebooks:jupyter
```

and the binary will built and executed. The browser will start and you can create a notebook as normal. Anything in the notebooks/BUILD deps will be available.

However you probably want to store your notebooks in a directory under your workspace rather then the bazel out directory created and used by ``bazel run``. The solution to this problem is to build the binary and then execute it directly.
```
bazel build notebooks:jupyter
bazel-bin/notebooks/jupyter
```
You when execute the binary this way you will see the example.ipynb included in this repo.
