# Patterns

## Pattern 1
```
*****
****
***
**
*
```

```cpp
for(int i=1;i<=n;i++){
    for(int j=1;j<=n-i+1;j++)
        cout<<"*";
    cout<<endl;
}

```
## Pattern 2
```
****
*  *
*  *
****
```

```cpp
for(int i=1;i<=n;i++){
    for(int j=1;j<=n;j++){
        if(i==1 || i==n || j==1 || j==n)
            cout<<"*";
        else
            cout<<" ";
    }
    cout<<endl;
}

```

### OR
``` CPP
   
```
## Pattern 3
```
*______*
**____**
***__***
********
```

```cpp
for(int i=1;i<=n;i++){
    for(int j=1;j<=i;j++)
        cout<<"*";
    for(int k=1;k<=n-i;k++)
        cout<<"*";
    for(int j=1;j<=i;j++)
        cout<<"*";
    cout<<endl;
}

```
## Pattern 3
```
44444444
333  333
22    22
1      1
1      1
22    22
333  333
44444444
```

```cpp
for(int i=1;i<=2*n;i++){
    if(i<5){
        for(int j=1;j<=n-i+1;j++)
            cout<<n-i+1;
        for(int k=1;k<=i-1;k++)
            cout<<" ";
        for(int j=1;j<=n-i+1;j++)
            cout<<n-i+1;
        cout<<endl;
    }
    else{
        for(int j=i-n;j<=)
            cout<<;
    }
}
```



