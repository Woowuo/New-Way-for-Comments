 # Some Explanations of my Denotations.
  
  1.`M {pattern[].len} = len(pattern)`<br>
    ***pattern*** -> array name<br>
    ***[]*** -> data type ***array***<br>
    ***len*** -> array length<br>
    **Natural Language Description: M represents the length of an array named pattern**<br>
  2.`i{text[I]}`<br>
    ***I*** -> Index, a jargon of computer science,representing in **CAPITAL LETTERS**<br>
    **Natural Language Description: i represents the index of an array named text.**<br>
  3. 
  ```
  //next[j]: {MAX_LEN(pattern[[0~j]],PALIM)}.
  j = [j-1]
  ```
  
  ***pattern[[0~j]]*** -> The substring of `pattern` from index 0 to index j(inclusive)<br>
  ***MAX_LEN()*** -> Like a function, return the max size of an array, and the array must satisfies the second parameter,which describes the attribute of the array.<br>
  ***PALIM*** -> Palimdromic, a jargon of computer science,representing in **CAPITAL LETTERS**<br>
  **Natural Language Description:<br> next[j] represents the max length of a string,which belongs to a set of strings. The set of strings must satisfies the following conditions:<br> 1.Any string of the set is a subsequence of an substring of pattern[0~j].<br>
  2.The subsequence must starting from index 0, ending index must <= j.<br>
  3.The subsequence must be palindromic.br<>**
  
  

