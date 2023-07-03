# backtrace

Latest Change:
    Changed ContextNode data structure to support parent and child nodes. Also obtained stack trace in reverse order after unwinding to build tree correctly.
 
Command to Compile and Run: 
    <br/>
    `g++ *.cpp -g -rdynamic -lunwind -lunwind-x86_64 -o backtrace`
    <br/>
    `./backtrace`

    

Output when run:

    2
    works

    ./backtrace(_start+0x2d) [0x7ff9d76e24bd]
    /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf2) [0x7ff9d7284082]
    ./backtrace(main+0x25) [0x7ff9d76e4e65]
    ./backtrace(_Z6test_1i+0x33) [0x7ff9d76e4f65]
    ./backtrace(_Z6test_2v+0x4e) [0x7ff9d76e4fb7]
    ./backtrace(_Z15printStackTracei+0x51) [0x7ff9d76e46c5]
    Caller:
    Callee: _start
    Caller: _start
    Callee: __libc_start_main
    Caller: __libc_start_main
    Callee: main
    Caller: main
    Callee: _Z6test_1i
    Caller: _Z6test_1i
    Callee: _Z6test_2v
    Caller: _Z6test_2v
    Callee: _Z15printStackTracei
    test2
    6
    ./backtrace(_Z6test_3v+0x5d) [0x7ff9d76e501d]
    ./backtrace(_Z18test_4_contextTreev+0x2e) [0x7ff9d76e504f]
    ./backtrace(_Z15printStackTracei+0x51) [0x7ff9d76e46c5]
    Caller: _Z6test_2v
    Callee: _Z6test_3v
    Caller: _Z6test_3v
    Callee: _Z18test_4_contextTreev
    Caller: _Z18test_4_contextTreev
    Callee: _Z15printStackTracei
    context tree works

    _start 0x7ff9d76e24bd 0x7fffc14f80e0
    __libc_start_main 0x7ff9d7284082 0x7fffc14f82b0
    main 0x7ff9d76e4e65 0x7fffc14f8370
    _Z6test_1i 0x7ff9d76e4f65 0x7fffc14f8470
    _Z6test_2v 0x7ff9d76e4fb7 0x7fffc14f8540
    _Z15printStackTracei 0x7ff9d76e46c5 0x7fffc14f8680
    _Z6test_3v 0x7ff9d76e501d 0x7fffc14f89e0
    _Z18test_4_contextTreev 0x7ff9d76e504f 0x7fffc14f8aa0
    _Z15printStackTracei 0x7ff9d76e46c5 0x7fffc14f8b30
