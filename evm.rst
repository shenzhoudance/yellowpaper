=====================
**EVM Instructions**
=====================

0x00    STOP
	Immidietly stops execution of the bytecode.
  
	Input Args
		None
	Return 
		None
    
---------------------

0x01    ADD
	Pop two arguments from the stack and adds them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 + value2
    
---------------------

0x02    MUL
	Pop two arguments from the stack and multiplies them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		value1 * value2
    
---------------------

0x03    SUB
	Pop two arguments from the stack and substract them.
  
	Input Args
		* value1 - first value   
		* value2 - second value
    
	Return 
		value1 - value2
    
---------------------

0x04    DIV
	Pop two arguments from the stack and divide them.
  
	Input Args
		* value1 - first value  
		* value2 - second value
    
	Return 
		(value2 != 0) ? value1 / value2 : 0
    
---------------------
