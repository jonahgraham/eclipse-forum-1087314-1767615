This project will fail with a build error. To fix it
you need to add the folder containing proj_a.h as GCC
sees it.

make all 
Building file: ../Hello.c
Invoking: GCC C Compiler
gcc -I"/tmp/so/ProjectB" -O0 -g3 -Wall -c -fmessage-length=0 -MMD -MP -MF"Hello.d" -MT"Hello.o" -o "Hello.o" "../Hello.c"
../Hello.c:1:20: fatal error: proj_a.h: No such file or directory
 #include "proj_a.h"
                    ^
compilation terminated.
subdir.mk:18: recipe for target 'Hello.o' failed
make: *** [Hello.o] Error 1
