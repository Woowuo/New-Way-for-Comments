 # Some Explanations of my Denotations.
 ## To traceback to introducing page, please view [README] (https://github.com/Woowuo/NewMarks/edit/main/README.md)
 ### 1.`M {pattern[].len} = len(pattern)`
    1. pattern -> array name
    2. [] -> data type array
    3. len -> array length
   **Natural Language Description: M represents the length of an array named pattern**<br>
### 2.`i{text[I]}`
    1. I -> Index, a jargon of computer science,representing in CAPITAL LETTERS
   **Natural Language Description: i represents the index of an array named text.**<br>
  ## 3. 
  ```
  //next[j]: {MAX_LEN(SET(pattern[[0~j]]),PALIM)}.
  j = [j-1]
  ```
  **This expression shows an example of syntax of my language.**<br>
  ``` SET -> A type name(typeid in C++) of Data Structure, representing in CAPITAL LETTERS, could use different symbols to represent it in future.
  1. To represent array, I have used [], [] and SET are actually the same, both used to describe the name of data structure.
  2. pattern[[0~j]] -> The substring of `pattern` from index 0 to index j(inclusive)
  3. SET(pattern[[0~j]] -> A set consists of substrings of `pattern`.The substrings in this set must starting from index 0, 
  ending index must <= j
  4. MAX_LEN() -> Like a function, could be overloaded.In this version of overloading, MAX_LEN() takes 2 parameters. 
     1.The first parameter is a kind of `std::multiset` in C++, or just multiset in mathematics, a kind of collection of different elements.
  
     2.The second parameter is A descriptive jargon in Computer Science(adjective slangs),such as palindromic, abbreviated to PALIM in my syntax
  
  The return value of the MAX_LEN means: The element in the multiset which has max size, and this element must satisfies the second parameter.
  In this case, Please view Natural Language Description.
  
  5.PALIM -> Palindromic, a jargon of computer science,representing in CAPITAL LETTERS
  ```
  **Natural Language Description:<br> next[j] represents the max length of a string,which belongs to a set of strings.<br>
  The set of strings must satisfies the following conditions:<br> 1.Any string of the set is an substring of pattern[0~j].<br>
  2.The substring must starting from index 0, ending index must <= j.<br>
  3.The substring must be palindromic.**
  
  

