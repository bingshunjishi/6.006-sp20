1-1：

![image-20230119175846942](https://t2y4y6ice-1251898419.cos.ap-chongqing.myqcloud.com/uPic/image-20230120001059134.jpg)

1-2：

```python
def swap_ends(D):
	first = D.delete_first()
  last = D.delete_last()
  D.insert_first(last)
  D.insert_last(first)
```

```python
def shift_left(D, k):
	if (k < 1) or (k > len(D) - 1):
    return
  temp = D.delete_first()
  D.insert_last(temp)
  shift_left(D, k - 1)
```

1-4：

```python
def reorder_students(L):
	n = len(L) // 2
  first_front = L.head
  for _ in range(n - 1):
  	first_front = first_front.next
  second_end = first_front.next
  for _ in range(n):
    second_end = second_end.next
  return
```

