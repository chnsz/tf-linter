# tf-lint

Static analysis libraries and tooling for [Terraform Provider](https://www.terraform.io/docs/providers/index.html) code.

It based on [tfproviderlint](https://pkg.go.dev/github.com/bflad/tfproviderlint)

## Usage

configuration options：

**fields**: specify fields will check whether these fields exist in the test file.

### Local Usage

To report issues, change into the directory of the Terraform Provider code and run:

```console
tflinter ./...
```

```console
tflinter -fields=name,enterprise_project_id ./...
```

It is also possible to run via [`go vet`](https://golang.org/cmd/vet/):

```console
go vet -vettool $(which tflinter) ./...
```

### Local Install Testing

```console
go install ./cmd/tflinter
```
