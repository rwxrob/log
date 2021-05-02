## Friday, December 4, 2020, 1:39:37PM EST <1607107177>

I *really* need to get a [Steelcase Gesture chair](https://duck.com/lite?kd=-1&kp=-1&q=Steelcase Gesture chair) when I have money.
This one from IKEA has never really cut it. But all the fancy gaming
chairs have arms preventing from sitting in Lotus and are overpriced.

## Friday, December 4, 2020, 3:43:36AM EST <1607071416>

<https://developers.google.com/protocol-buffers/docs/proto3>  
<https://blog.golang.org/protobuf-apiv2>  
<https://github.com/etcd-io/etcd/pull/12398#discussion_r505322880>  
<https://github.com/a-h/generate>  
<https://stackoverflow.com/questions/39873229/protobuf3-string-validation-with-regex>  
<https://github.com/envoyproxy/protoc-gen-validate>  
<https://research.google/pubs/pub43438/>

## Friday, December 4, 2020, 2:17:51AM EST <1607066271>

Take a look at [Mage](https://github.com/magefile/mage) when you get a
second. It's an interesting `make` alternative.

## Friday, December 4, 2020, 2:05:11AM EST <1607065511>

Nice tip from [\@taniwha3](https://twitch.tv/taniwha3) about this "hard earned" generator line for
incorporating Protocol Buffer IDL into a Go project:

```go
//go:generate bash -c "protoc -I .  *.proto --go_out=plugins=grpc,paths=source_relative:. --proto_path=$GOPATH/src/ --proto_path=$GOPATH/pkg/mod/  --proto_path=$( go list -f '{{ .Dir }}' -m github.com/golang/protobuf )"
```

