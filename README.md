# NewMarks
An inspiration, a system of new marks could be used to help you better understand your and others' code

## Case1: Description of KMP algorithm
### Description of the Question
  Given 2 strings, `text` and `pattern`. Find if `pattern` in `text`. If `pattern` is found, return the index of the firstly matched character in text. Otherwise, return -1. Suppose `next` array is already computed.
### Natural Language Description (***Comments***) 
**This is for Human Reading and Understanding,but too VERBOSE;Besides,for developers from different countries, the translations of code are required, which makes international co-working much more harder.**
  1. Create a `next` array,which stores the number of palindromic characters from `pattern` 's first index to `pattern` 's currently visited index.
  2. Create 2 `next` values, `i` and `j`. `i`  stores the index of the currently visited character in `text` string, `j`  stores the index of the currently visited character in `pattern` string. Both `i` and `j` are initialized to 0.
  3. Compare `text[i]` with `pattern[j]`. Case1: They are identical and `j` has not yet reaches the end of the `pattern` array, `i++` and `j++`.  Case2: They are identical and `j` has already reaches the end of the `pattern` array, which means the `pattern` is found in `text`. Return `i - j`.Case3: They are distinct. And `j` is not the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `j = next[j-1]` . Case4:  They are distinct. And `j` is the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `i++`. Case5: They are distinct. And `i` has reached the end of `text`. In this case, return -1.
### Pseudo-code(***A more Concise way for Human Reading and Understanding***)
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
            return 0
          
```
### Current Fashion (***mix-up of Code and Comments***) 
**Trying to Balance ACCESSIBILITY and SIMILARITY to Real Code,But could be AMELIORATED**
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
            return 0
            
```
### My Fashion***(ACCESSIBLE AND CONCISE)***
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
            return 0

```

