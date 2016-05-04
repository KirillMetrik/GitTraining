# Reviewing the repository history
```
> git log --oneline
6cfa070 Removal of console application
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
0f412a0 First commit and comment for it
```
```
> git log --oneline my_apple_app
5a1710a OS X version
6cfa070 Removal of console application
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
0f412a0 First commit and comment for it
```
```
> git log --oneline MyWindowsApp/code.txt
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
```

Or even a folder
```
> git log --oneline MyWindowsApp
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
```
```
> git mv MyWindowsApp/code.txt MyWindowsApp/dll.txt
> git commit -m "moved code into dll"
[master eeab96e] moved code into dll
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename MyWindowsApp/{code.txt => dll.txt} (100%)
```

See the history:

```
> git log --follow --oneline MyWindowsApp/dll.txt
eeab96e moved code into dll
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
```
```
> git log --follow --oneline -- MyConsoleApp/console.txt
6cfa070 Removal of console application
c72c6d6 My first lab commit 2
b76b4f2 My first lab commit 1
```
```
> git log --follow --name-status --oneline MyWindowsApp/dll.txt
e2385cf main in dll
M       MyWindowsApp/dll.txt
eeab96e moved code into dll
R100    MyWindowsApp/code.txt   MyWindowsApp/dll.txt
c72c6d6 My first lab commit 2
M       MyWindowsApp/code.txt
b76b4f2 My first lab commit 1
A       MyWindowsApp/code.txt
```
```
> git log --follow -p MyWindowsApp/dll.txt
commit eeab96ec34708b47a7567cf78059b25b4edb45a6
Author: Wolf <wolf@wolfsden.cz>
Date:   Wed Mar 30 16:21:43 2016 +0200

    moved code into dll
diff --git a/MyWindowsApp/code.txt b/MyWindowsApp/dll.txt
similarity index 100%
rename from MyWindowsApp/code.txt
rename to MyWindowsApp/dll.txt
commit c72c6d6f4ea5ac79185fc6767426adcf5e1a3700
Author: Wolf <wolf@wolfsden.cz>
Date:   Wed Mar 30 16:03:31 2016 +0200
    My first lab commit 2
diff --git a/MyWindowsApp/code.txt b/MyWindowsApp/code.txt
index e69de29..fc8502f 100644
--- a/MyWindowsApp/code.txt
+++ b/MyWindowsApp/code.txt
@@ -0,0 +1 @@
+Added during git workshop
commit b76b4f226b94066ece47233222a9755e3902c999
Author: Wolf <wolf@wolfsden.cz>
Date:   Wed Mar 30 16:02:47 2016 +0200
    My first lab commit 1
diff --git a/MyWindowsApp/code.txt b/MyWindowsApp/code.txt
new file mode 100644
index 0000000..e69de29
```
## More information