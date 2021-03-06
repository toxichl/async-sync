# async-sync

A gulp-based nodejs test project about performance comparison of sync(serial) and async(parallel) 

<br>

> 中文README请移步: [中文文档](README_zh.md)

<br>


## Description

There are altogether 2000 documents, each file has 100 lines, a total of `20w` line, and each line needs to be modified.

`Async` uses `promise.all()` to modify all files in parallel, ending with the ending of the last file modification;

`Sync` using the `ES6 Generator` control synchronization, file serial modification, each reading and writing of a file  will wait for the previous file to read and write the end

Time consuming results are tested as follows:


### Async

<img style="width: 50%" src="result/async-01.png" alt="">
<img style="width: 50%" src="result/async-02.png" alt="">


### Sync
<img style="width: 50%" src="result/sync-01.png" alt="">
<img style="width: 50%" src="result/sync-02.png" alt="">

- This gap is too big now !!!!
- This gap is too big now !!!!
- This gap is too big now !!!!


## local test

Can clone this item on your local machine for testing:

```
$ Git clone https://github.com/toxichl/async-sync.git
```
Installation Dependencies:

```
$ mpm i
```

> Note: This test is based on Gulp, you can consider the global installation of Gulp.

Initialize, if there is an old test files, delete them, and then generate the new test file:

```
$ gulp init
```

Asynchronous (parallel) test:

```
$ gulp async
```

Synchronous (serial) test:

```
$ Gulp sync
```

Remove old test files:

```
$ Gulp del
```


## Conclusion

In some cases where `parallel control` is allowed, use `parallelism` as much as possible to improve program performance.



