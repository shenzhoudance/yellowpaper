=====================
**EVM Instructions**
=====================

0x00    STOP
	Halts execution.
	Immidietly stops execution of the bytecode.
  
	Input Args
		None
	Return 
		None
    
---------------------

0x01    ADD
	Addition operation
	Pops two word(32byte) elements from the stack and adds them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 + value2
    
---------------------

0x02    MUL
	Multiplication operation.
	Pops two word(32byte) elements from the stack and multiplies them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 * value2
    
---------------------

0x03    SUB
	Subtraction operation.
	Pops two word(32byte) elements from the stack and substract them.
  
	Input Args
		* value1 - first value   
		* value2 - second value
    
	Return 
		value1 - value2
    
---------------------

0x04    DIV
	Integer division operation.
	Pops two word(32byte) elements from the stack and divide them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** value1 / value2 **:** 0
    
---------------------

0x05    SDIV
	Signed integer division operation (truncated).
	Where all values are treated as two’s complement signed 256-bit integers.
	Pops two word(32byte) elements from the stack and divide them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value1 == -2^255 **&&** value2 == -1) **?** -2^255 : (value2 == 0) **?** 0 **:** **sgn** (value1/value2) * value1/value2
    
---------------------

0x06    MOD
	Modulo remainder operation.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** value1 % value2 **:** 0
    
---------------------

0x07    SMOD
	Signed modulo remainder operation.
	Where all values are treated as two’s complement signed 256-bit integers.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** **sgn** (value1) * (value1 % value2) **:** 0
    
---------------------

0x08    ADDMOD
	Modulo addition operation.
	All intermediate calculations of this operation are not subject to the 2^256 modulo.
	Pops three word(32byte) elements from the stack
  
	Input Args
		* value1 - first value  
		* value2 - second value
		* value3 - module
    
	Return 
		(value3 != 0) **?** (value1 + value2) % value3 **:** 0
    
---------------------

0x09    MULMOD
	Modulo multiplication operation.
	All intermediate calculations of this operation are not subject to the 2^256 modulo.
	Pops three word(32byte) elements from the stack
  
	Input Args
		* value1 - first value  
		* value2 - second value
		* value3 - module
    
	Return 
		(value3 != 0) **?** (value1 * value2) % value3 **:** 0
    
---------------------

0x0a    EXP
	Exponential operation.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - base value  
		* value2 - exponent value
    
	Return 
		value1 ^ value2
    
---------------------

0x0b    SIGNEXTEND
	Extend length of two’s complement signed integer.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - length. Should be in range [0x00 ... 0x20]
		* value2 - original integer value.
    
	Return 
		Replaces all bits of the first **31 - arg** bytes with the first bit of byte number **31 - arg** and the rest of the bytes are copyied from the original.
		
    
---------------------

---------------------

0x10    LT
	Less-than comparision. Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 < value2) **?** 1 : 0
    
---------------------

0x11    GT
	Greater-than comparision. Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 > value2) **?** 1 : 0
    
---------------------

0x12    SLT
	Signed less-than comparision. 
	Where all values are treated as two’s complement signed 256-bit integers.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 < value2) **?** 1 : 0
    
---------------------

0x13    SGT
	Signed greater-than comparision.
	Where all values are treated as two’s complement signed 256-bit integers.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 > value2) **?** 1 : 0
    
---------------------

0x14    EQ
	Equality comparision.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 == value2) **?** 1 : 0
    
---------------------

0x15    ISZERO
	Simple not operator.
	Pops one word(32byte) element from the stack.
  
	Input Args
		* value1 - first value
    
	Return 
		(value1 == 0) **?** 1 : 0
    
---------------------

0x16    AND
	Bitwise AND operation.
	Pops two word(32byte) elements from the stack and perform a bitwise && operation.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		value1 && value2
    
---------------------

0x17    OR
	Bitwise OR operation.
	Pops two word(32byte) elements from the stack and perform a bitwise || operation.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		value1 || value2
    
---------------------

0x18    XOR
	Bitwise XOR operation.
	Pops two word(32byte) elements from the stack and perform a bitwise (+) operation.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		value1 XOR value2
    
---------------------

0x19    NOT
	Bitwise NOT operation.
	Pops two word(32byte) elements from the stack and perform a bitwise NOT operation.
  
	Input Args
		* value1 - argument to be nagaited
    
	Return 
		!value1
    
---------------------

0x1a    BYTE
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - byte number. Should be in range [0...32)
		* value2 - argument
    
	Return 
		(value1 < 32) **?** value2[value1] : 0
    
---------------------

---------------------

0x20    SHA3
	Compute Keccak-256 hash.
	Pops two word(32byte) elements from the stack.
  
	Input Args
		* value1 - Index of the first element from memory.
		* value2 - Length
    
	Return 
		sha3(memory(value1)...memory(value1 + value2 - 1))
    
---------------------

---------------------

0x30    ADDRESS
	Get address of currently executing account.
	Pops a word(32byte) element from the stack.
  
	Input Args
		* none
    
	Return 
		address (32 bytes)
    
---------------------

0x31    BALANCE
	Get balance of the provided account.
	Pops a word(32byte) element from the stack.
  
	Input Args
		* value1 - Account address
    
	Return 
		Balance of the account with address value1. 0 if such account does not exist.
    
---------------------

0x32    ORIGIN
	Get address of currently executing account.
	This is the sender of original transaction; it is never an account with non-empty associated code.
  
	Input Args
		* none
    
	Return 
		address(32 bytes)
    
---------------------

0x33    CALLER
	Get caller address.
	This is the address of the account that is directly responsible for this execution.
  
	Input Args
		* none
    
	Return 
		address(32 bytes)
    
---------------------

0x34    CALLVALUE
	Get deposited value by the instruction/transaction responsible for this execution.
  
	Input Args
		* none
    
	Return 
		bigint(32 bytes)
    
---------------------

0x35    CALLDATALOAD
	Get input data of current environment.
	This pertains to the input data passed with the message call instruction or transaction
  
	Input Args
		* value1 - index (32 bytes)
    
	Return 
		data(32 bytes) (Takes 32 bytes of data from position=value1 from input memory. If memory is not set such byte is 0)
    
---------------------
