#### BufBomb

Overflowing the Gets() function in C in order to take control over the program.

Typically, this recipe was followed:
  * overwrite the return address on the stack
  * execute our byte code which would:
    * move our cookie into the %eax register
    * possibly use NOPs (null operations) to deal with dynamically allocated memory
    * reset the %ebp (base pointer) such that we avoid sementation faults

To Run:
  '''
cat *_solution.txt | ./hex2raw | ./bufbomb -u ianks
  '''
