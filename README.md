# J: From C to C++20

J is an [array programming language](https://en.wikipedia.org/wiki/Array_programming) created by [Ken Iverson](https://en.wikipedia.org/wiki/Kenneth_E._Iverson) and [Roger Hui](https://en.wikipedia.org/wiki/Roger_Hui) (see image below).

This is a fork of `jsoftware/jsource` and we will be porting it to C++20.

## Goals
* [ ] Reduce complexity of build options
   * [x] Remove [blis](https://github.com/flame/blis)
   * [x] Remove [SLEEF](https://sleef.org/)
   * [x] Remove AVX
   * [x] Remove Neon
   * [x] Remove SSE41
   * [x] Remove SSE42
   * [x] Remove SSSE3
   * [x] Remove Android
   * [x] Remove Windows (just use [WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions#whats-new-in-wsl-2))
   * [ ] Remove Raspberry Pi (not sure if much to do here)
   * [x] Remove blis
   * [ ] Remove 32 bit support
   * [ ] Remove big endian support
* [ ] Compile with GCC 10+
* [ ] Compile with Clang 11+
* [ ] Remove all (most) of the macros
* [ ] Clang-format the code base
* [ ] Clang-tidy the code base
* [ ] Set up Travis-CI
* [ ] Set up CodeCov
* [ ] Set up [badges](https://github.com/badges/shields)
* [ ] Get both build / tests running in parallel
   * [x] Parallel build (for free off of zhihaoy branch)
   * [ ] Parallel tests
* [ ] Monitor compile & run time perf while refactoring

## Non-Codebase Goals

* [ ] Learn to not use mouse

## Comparison of Languages

Calculating the first 10 odd numbers:

**Python**:
```python
[1 + 2 * i for i in range(10)]
```
**Haskell**:
```hs 
map (1+) $ map (2*) [0..9]
map ((+1) . (*2)) [0..9] -- alternative thanks to Alexandru Dinu
```
**R**:
```R
-1+2*seq(10) -- thanks to Roi Barkan
```
**APL**:
```apl
1+2×⍳10
```
**J**:
```ijs
1+2*i.10
```

## Getting started & Building:
For building this repository, please see `CONTRIBUTING.md`.

![image](https://user-images.githubusercontent.com/36027403/104798929-e4311700-5798-11eb-859c-5a55738daf79.png)
