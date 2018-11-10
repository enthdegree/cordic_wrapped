# wrapped_cordic
Wrapped calls to functions from Voidware's CORDIC methods here: http://www.voidware.com/cordic.htm

The effect is a reasonably precise implementation of special functions whose compile size is much smaller than their equivalents in `<math.h>`, albeit a bit slower.

To use in your project, bring the following files in:
```
cordic.c, cordic_consts.c, cordic_wrapped.c, cordic_wrapped.h
```
Add `cordic.c` and `cordic_wrapped.c` to your makefiles, and to include use `#include cordic_wrapped.h`.

----

To run some precision tests against equivalent functions in `<math.h>`, compile `test_math.c`:

```
    $ cc -lm ./cordic.c ./cordic_wrapped.c ./test_math.c
    $ ./a.out
```
To regenerate constants, see `cordic_consts.c`.


## Todo:
- Fix `atan_wc`'s imprecision
- Add more thorough tests in `test_math.c`
