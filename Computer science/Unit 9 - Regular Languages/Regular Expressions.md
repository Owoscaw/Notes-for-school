
Regular expressions are patterns used to specify a set of strings. They are used for finding a particular word in a string, finding combinations of characters in a string, and definiting a set of acceptable strings for a language. 
$$\Huge \{a, ab,abbb,abbbb,...\}$$
Can be written using the regular expression $ab^*$. This expression defines a set of strings that have the character "a" followed by 0 or more "b"s.

Precedence rules apply in regular expressions:
> Members side-by-side must appear in sequence
> | seperates alternatives
> * indicates 0 or more of the preceding element
> + indicates 1 or more of the preceding element
> ? indicates 0 or 1 of the preceding element
> () are used to identify groupings

For example, $a^+b^+$ describes the set of all strings with 1 or more "a"s followed by 1 or more "b"s:
$$\Huge a^+b^+=\{\,\,,a,b,aab,abb,aaab,...\}$$
$$\Huge (01)^*=\{\,\,,01,0101,010101,...\}$$
$$\Huge 10^+1=\{101,1001,10001,100001,...\}$$
$$\Large (10^+\,|\,01^+)=\{10,100,1000,...,01,011,0111,...\}$$
$$\huge 10(00)|(11)1?=\{10001,1000,1011,10111\}$$
