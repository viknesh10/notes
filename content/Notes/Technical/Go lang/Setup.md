- Install the latest version of Go from https://go.dev/doc/install
- Check if right version is installed using the following code in Terminal window
```
go version
```
- Alternate way is to install through [[Homebrew]] using the following command
```
brew install go
```
- Setup PATH and [[GOPATH]] environment variables using the following commands in [[zshrc]]
- GOROOT should have been set originally as well but there has been concerns about setting GOROOT when you keep upgrading to newer versions of Go. More details are found in this blog
	https://dave.cheney.net/2013/06/14/you-dont-need-to-set-goroot-really
- Install the Go extension for VS Code
- Open a folder and create a new file hello-world.go
- Type the following code 
``` go
package main

func main() {

println("Hello World")

}
```
- Compile the code using the following command:
```
go run hello-world.go
```
- In order to make the directory a module, you need to add a mod file (or initialise it - in Go terms)
```
go mod init <directory-name>
```
- This will initialise a go.mod package inside the directory
- Adding external packages to the module:
```
go get <package-name>
```
