# glog #

It forked from [golang/glog](https://github.com/golang/glog).
Also added a quick and dirty modification to log a file.
golang/glog was for logging files by each severity levels.
This glog is going make a only one file to log.

## Usage ##

```go
import (
  "flag"

  "github.com/hyoyoung/glog"
)

func main() {
  flag.Parse()

  glog.Info("info log message")

  glog.Error("error log message")
}
```

```bash
$ ./your_program -log_dir=./log
```

## Flags List ##

| Flags            | default | Description                                                          |
|------------------|---------|----------------------------------------------------------------------|
| log_dir          |         | logging directory path                                               |
| logtostderr      | false   | log to standard error instead of files                               |
| alsologtostderr  | false   | log to standard error as well as files                               |
| v                |         | log level for V logs                                                 |
| stderrthreshold  |         | logs at or above this threshold go to stderr                         |
| vmodule          |         | comma-separated list of pattern=N settings for file-filtered logging |
| log_backtrace_at |         | when logging hits line file:N, emit a stack trace                    |
| afilelogging     | true    | log to a file                                                        |
