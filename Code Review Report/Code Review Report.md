
|Line No.|Defect Type|Problem|Proposed Fix|Severity|

|40|Array Overflow|Adding more than 5 monsters may corrupt memory.|Check the maximum limit before adding.|High|

|46|Assignment Error|`=` changes the ID instead of comparing it.|Use `==` instead.|High|

|53–54|Null Pointer|Accessing a missing monster may crash the program.|Check `if (!m) return 0;`.|High|

|55|Unsigned Underflow|Health subtraction may produce an incorrect value.|Check health before subtraction.|High|

|63|Off-by-One Error|The loop accesses an invalid array index.|Use `i < monsterCount`.|High|

|70–73|Dangling Reference|Returns a reference to a destroyed local string.|Return `std::string` by value and check for 

null.|High|

|77, 80|Uninitialized Variable|`sum` is uninitialized and division by zero is possible.|Initialize `sum` and check the 

count.|High|

|85–86|Use-After-Free|Accesses monster data after deletion.|Print the name before deleting the object.|High|

|91|Precision Loss|Integer arithmetic may lose decimal precision.|Convert an operand to `double`.|Low|

|98|Missing Return|Some inputs do not return a value.|Add a default return statement.|Medium|

|102, 105|Buffer Overflow|Input may exceed the buffer; incorrect deletion causes errors.|Use `std::string` instead.|High|

|118|Memory Leak|The `bonus` object is never deleted.|Delete it or use a smart pointer.|Medium|

|129|Shallow Copy|Copying `Game` may cause double deletion.|Implement deep copying or disable copying.|High|
