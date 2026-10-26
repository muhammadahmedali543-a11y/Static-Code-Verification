

|Category|Item / Question|Status|Notes / Findings|

|Initialization|Are variables initialized before use?|FAIL|`sum` is uninitialized in `averageAttack()`.|

|Initialization|Are pointers and arrays initialized safely?|FAIL|`char[10]` lacks proper input boundary checks.|

|Pointers|Are pointers checked before use?|FAIL|Missing null checks in `attackMonster()`, `getMonsterLabel()`, and 

`defeatMonster()`.|

|Pointers|Are deleted pointers handled safely?|FAIL|Use-after-free in `defeatMonster()` and incorrect array deletion.|

|Pointers|Are allocations released correctly?|FAIL|Uses `delete` instead of `delete[]`; `bonus` causes a memory leak.|

|Arrays|Are array bounds checked?|FAIL|`spawnMonster()` may exceed capacity; `readBoss()` risks buffer overflow.|

|Loops|Are loop conditions correct?|FAIL|`totalMonsterHealth()` uses `<=` instead of `<`.|

|Arithmetic|Are calculations accurate?|FAIL|`calculateDamage()` uses integer division and loses precision.|

|Arithmetic|Is unsigned underflow prevented?|FAIL|`m->health - dmg < 0` fails due to unsigned arithmetic.|

|Control Flow|Are comparison operators used correctly?|FAIL|`findMonster()` uses `=` instead of `==`.|

|Control Flow|Do all non-void functions return values?|FAIL|`playerRank()` has a missing return for some scores.|

|Function Calls|Are local variables returned safely?|FAIL|`getMonsterLabel()` returns a reference to a local string.|

|Classes|Are heap-owning classes copied safely?|FAIL|`Game copy = game;` may cause double deletion due to shallow copying.|
