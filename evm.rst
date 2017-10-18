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
