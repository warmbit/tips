# Tips 

## How to git sync fork with original repo

For example, https://github.com/warmbit/excalidraw is forked from https://github.com/excalidraw/excalidraw. Need to make sure that my local is updated with the original.

### 1. check if there is any remote repo configured 
Skip this step if it is configured.

```
$ git remote -v
origin	https://github.com/warmbit/excalidraw (fetch)
origin	https://github.com/warmbit/excalidraw (push)
```

### 2. add the original repo as an upstream repo

```
$ git remote add upstream https://github.com/excalidraw/excalidraw.git
```

### 3. check again

```
$ git remote -v
origin	https://github.com/warmbit/excalidraw (fetch)
origin	https://github.com/warmbit/excalidraw (push)
upstream	https://github.com/excalidraw/excalidraw.git (fetch)
upstream	https://github.com/excalidraw/excalidraw.git (push)
```

Now both origin and upstream are configured.

### 4. merge original repo into your fork

```
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
$ git push origin master
```


