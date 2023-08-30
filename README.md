# cython_bbox

cython_bbox is widely used in object detection tasks. To my best knowledge, it was first implemented in [Faster-RCNN](https://github.com/rbgirshick/py-faster-rcnn). Since then, almost all object detection projects use the source code directly.

In order to use it in standalone code snippets or small projects, I make it a pypi module. The `cython_bbox.pyx` is totally borrowed from [Faster-RCNN](https://github.com/rbgirshick/py-faster-rcnn). Thanks [RBG](http://www.rossgirshick.info/)!

## install

```
pip install cython_bbox
```

## usage


```
from cython_bbox import bbox_overlaps
overlaps = bbox_overlaps(
        np.ascontiguousarray(dt, dtype=np.float32),
        np.ascontiguousarray(gt, dtype=np.float32)
    )

```

## Custom fork (jcruz-ferreyra)

I downloaded tar.gz file from PyPI and did the modifications for windows support decribed here:
https://stackoverflow.com/questions/60349980/is-there-a-way-to-install-cython-bbox-for-windows

I also change line 12 in `src/cython_bbox.pyx`. As "np.float" was deprecated I need to change it to just "float".
