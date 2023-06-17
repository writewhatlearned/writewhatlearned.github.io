# Binary Search

<!--more-->

# 二分查找

## 原理

二分查找，又称折半查找，即在**有序**序列中，通过每次比较*查找值*与*序列中位数值*的大小，从而确定查找值所存在的序列折半空间，依次循环往复，直至序列半空间大小为1时停止，从而确定该有序序列是否存在该值。

> 折半空间，即以序列中位数值为分割点，将序列对等分为左右子序列。

## 源码

```python
def binary_search(ordered_list: list, find_value: any) -> Union[int, None]:
    low = 0
    high = len(ordered_list) - 1  # low和high跟踪折半空间
  
    while low <= high:			 # 循环结束准则，折半空间至少含有1个元素 
        mid = (low + high) / 2	 # 每次比较其中位数值的索引
        guess = ordered_list[mid]
        if guess == find_value:	 # 相等 
            return mid
        if guess > find_value:	 # 大了，high取左边，即最大值在mid左边
            high = mid - 1
        else:					 # 小了，low取右边，即最小值在mid右边
            low = mid + 1
    return None

```

## 复杂度

### 空间复杂度

### 时间复杂度

