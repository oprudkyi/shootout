# shootout

The Computer Language  Benchmarks Game   
http://shootout.alioth.debian.org/

Project for reviewing/updating php programs

## Results:

### [Calculate the digits of Pi with streaming arbitrary-precision arithmetic - pidigits](http://benchmarksgame.alioth.debian.org/u32/performance.php?test=pidigits) 

1.63x speedup - from [4.56 sec](http://benchmarksgame.alioth.debian.org/u32/program.php?test=pidigits&lang=php&id=2) to 
[2.8 sec](http://benchmarksgame.alioth.debian.org/u32/program.php?test=pidigits&lang=php&id=4)

Changes:
* global variables are used for temporary values instead of arrays
* functions are inlined
* count of math operations is reduced
* functions return simple values instead of arrays
* output buffering is optimized

implementation based/ported from [lua-5](http://shootout.alioth.debian.org/u64/program.php?test=pidigits&lang=lua&id=5) version


### [array permutations - fannkuch-redux - single core version](http://benchmarksgame.alioth.debian.org/u32/performance.php?test=fannkuchredux) 

1.31x speedup - from [59 min](http://benchmarksgame.alioth.debian.org/u32/program.php?test=fannkuchredux&lang=php&id=1) to
[45 min](http://benchmarksgame.alioth.debian.org/u32/program.php?test=fannkuchredux&lang=php&id=2)

Changes:
* deep optimization of code - references, faster incrementors, avoiding double-counting of indexes 

### [array permutations - fannkuch-redux - multi core version](http://benchmarksgame.alioth.debian.org/u32q/performance.php?test=fannkuchredux) 

5.36x speedup - from [59 min](http://benchmarksgame.alioth.debian.org/u32q/program.php?test=fannkuchredux&lang=php&id=1) to
[11 min](http://benchmarksgame.alioth.debian.org/u32q/program.php?test=fannkuchredux&lang=php&id=3)

Changes:
* algorithm is based on multicore Java 6 source code by [Oleg Mazurov](http://benchmarksgame.alioth.debian.org/u32q/program.php?test=fannkuchredux&lang=java&id=1)
* multi-core support for PHP is based on [mandelbrot.php-3](http://benchmarksgame.alioth.debian.org/u64q/program.php?test=mandelbrot&lang=php&id=3)
