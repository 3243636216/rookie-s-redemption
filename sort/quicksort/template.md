```
//快排
void quick_sort(int a[],int l,int r)
{
    if(l>=r) return;
    int x=a[(l+r)>>1],i=l-1,j=r+1;
    while(i<j)
    {
        while(a[++i]<x);
        while(a[--j]>x);
        if(i<j)  swap(a[i],a[j]);
    }
    quick_sort(a,l,j);
    quick_sort(a,j+1,r);
}
```
```
//快选
int quick_sort(int l,int r,int k)
{
    if(l>=r) return a[l];
    int x=a[(l+r)>>1],i=l-1,j=r+1;
    while(i<j)
    {
        while(a[++i]<x);
        while(a[--j]>x);
        if(i<j) swap(a[i],a[j]);
    }
    int sl=j-l+1;
    if(k<=sl)    return quick_sort(l,j,k); 
    else    return quick_sort(j+1,r,k-sl);
}
```
