### Item 1:  Prefer const and inline to #define
1. prefer 
`const double ASPECT_RATIO = 1.653;`
to
`#define ASPECT_RATIO 1.653`
2. To define a constant char*-based string in a header file, for example, you have to write const twice: 
`const char * const authorName = "Scott Meyers";`
3. it's often convenient to define class-specific constants, and that calls for a slightly different tack.
```
    class GamePlayer {
        private:'
        static const int NUM_TURNS = 5;    // constant declaration
        int scores[NUM_TURNS];             // use of constant
        ...
    };
```
### Item 2:  Prefer <iostream> to <stdio.h>
### Item 3:  Prefer new and delete to malloc and free.
### Item 5:  Use the same form in corresponding uses of new and delete.
### Item 6:  Use delete on pointer members in destructors
### Item 7:  Be prepared for out-of-memory conditions