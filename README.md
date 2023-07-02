# backtrace

Latest Change:
    Obtained accurate function caller and callee. 
 
Command to Compile and Run: 
    <br/>
    `g++ *.cpp -g -rdynamic -lunwind -lunwind-x86_64 -o backtrace`
    <br/>
    `./backtrace`

    

Output when run:

    2
    works

    ./backtrace(_start+0x2d) [0x7f4fc496847d]
    /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf2) [0x7f4fc4504082]
    ./backtrace(main+0x25) [0x7f4fc49699e6]
    ./backtrace(_Z6test_1i+0x33) [0x7f4fc4969ae6]
    ./backtrace(_Z6test_2v+0x4e) [0x7f4fc4969b38]
    ./backtrace(_Z15printStackTracei+0x4c) [0x7f4fc4969371]
    NUM FUNCTION PRINTING: 6
    Callee: _Z15printStackTracei
    Caller: _Z6test_2v
    Callee: _Z6test_2v
    Caller: _Z6test_1i
    Callee: _Z6test_1i
    Caller: main
    Callee: main
    Caller: __libc_start_main
    Callee: __libc_start_main
    Caller: _start
    Callee: _start
    Caller:
    test2
    6
    ./backtrace(_Z6test_3v+0x5d) [0x7f4fc4969b9e]
    ./backtrace(_Z18test_4_contextTreev+0x2e) [0x7f4fc4969bd0]
    ./backtrace(_Z15printStackTracei+0x4c) [0x7f4fc4969371]
    NUM FUNCTION PRINTING: 3
    Callee: _Z15printStackTracei
    Caller: _Z18test_4_contextTreev
    Callee: _Z18test_4_contextTreev
    Caller: _Z6test_3v
    Callee: _Z6test_3v
    Caller: _Z6test_2v
    context tree works

    _start 0x7f4fc496847d 0x7fffe05300e0
    __libc_start_main 0x7f4fc4504082 0x7fffe0530220
    main 0x7f4fc49699e6 0x7fffe0530160
    _Z6test_1i 0x7f4fc4969ae6 0x7fffe0530300
    _Z6test_2v 0x7f4fc4969b38 0x7fffe0530360
    _Z15printStackTracei 0x7f4fc4969371 0x7fffe0530410
    _Z6test_3v 0x7f4fc4969b9e 0x7fffe05306e0
    _Z18test_4_contextTreev 0x7f4fc4969bd0 0x7fffe0530790
    _Z15printStackTracei 0x7f4fc4969371 0x7fffe0530810
    NUM FUNCTION PRINTING: 0
