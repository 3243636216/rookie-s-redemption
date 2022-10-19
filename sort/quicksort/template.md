```
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
