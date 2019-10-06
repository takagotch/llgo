### llgo
---
https://github.com/go-llvm/llgo

```sh
// llgo-go.sh
scriptpath=$(which "$0")
scriptpath=$(readlink -f "$scriptpath")
bindir=$(dirname "$scriptpath")
prefix=$(dirname "$binddir")

cmd="$1"

case "$cmd" in
build | get | install | run | test)
  shift
  PATH="$prefix/lib/llgo/go-path/:$PATH" exec "$cmd" -compiler gccgo "$@"
  ;;
  
*)
  exec go "$@"
  ;;
esac
```

```
```

```
```


