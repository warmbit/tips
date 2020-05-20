# Tips 

## git sync fork with original repo

For example, https://github.com/warmbit/excalidraw is forked from https://github.com/excalidraw/excalidraw.

### check if there is any remote repo configured

```
$ git remote -v
origin	https://github.com/warmbit/excalidraw (fetch)
origin	https://github.com/warmbit/excalidraw (push)
```

### add the original repo as an upstream repo

```
$ git remote add upstream https://github.com/excalidraw/excalidraw.git
```

### check again

```
$ git remote -v
origin	https://github.com/warmbit/excalidraw (fetch)
origin	https://github.com/warmbit/excalidraw (push)
upstream	https://github.com/excalidraw/excalidraw.git (fetch)
upstream	https://github.com/excalidraw/excalidraw.git (push)
```

Now both origin and upstream are configured.

### merge original repo into your fork

```
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
$ git push origin master
```



