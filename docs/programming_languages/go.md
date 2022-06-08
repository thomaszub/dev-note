# Go

This note is about the Go language.

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