# Sorting
Sorting is an important operation in computer programming. Its function is to rearrange any sequence of data elements (or records) into a keyword-ordered sequence.
## 1.冒泡排序； 
* 比较相邻的前两个数据，如果前面的数据a[0]大于后面的数据a[1]，就将前面两个数据进行交换。在将计数器 i ++; 
* 当遍历完N个数据一遍后，最大的数据就会沉底在数组最后a[N-1]。 
* 然后N=N-1；再次进行遍历排序将第二大的数据沉到倒数第二位置上a[N-2]。再次重复，直到N=0；将所有数据排列完毕。
* 每次遍历都会得到一个合适值到恰当位置
``` java
for(i = 0; i < n; ++i){ 
        for(j = 1; j < n - i; ++j){
            if(array[j - 1] > array[j]){
                 temp = array[j-1];
                 array[j - 1] = array[j];
                 array[j] = temp;
            }
        }
    }
 ```
 * 时间复杂度为o(n^2)，稳定排序方法
## 2.选择排序； 
* 遍历一遍找到最小的，与第一个位置的数进行交换。再遍历一遍找到第二小的，与第二个位置的数进行交换。
```
for(i; i < n; i++){
        min = i;
        for(j = i + 1; j < n; j++){
        if(array[min] > array[j])
            min = j;
        }
        temp = array[min];
        array[min] = array[i];
        array[i] = temp; 
    }

```
* 时间复杂度为o(n^2),不稳定排序方法
## 3.插入排序； 
* 1.初始时，第一个数据a[0]自成有序数组，后面的a[1]~a[N-1]为无序数组。令 i = 1; 
* 2.将第二个数据a[1]加入有序序列a[0]中，使a[0]~a[1]变为有序序列。i++; 
* 3.重复循环第二步，直到将后面的所有无序数插入到前面的有序数列内，排序完成。
```
for(i = 1; i < n; i++){
        if(array[i] < array[i-1]){
            temp = array[i]; 
        for(j = i - 1; j >= 0 && array[j] > temp; j--){   
            array[j+1] = array[j];
            }
            array[j+1] = temp;
        }
    } 
```
* 时间复杂度为o(n^2),稳定排序方法
## 4.快速排序； 
* 1. 先在无序的数组中取出一个数作为基数。（一般取第一个和最后一个）
* 2. 将比基数小的数扔到基数的左边，成为一个区。将比基数大的数扔到基数的右边，成为另一个区。 
* 3. 将左右两个区重复进行前两步操作。
* 4. 重复操作，直到每个区里只有一个数时，排序完成。
* 时间复杂度o(nLogn),不稳定排序方法
## 5.归并排序； 
*归并排序采用分治法（Divide and Conquer），将已有序的子序列合并，得到完全有序的序列；即先使每个子序列有序，再使子序列段间有序。若将两个有序表合并成一个有序表，称为二路归并。
*依次合并相邻有序子序列
## 6.希尔排序； 
