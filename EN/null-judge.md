# null judge

### int null value is 0,

### string null value is "" instead of null or nil (different from other languages),

### Slice nulls are Slices of length 0 instead of nil,

### map null value is nil,

### error is nil,

### A struct null value is an empty Struct with "all members are null values" instead of nil,

### You cannot simply determine whether a struct is nil, because it can never be nil. You can determine whether it is empty by returning an error
### Common practice in golang standard library: if err! = nil

### In the official document of go, nil is a predefined identifier, representing zero value of pointer, channel, function, interface, map or slice, not a reserved keyword of go
### Nil can only be assigned to a variable of type pointer, channel, func, interface, map or slice (non base type) otherwise, panic will be raised

### usual type nil

```
bool      -> false                              
numbers -> 0                                 
string    -> ""      

pointers -> nil
slices -> nil
maps -> nil
channels -> nil
functions -> nil
interfaces -> nil
```