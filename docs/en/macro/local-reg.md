# Use internal storage area in script

SKTOOL configuration software provides the operation interface for HMI internal storage area. Users can make direct operations for the internal storage area in the script. Detailed methods have two kinds:

1.  Access storage area with keywords

LocalBit: reference of internal storage area LB; LocalWord: reference of internal storage area LW; RWIWord: reference of internal storage area RWI.

The keyword can be used directly in macro. For example:

```c
if(LocalBit[5])
{
LocalWord[1]=0;
}
```

else

```c
{
LocalWord[1]=1;
}
```

2.  Establish a linkage between variable and internal storage area by setting of variable. Detailed usage refers to script instance.
