Here are the answers to your questions, in order:

1.  Assume l is a variable of type list, what is the type of the expression sorted(l)?
    ☑ list

2.  Assume l is a variable of type list, what is the type of the expression 1+5?
    ☑ int

3.  Assume l is a variable of type list, what is the type of the expression l.extend((5,6))?
    ☑ NoneType

4.  Assume l is a variable of type list, what is the type of the expression l.extend((5))?
    ☑ Invalid Expression (Raises Error)

5.  Assume l is a variable of type list, what is the type of the expression l[:2]?
    ☑ list

6.  Assume `l` is a variable of type `list` and has elements of type `str`, what is the type of the expression `l.index('hi')` if `'hi'` is present in the list?
    ☑ int

7.  Assume l is a variable of type list and has elements of type str, what is the type of the expression l.index('hi') if 'hi' is not present in the list?
    ☑ Invalid Expression (Raises Error)

8.  Assume l is a variable of type list and has elements of type str, what is the type of the expression l.remove('hi') if 'hi' is present in the list?
    ☑ NoneType

9.  Assume l is a variable of type list and has elements of type str, what is the type of the expression l.remove(1) if the list has more than 2 elements?
    ☑ Invalid Expression (Raises Error)

10. Assume l is a variable of type list and has elements of type str, what is the type of the expression l.pop(1) if the list has more than 2 elements?
    ☑ str

11. Assume s is a variable of type set, what is the type of the expression s.sort()?
    ☑ Invalid Expression (Raises Error)

12. Assume t is a variable of type tuple, what is the type of the expression t.sort()?
    ☑ Invalid Expression (Raises Error)

13. Assume t is a variable of type tuple, what is the type of the expression t.append(5)?
    ☑ Invalid Expression (Raises Error)

14. **Assume** `t` is a variable of type `tuple`, what is the type of the expression `t + (5,6)`?
    ☑ tuple

15. Assume t is a variable of type tuple, what is the type of the expression t.reverse()?
    ☑ Invalid Expression (Raises Error)

16. Assume `s` is a variable of type `set`, what is the type of the expression `s | s[:2]`?
    ☑ Invalid Expression (Raises Error)

17. Assume s is a variable of type set, what is the type of the expression s.append((1,2))?
    ☑ Invalid Expression (Raises Error)

18. Assume s is a variable of type set, what is the type of the expression s | (1,2)?
    ☑ Invalid Expression (Raises Error)

19. Assume s is a variable of type set, what is the type of the expression s ^ s?
    ☑ set

20. Assume s is a variable of type set, what is the type of the expression s.add({1,2})?
    ☑ Invalid Expression (Raises Error)

21. Assume d is a variable of type dict, what is the type of the expression d.sort()?
    ☑ Invalid Expression (Raises Error)

22. Assume d is a variable of type dict, what is the type of the expression sorted(d)?
    ☑ list

23. Assume `d` is a variable of type `dict`, what is the type of the expression `d.append(5)`?
    ☑ Invalid Expression (Raises Error)

24. Assume d is a variable of type dict, what is the type of the expression d.update((5,6))?
    ☑ Invalid Expression (Raises Error)

25. Assume d is a variable of type dict, what is the type of the expression d.add(5,6)?
    ☑ Invalid Expression (Raises Error)

26. Assume d is a variable of type dict, what is the type of the expression d | {5:6}?
    ☑ dict

27. Assume d is a variable of type dict, what is the type of the expression (d | {5:6}).pop(5)?
    ☑ int

28. Assume d is a variable of type dict, what is the type of the expression d.values()?
    ☑ None of the Above (Specifically, `dict_values`)

29. Assume d is a variable of type dict, what is the type of the expression list(d.items())[0]?
    Also assume d is non empty.
    ☑ tuple

30. Assume d is a variable of type dict, what is the type of the expression d.popitem()?
    Also assume d is non empty.
    ☑ tuple
