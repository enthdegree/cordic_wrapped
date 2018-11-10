# wrapped_cordic
Wrapped calls to functions from Voidware's CORDIC implementation here: http://www.voidware.com/cordic.htm.

To test, run:

<code>
   $ cc -lm ./cordic.c ./cordic_wrapped.c ./test_math.c
   
   $ ./a.out
</code>
