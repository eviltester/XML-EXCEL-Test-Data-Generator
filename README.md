XML-EXCEL-Test-Data-Generator
=============================

Prior to writing https://github.com/eviltester/XML-VB-Test-Data-Generator I wrote a Prototype for the XML driven Test Data Generator in EXCEL

This was back in 2004 - 2005 so I don't remember much about it now.

```
<!-- DataDefinitions
	contains Sets and Rules

	Sets contains
		Set (with a name) contains
			Element with the details in the contents

	Rules contains
		Rule (with a name)

		a rule can contain any of the rule blocks in any order
		
		Rule Blocks:

			SetOperation
			Range
			Term
			Optional
			Choice
			Repeat
		
		SetOperation
		============

		A SetOperation is a rule for combining sets.
	
		A SetOperation has a type which can be {Union,Intersection,Difference}

		A SetOperation can contain any number of OperatesOn which document the sets which
		the SetOperation block operates on.
	
		The rule will return a single value from the set resulting from the operation
		on the OperatesOn sets.

		Range
		=====
		
		A Range block is a rule for specifing a range of information.

		A Range block has a type which determines what kind of range it is {int,date,char}

		An int range is a number 'from' some value, 'to' some other value. It can have a specified:
		. return 'width' which can be 
		. 'paddedWith' some character and
		. 'padded' from some direction {Left,Right}

		A date range is a range of dates 'from' some date 'to' some other date. It can have a specified:
		. 'format' which determines what is returned - default is 'dddddd ttttt'

		A char range is a range of characters 'from' some char 'to' some other char.

		A range block returns a single value from the range.

		Term
		====
		A term is a simple way of getting information into the rule, it could be a literal, contained
		in the body of the term, or it could be a 'name'd rule or set.

		Optional
		========
		
		A block which is optional i.e. has a 50-50 chance of appearing or not.

		Can contain other blocks.

		Choice
		======

		A choice of blocks. One of the contained Option blocks will be selected. Option blocks can
		be weighted to have a higher (or lesser) chance of being chosen.		

		Repeat
		======
		A repeat block is a block where the contents of the block are repeated a defined or random 
		number of times.

		'from' the minimum number of times to repeat
		'to' the maximum number of times to repeat
			if no to is provided then the default is used.
 --> 
```

Licensed Under Apache 2.0
--------------------------


Copyright 2005 Alan Richardson - Compendium Developments

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.