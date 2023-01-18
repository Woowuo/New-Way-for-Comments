# NewMarks
An inspiration, a system of new marks could be used to help you better understand your and others' code

## Case1: Description of KMP algorithm
### Description of the Question
  Given 2 strings, `text` and `pattern`. Find if `pattern` in `text`. If `pattern` is found, return the index of the firstly matched character in text. Otherwise, return -1. Suppose `next` array is already computed.
### Natural Language Description (***Comments***) 
**Without Using My Symbol, and This is for Human Reading and Understanding,but too VERBOSE;Besides,for people from different countries, it is needed to write different translations of comments, which makes communication much more harder.**
  1. Create a `next` array,which stores the number of palindromic characters from `pattern` 's first index to `pattern` 's currently visited index.
  2. Create 2 `next` values, `i` and `j`. `i`  stores the index of the currently visited character in `text` string, `j`  stores the index of the currently visited character in `pattern` string. Both `i` and `j` are initialized to 0.
  3. Compare `text[i]` with `pattern[j]`. Case1: They are identical and `j` has not yet reaches the end of the `pattern` array, `i++` and `j++`.  Case2: They are identical and `j` has already reaches the end of the `pattern` array, which means the `pattern` is found in `text`. Return `j - i`.Case3: They are distinct. And `j` is not the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `j = next[j-1]` . Case4:  They are distinct. And `j` is the beginning character of the `pattern`. And `i` is not the ending character of the `text` string. In this case, `i++`. Case5: They are distinct. And `i` has reached the end of `text`. In this case, return -1.
### Pseudo-code(***A more Concise way for Human Reading and Understanding***)
**Close to Real Code, but too INACCESSIBLE**
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
### Current Fashion, or ***mix-up of Code and Comments*** **(TOO INACCESSIBLE AND TOO VERBOSE)**
```
def KMP(pattern, text)
    
    // M is the length of pattern
    M = len(pattern)
    // N is the length of text
    N = len(text)
 
    // i is the index of text
    i = 0
    // j is the index of pattern
    j = 0 
    
    while (i < N):
        if pattern[j] == text[i]:
          i += 1
          j += 1
          //case 1
          if j == M:
            return (i - j)
          else
          //case 2
            continue
        else
          //case 3
          if j != 0 and i != N
            j = next[j-1]
           //case 4
          elif j == 0
            i++
           //case 5
          else
            return 0
            
```


