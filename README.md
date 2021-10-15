# SANTITIZER FOR FIRST AND_LAST_NAMES

So.... I was filing paperwork on the computer for an apartment. Their website would not allow me to apply to the apartment without typing my name perfectly, with the first letter of each word capitalized


samuel muldoon..... ERROR
SAMUEL MULDOON .... ERROR
Samuel Muldoon ..... made their website happy.

This is not the first time I have used a website which did this.

Below is code I wrote in python which makes sure that the first letter of each word is a capital (uppercase) letter and that all other letters are lowercase.

Bascially, it doesn't matter how people type things, because it takes 10 lines of code or less for the computer to fix it.  

Here you go:

```
def fix_case_on_name(xname: str) -> str:
    """
    This function correctly capitalizes people's names.
    Some examples are shown below:
    
    +------------+-----------+
    |  INPUT     |  OUTPUT   |
    +------------+-----------+
    +------------+-----------+
    | IaN MilLeR | IanMiller |
    +------------+-----------+
    | Ian Miller | IanMiller |
    +------------+-----------+
    | IAN MILLER | IanMiller |
    +------------+-----------+
    
    """
    # Impementation 
    iname = str(xname).strip()
    xparts = iname.split()
    oparts = [None]*len(xparts)
    for idx, xpart in enumerate(xparts, 0):
        opart = xpart[0].upper() + xpart[1:].lower()
        oparts[idx] = opart
    oname = " ".join(oparts)
    return oname
```
    
