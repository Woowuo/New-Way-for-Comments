 # Some Explanations of my Denotations.
 ## To traceback to introduction page, please view [Intro] (https://github.com/Woowuo/NewMarks/edit/main/README.md)
 ### 1.`M {pattern[].len} = len(pattern)`
    1. pattern -> array name
    2. [] -> data type array
    3. len -> array length
    **Natural Language Description: M represents the length of an array named pattern**<br>
### 2.`i{text[I]}`
    ***I*** -> Index, a jargon of computer science,representing in **CAPITAL LETTERS**<br>
    Natural Language Description: i represents the index of an array named text.**<br>
  ## 3. 
  ```
  //next[j]: {MAX_LEN(SET(pattern[[0~j]]),PALIM)}.
  j = [j-1]
  ```
  This expression shows an example of syntax of my language.<br>
  ***SET*** -> A type name(typeid in C++) of Data Structure, representing in **CAPITAL LETTERS**, could use different symbols to represent it in future<br>
  To represent array, I have used ***[]***, ***[]*** and ***SET*** are actually the same things<br>
  ***pattern[[0~j]]*** -> The substring of `pattern` from index 0 to index j(inclusive)<br>
  ***SET(pattern[[0~j]]*** -> A set consists of substrings of `pattern`.The substrings in this set must starting from index 0, ending index must <= j
  ***MAX_LEN()*** -> Like a function, could be overloaded.In this version of overloading, ***MAX_LEN()*** takes 2 parameters. <br>
  1.The first one is a kind of `std::multiset` in C++, or just multiset in mathematics, a kind of collection of different elements.<br>
  And the para 
  2.A descriptive jargon in Computer Science(adjective slangs),such as palindromic, abbreviated to ***PALIM*** in my syntax<br>
  The return value of the ***MAX_LEN*** means: The element in the multiset which has max size, and this element must satisfies the second parameter.
  In this case, Please view ***Natural Language Description***.
  ***PALIM*** -> Palindromic, a jargon of computer science,representing in **CAPITAL LETTERS**<br>
  **Natural Language Description:<br> next[j] represents the max length of a string,which belongs to a set of strings. The set of strings must satisfies the following conditions:<br> 1.Any string of the set is an substring of pattern[0~j].<br>
  2.The substring must starting from index 0, ending index must <= j.<br>
  3.The substring must be palindromic.**
  
  

