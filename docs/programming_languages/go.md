# Go

This note is about the Go language.

## General design

„Align the happy path to the left; you should quickly be able to scan down one column to see the expected execution flow.“ - Mat Ryer

## Design patterns


### Singleton

```Go

type Singleton interface {
  DoSomething()
}

type singleton struct {
}

(m *singleton) DoSomething() {
  //Implementation
}

var instance *singleton

var once sync.Once

func GetInstance() Singleton {
  once.Do(func() {
    instance = &singleton{}
  })
  return *instance
}
```

### Option

```Go

type options struct {
  myValue int
}

type Option func(options *options) err

func WithValue(value int) Option {
  return func(options *options) err {
    options.myValue = value
    return nil
  }
}

```