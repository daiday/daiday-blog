在StackOverflow上看到的一个给frameless window添加阴影的解决方案。已经非常不错了。
需要注意的是，要给阴影足够的空间，不然显示有问题。

Draw Shadow In Frameless Window 
As of at least Qt 5.3 you don't need anything as elaborate as in the previous answers:

```cpp
Window {
    flags: Qt.Window | Qt.FramelessWindowHint | Qt.WA_TranslucentBackground
    color: "#00000000"
```

main.cpp: `QQuickWindow::setDefaultAlphaBuffer(true);`
