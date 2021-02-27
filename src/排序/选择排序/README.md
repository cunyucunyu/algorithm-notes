# 选择排序

- 选择排序
- 挑出少量几个最大数或最小数
- 交换模板

## 选择排序

```java
public static void selectionSort(int[] arr){
    for(int i=0;i<arr.length-1;i++){
        int index=i;
        for(int j=i+1;j<arr.length;j++){
            index=arr[index]<arr[j]?index:j;
        }
        swap(arr,i,index);
    }
}
```

## 挑出少量几个最大数或最小数

```java
// 最小的和第二小的
int min1 = Integer.MAX_VALUE, min2 = Integer.MAX_VALUE;
// 最大的、第二大的和第三大的
int max1 = Integer.MIN_VALUE, max2 = Integer.MIN_VALUE, max3 = Integer.MIN_VALUE;

for (int x : nums) {
    if (x < min1) {
        min2 = min1;
        min1 = x;
    } else if (x < min2) {
        min2 = x;
    }

    if (x > max1) {
        max3 = max2;
        max2 = max1;
        max1 = x;
    } else if (x > max2) {
        max3 = max2;
        max2 = x;
    } else if (x > max3) {
        max3 = x;
    }
}
```

## 交换模板

```java
private static void swap(int[] arr,int i,int j){
    int temp=arr[i];
    arr[i]=arr[j];
    arr[j]=temp;
}
```













