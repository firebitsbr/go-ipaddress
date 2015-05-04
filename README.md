# ipv4
--
    import "github.com/hit9/go-ipv4/ipv4"

Ipv4 address utils for golang.

## Usage

#### func  Atoi

```go
func Atoi(addr string) (sum uint32, err error)
```
Atoi returns the uint32 representation of an ipv4 addr string value.

Example:

    Atoi("192.168.0.1")   // 3232312315

#### func  Itoa

```go
func Itoa(integer uint32) string
```
Itoa returns the string representation of an ipv4 addr uint32 value.

Example:

    Itoa(3232312315)  // "192.168.0.1"

#### func  Next

```go
func Next(addr string) (string, error)
```
Example:

    Next("192.168.0.1")  // "192.168.0.2"

#### func  Not

```go
func Not(addr string) (string, error)
```
Example:

    Not("0.0.255.255")  // "255.255.0.0"

#### func  Or

```go
func Or(addra string, addrb string) (addr string, err error)
```
Example:

    Or("0.0.1.1", "1.1.0.0")  // "1.1.1.1"

#### func  Prev

```go
func Prev(addr string) (string, error)
```
Example:

    Prev("192.168.0.1")  // "192.168.0.0"

#### func  Xor

```go
func Xor(addra string, addrb string) (addr string, err error)
```
Example:

    Xor("0.255.255.255", "192.255.255.255")  // "192.0.0.0"

#### type Net

```go
type Net struct {
	address   string // address
	bitmask   uint8  // bitmask
	mask      string // mask
	hostmask  string // hostmask
	broadcast string // broadcast
	first     string // first
	last      string // last
	size      uint32 //size
}
```


#### func  Network

```go
func Network(block string) (net Net, err error)
```
Returns information for a netblock.
