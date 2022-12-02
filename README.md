# pcre2demo

Standalone pcre2demo CMake project for easy debug

## Build

```sh
mkdir build
cd build
cmake ..
make
```

## Test

```sh
./build/pcre2demo 'cat|dog' 'the cat sat on the mat'
./build/pcre2demo -g 'cat|dog' 'the dog sat on the cat'
```

## Docs

* <https://www.pcre.org/current/doc/html/pcre2sample.html>
* <https://github.com/PCRE2Project/pcre2/blob/master/src/pcre2demo.c>
