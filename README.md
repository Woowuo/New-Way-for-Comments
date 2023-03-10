# A new way to write your comments
An inspiration, a system of new denotations could be built to represent comments. Writing comments is too annoying.

## Case1: Description of KMP algorithm
### Description of the Question
  Given 2 strings, `text` and `pattern`. Find if `pattern` in `text`. If `pattern` is found, return the index of the firstly matched character in text. Otherwise, return -1. Suppose `next` array is already computed.
### Natural Language Description (***Comments***) 
**This is for Human Reading and Understanding,but too VERBOSE<br>Besides,for developers from different countries, the translations of comments are required, which makes international co-working much more harder.**
  1. Create a `next` array
  2. Create 2 `next` values, `i` and `j`. `i`  stores the index of the currently visited character in `text` string, `j`  stores the index of the currently visited character in `pattern` string. Both `i` and `j` are initialized to 0.
  3. Compare `text[i]` with `pattern[j]`. <br>Case1: They are identical and `j` has not yet reaches the end of the `pattern` array, `i++` and `j++`.<br> Case2: They are identical and `j` has already reaches the end of the `pattern` array, which means the `pattern` is found in `text`. Return `i - j`.<br>Case3: They are distinct. And `j` is not the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `j = next[j-1]` .<br> Case4:  They are distinct. And `j` is the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `i++`.<br>Case5: They are distinct. And `i` has reached the end of `text`. In this case, return -1.<br>
### Pseudo-code ***(A more Concise way,but too hard for Human Reading and Understanding)***
**Similar to Real Code, but too UNREADABLE**
```
def KMP(pattern, text)

    M = len(pattern)
    N = len(text)
 
    i = 0
    j = 0 
    
    while (i < N):
        if pattern[j] == text[i]:
          i += 1
          j += 1
          if j == M:
            return (i - j)
          else
            continue
        else
          if j != 0 and i != N
            j = next[j-1]
          elif j == 0
            i++
          else
            return -1
          
```
### Current Fashion ***(mix-up of Code and Comments)*** 
**Trying to Balance  and SIMILARITY to Real Code,But could be AMELIORATED**
```
def KMP(pattern, text)
    
    M = len(pattern) // M is the length of pattern
    N = len(text) // N is the length of text
 
    i = 0 // i is the index of text
    j = 0 // j is the index of pattern
    
    while (i < N):
    
        if pattern[j] == text[i]:
          i += 1
          j += 1
          
          /*
            Case1: 
            They are identical and `j` has not yet reaches the end of the `pattern` array,
            In this case,`i++` and `j++`.
         */
          if j == M:
            return (i - j)
         
          /*
            Case2: 
            They are identical and `j` has already reaches the end of the `pattern` array, which means the `pattern` is found in `text`. 
            In this case,Return `i - j`
          */
          else
            continue
        else// They are distinct
       
          /*
            Case3: 
            They are distinct. And `j` is not the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. 
            In this case, `j = next[j-1]` . 
          */
          if j != 0 and i != N
            j = next[j-1]
          
          /*
            Case4:  They are distinct. And `j` is the beginning character of the `pattern`. And `i` is not the ending character of the `text` string.
            In this case, `i++`.
          */
          elif j == 0
            i++
            
          /*
            Case5: They are distinct. And `i` has reached the end of `text`. 
            In this case, return -1. 
          */
          else
            return -1
            
```
### My Fashion ***(ACCESSIBLE AND CONCISE)***
**All the new Denotations are contained in CURLY BRACKETS**
```
def KMP(pattern, text)
    
    // M: {pattern[].len}
    M  = len(pattern)
    // N: {text[].len} 
    N  = len(text)
    
    // i: {text[I]}
    i = 0
    // j: {pattern[I]}
    j = 0 
    
    // i: {text[I]}, N: {text[].len}
    while (i < N):
        if pattern[j] == text[i]:
          i += 1
          j += 1
          if j == M{pattern[].len}:
            return (i - j)
          else
            continue
        else
          if j != 0 and i != N
            //next[j]: {MAX_LEN(SET(pattern[[0~j]]),PALIM)}
            j = next[j-1]
          elif j == 0
            i++
          else
            return -1

```
### 1.`M???{pattern[].len} `
    1. pattern -> array name
    2. [] -> data type array
    3. len -> array length
   **Natural Language Description: M represents the length of an array named pattern**<br>
### 2.`i???{text[I]}`
    1. I -> Index, a jargon of computer science,representing in CAPITAL LETTERS
   **Natural Language Description: i represents the index of an array named text.**<br>
  ## 3. 
  ```
  //next[j]: {IF pattern[0~j] IS PALIM: j/2 +1 DEFAULT:0}.
  //next[0] == 0
  j = next[j-1]
  ```
  **This expression shows an example of syntax of my language. The value of next[j] equals to:**<br>
  1.If the substring of pattern starting from index 0, ending at index j is **palindromic**, next[j] = j/2 + 1
  2.If this substring is not **palimdromic**, next[j] will be set to default value, that is 0.
  3.next[0] is **always 0**.
  **Natural Language Description:<br> next[j] represents the maximum length with the same prefix and suffix in [0, i-1] before i<br>
  1. To represent array, I have used [], [] and SET are actually the same, both used to describe the name of data structure.
To be continued, I will show you another example that this method will GREATLY enhance the readability of code.<br>
[Example Code]https://users.cs.fiu.edu/~weiss/dsaa_c2e/avltree.c

In the following snippet of code, assume that an AVL tree test is calling the function. I suppose using **Nature Language Description** to comment will cost too much characters.
```
Position FindMin( AvlTree T )
{
  if( T == NULL )// The Height of T is -1 
    return NULL;
    
  // T has no left child,
  // T->ElemenType is minimum value of the AVL tree test
  else if( T->Left == NULL )
     return T;
     
  else
     return FindMin( T->Left );// T is no
}

```
With my new method, the complete version(including code and comments) would be like:
```
Position FindMin( AvlTree T )
{
   // T:{H = -1}
  if( T == NULL ) 
    return NULL;
  
  // T:{(!LeftChild)}, T->Element: {MIN(AVL test)}  
  else if( T->Left == NULL )
     return T;
     
  else
     return FindMin( T->Left );// T is no
}

```
Explanations:<br>
### 1.`T: {H = -1}`
The height of the node T is -1, that is, T is a null node.
### 2.`T:{(!LeftChild)}, T->Element: {MIN(AVL test)}`
Node T has no Left Child, the Element of T is the minimum element of the AVL tree test.

