### Thread 0

1

    ..main():::ENTER
    ::value == 0
    ===========================================================================
    ..main():::EXIT
    ::value one of { 1, 2 }

### Thread 1


1
    ..atomicCAS():::ENTER
    ::value one of { 0, 1 }
    ===========================================================================
    ..atomicCAS():::EXIT
    ::value one of { 1, 2 }
    ===========================================================================

1

    ..thr1():::ENTER
    ::value == 0
    ===========================================================================
    ..thr1():::EXIT
    ::value one of { 1, 2 }

### Thread 2

1
    ..atomicCAS():::ENTER
    ::value one of { 0, 1 }
    ===========================================================================
    ..atomicCAS():::EXIT
    ::value one of { 1, 2 }
    ===========================================================================

1
    ..thr1():::ENTER
    ::value one of { 0, 1 }
    ===========================================================================
    ..thr1():::EXIT
    ::value one of { 1, 2 }

Total: 5