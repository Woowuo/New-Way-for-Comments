# New Type of Languages

## Introduction
  An inspiration, a system of new denotations could be built to represent ***comments*** in coding. To represent algorithms, there are 2 ways:
1.Comments
2.Programming languages***Comments*** are actually belongs to ***natural language***, designed for ***developers***. But ***natural languages*** is not suitable for describing ***programming languages***,because ***programming languages*** are designed for ***machines***. So using ***natural languages*** to describe ***programming languages*** is not suitable. Writing ***comments***, are actually using ***natural languages*** to describe ***programming languages***, so it is not suitable. Therefore, a new type of language, trying to build ***connections between human and machine*** is needed and urgent.In the following article, ***comments*** could be denoted by ***Natural Language Description***, or ***Natural Language***,and ***Programming Languages*** could be denoted by ***Pseudo-code***.    

## Scenario: <br>
## 1.Algorithm Representation
## Different Descriptions of KMP algorithms, an algorithm used to solve string-mathcing problem.
### Description of the string-mathcing problem
  Given 2 strings, `text` and `pattern`. Find if `pattern` in `text`. If `pattern` is found, return the index of the firstly matched character in text. Otherwise, return -1. Suppose `next` array is already computed.
### Natural Language Description (***Comments***) 
**This is for Human Reading and Understanding,but too VERBOSE<br>Besides,for developers from different countries, the translations of comments are required, which makes international co-working much more harder.**
  1. Create a `next` array
  2. Create 2 `next` values, `i` and `j`. `i`  stores the index of the currently visited character in `text` string, `j`  stores the index of the currently visited character in `pattern` string. Both `i` and `j` are initialized to 0.
  3. Compare `text[i]` with `pattern[j]`. <br>Case1: They are identical and `j` has not yet reaches the end of the `pattern` array, `i++` and `j++`.<br> Case2: They are identical and `j` has already reaches the end of the `pattern` array, which means the `pattern` is found in `text`. Return `i - j`.<br>Case3: They are distinct. And `j` is not the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `j = next[j-1]` .<br> Case4:  They are distinct. And `j` is the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `i++`.<br>Case5: They are distinct. And `i` has reached the end of `text`. In this case, return -1.<br>
### Pseudo-code ***(A more Concise and Similar way to programming language)***
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
### Current Solution ***(mix-up of Pseudo-code and Comments)*** 
**Inserting Natural Languages in Programming Languages**
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
### My Solution ***(READABLE AND SIMILAR TO PROGRAMMING LANGUAGES)***
**All the new Denotations are contained in CURLY BRACKETS**
```
def KMP(pattern, text)

    M {pattern[].len} = len(pattern)
    N {text[].len} = len(text)
 
    i {text[I]}= 0
    j {pattern[I]}= 0 
    
    while (i{text[I]} < N{text[].len}):
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
To understand each expression means, Please view [Explanation]
