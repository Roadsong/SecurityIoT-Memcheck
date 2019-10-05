# SecurityIoT-Memcheck

## Overview

- This repo collects valgrind memcheck reports for all groups in [WUSTL CSE 569S FALL 2019](https://cybersecurity.seas.wustl.edu/ning/teaching/F19cse569s/index.html).
- All of the test are performed under Ubuntu 18.04 64-bit version.
- All of the test are performed using the following command:

```
$ valgrind --leak-check=full --show-leak-kinds=all --log-file=[team_name].log ./embeddedlab 
```



## Results

|                 | definitely lost | indirectly lost | possibly lost | still reachable | suppressed | others |
| --------------- | :-------------: | :-------------: | :-----------: | :-------------: | :--------: | :----: |
| Anon           |                 |                 |               |       YES       |            |        |
| CSE Rangers     |                 |                 |               |       YES       |            |        |
| sudo rm -rf    |       YES       |       YES       |               |       YES       |            |  YES   |
| TBD             |       YES       |                 |               |       YES       |            |        |
| Team Blue       |       YES       |       YES       |               |       YES       |            |  YES   |
| Undecidable     |       YES       |                 |               |       YES       |            |  YES   |
| Vegie Broilers |       YES       |       YES       |               |       YES       |            |  YES   |



## Notice

- There are two tiny compilation error in ```Anon``` .
- There is a babaric protection mechnism in ```sudo rm -rf :``` , bless you.
- It takes forever to run a CNN test, so if you don't have sufficient time and memory, don't do that.
- ```Anon``` will throw a hash error and terminate execution on Ubuntu 18.04.
- ```Vegie Broilers``` will throw a segmentation fault and terminate execution on Ubuntu 18.04.


## Reference

- [Valgrind website](http://valgrind.org)
- [Valgrind paper](http://valgrind.org/docs/valgrind2007.pdf)
- [Course website](https://cybersecurity.seas.wustl.edu/ning/teaching/F19cse569s/index.html)
