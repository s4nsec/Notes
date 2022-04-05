To change inheritance and protection parameters of a handle, ::SetHandleInformation API can be used:
```C
BOOL SetHandleInformation(
_In_ HANDLE hObject, // handle to the object
_In_ DWORD dwMask, // A mask that specifies //the flag bits to be changed.
_In_ DWORD dwFlags); //actual flag value
```

The following code removes the flag from object:
```C
::SetHandleInformation(h, HANDLE_FLAG_PROTECT_FROM_CLOSE, 0);
```

Following api function retrieves the object flag:
```C
DWORD flag;
::GetHandleInformation(hObject, flag);
```

## Test image:



![my image](https://github.com/s4nsec/Notes/blob/main/aprocess.png)
