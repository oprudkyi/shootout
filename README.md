# shootout

The Computer Language  Benchmarks Game   
http://shootout.alioth.debian.org/

Project for reviewing/updating php programs

## Results:

### [pidigits](http://benchmarksgame.alioth.debian.org/u32/performance.php?test=pidigits) 

1.63x speedup - from [4.56 sec](http://benchmarksgame.alioth.debian.org/u32/program.php?test=pidigits&lang=php&id=2) to 
[2.8 sec](http://benchmarksgame.alioth.debian.org/u32/program.php?test=pidigits&lang=php&id=4)

Changes:
* global variables are used for temporary values instead of arrays
* functions are inlined
* count of math operations is reduced
* functions return simple values instead of arrays
* output buffering is optimized

implementation based/ported from [lua-5](http://shootout.alioth.debian.org/u64/program.php?test=pidigits&lang=lua&id=5) version


