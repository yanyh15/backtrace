# backtrace

Latest Change:
    Used libunwind library to find caller and callee functions

 
Command to Compile and Run: 
    <br/>
    `g++ *.cpp -g -rdynamic -lunwind -lunwind-x86_64 -o backtrace`
     added flags for program to link to libunwind library
    <br/>
    `./backtrace`

    

Output when run:

    2
    works

    ./backtrace(_start+0x2d) [0x7f535250847d]
    /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf2) [0x7f53520a4082]
    ./backtrace(main+0x25) [0x7f53525099ab]
    ./backtrace(_Z6test_1i+0x33) [0x7f5352509ab0]
    ./backtrace(_Z6test_2v+0x53) [0x7f5352509b07]
    ./backtrace(_Z15printStackTraceii+0x48) [0x7f535250936d]
    Caller: _Z6test_2v
    Callee: _Z6test_1i
    Caller: main
    Callee: __libc_start_main
    Caller: _start
    Callee:
    test2
    6
    ./backtrace(_Z6test_3v+0x5d) [0x7f5352509b6d]
    ./backtrace(_Z18test_4_contextTreev+0x33) [0x7f5352509ba4]
    Caller: _Z18test_4_contextTreev
    Callee: _Z6test_3v
    Caller: _Z6test_2v
    Callee: _Z6test_1i
    Caller: main
    Callee: __libc_start_main
    Caller: _start
    Callee:
    context tree works

    _start 0x7f535250847d 0x7fffe1bb90e0
    __libc_start_main 0x7f53520a4082 0x7fffe1bb9220
    main 0x7f53525099ab 0x7fffe1bb9160
    _Z6test_1i 0x7f5352509ab0 0x7fffe1bb9300
    _Z6test_2v 0x7f5352509b07 0x7fffe1bb9360
    _Z15printStackTraceii 0x7f535250936d 0x7fffe1bb9460
    _Z6test_3v 0x7f5352509b6d 0x7fffe1bb9740
    _Z18test_4_contextTreev 0x7f5352509ba4 0x7fffe1bb97a0
    Caller: main
    Callee: __libc_start_main
    Caller: _start
    Callee:
