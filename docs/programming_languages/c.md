# C

## GCC

The following command lists the activated optimizations

```
gcc -Q <used optimizations, like -O2> --help-optimizers
```

To enable or disable optimizations at code level, GCC specific pragmas can be used

```
#pragma GCC push_options
#pragma GCC optimize("O0")

<code>

#pragma GCC pop_options
```