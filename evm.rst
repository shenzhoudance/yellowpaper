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
	Pop two arguments from the stack and adds them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 + value2
    
---------------------

0x02    MUL
	Multiplication operation.
	Pop two arguments from the stack and multiplies them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 * value2
    
---------------------

0x03    SUB
	Subtraction operation.
	Pop two arguments from the stack and substract them.
  
	Input Args
		* value1 - first value   
		* value2 - second value
    
	Return 
		value1 - value2
    
---------------------

0x04    DIV
	Integer division operation.
	Pop two arguments from the stack and divide them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** value1 / value2 **:** 0
    
---------------------

0x05    SDIV
	Signed integer division operation (truncated). Pop two arguments from the stack and divide them. Where all values are treated as two’s complement signed 256-bit integers.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value1 == -2^255 **&&** value2 == -1) **?** -2^255 : (value2 == 0) **?** 0 **:** **sgn** (value1/value2) * value1/value2
    
---------------------

0x06    MOD
	Modulo remainder operation.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** value1 % value2 **:** 0
    
---------------------

0x07    SMOD
	Signed modulo remainder operation. Where all values are treated as two’s complement signed 256-bit integers.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) **?** **sgn** (value1) * (value1 % value2) **:** 0
    
---------------------

0x08    ADDMOD
	Modulo addition operation. All intermediate calculations of this operation are not subject to the 2^256 modulo.
  
	Input Args
		* value1 - first value  
		* value2 - second value
		* value3 - module
    
	Return 
		(value3 != 0) **?** (value1 + value2) % value3 **:** 0
    
---------------------

0x09    MULMOD
	Modulo multiplication operation. All intermediate calculations of this operation are not subject to the 2^256 modulo.
  
	Input Args
		* value1 - first value  
		* value2 - second value
		* value3 - module
    
	Return 
		(value3 != 0) **?** (value1 * value2) % value3 **:** 0
    
---------------------

0x0a    EXP
	Exponential operation.
  
	Input Args
		* value1 - base value  
		* value2 - exponent value
    
	Return 
		value1 ^ value2
    
---------------------

0x10    LT
	Less-than comparision.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 < value2) **?** 1 : 0
    
---------------------

0x11    GT
	Greater-than comparision.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 > value2) **?** 1 : 0
    
---------------------

0x12    SLT
	Signed less-than comparision. Where all values are treated as two’s complement signed 256-bit integers.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 < value2) **?** 1 : 0
    
---------------------

0x13    SGT
	Signed greater-than comparision. Where all values are treated as two’s complement signed 256-bit integers.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 > value2) **?** 1 : 0
    
---------------------

0x14    EQ
	Equality comparision.
  
	Input Args
		* value1 - first value
		* value2 - second value
    
	Return 
		(value1 == value2) **?** 1 : 0
    
---------------------

0x15    ISZERO
	Simple not operator.
  
	Input Args
		* value1 - first value
    
	Return 
		(value1 == 0) **?** 1 : 0
    
---------------------
