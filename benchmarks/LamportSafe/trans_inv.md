### Thread 0

Five

    ..main():::ENTER
    ::b1 == ::x
    ::b1 == ::y
    ::b1 == ::b2
    ::b1 == ::X
    ::b1 == 0
    ===========================================================================
    ..main():::EXIT
    ::b1 == ::b2
    ::b1 == orig(::b1)
    ::x one of { 1, 2 }
    ::y one of { 0, 1 }
    ::X one of { 0, 1 }

### Thread 1

Five

    ..thr1():::ENTER
    ::b1 == ::x
    ::b1 == ::y
    ::b1 == ::b2
    ::b1 == ::X
    ::b1 == 0
    ===========================================================================
    ..thr1():::EXIT
    ::b1 == orig(::b1)
    ::x one of { 1, 2 }
    ::y one of { 0, 1, 2 }
    ::b2 one of { 0, 1 }
    ::X one of { 0, 1 }

### Thread 2

Five

    ..thr2():::ENTER
    ::b2 == ::X
    ::b1 one of { 0, 1 }
    ::x one of { 0, 1 }
    ::y one of { 0, 1 }
    ::b2 == 0
    ===========================================================================
    ..thr2():::EXIT
    ::b2 == orig(::b2)
    ::b1 one of { 0, 1 }
    ::x one of { 1, 2 }
    ::y one of { 0, 1, 2 }
    ::X one of { 0, 1 }

Total: 15
