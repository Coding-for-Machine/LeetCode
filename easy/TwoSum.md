Butun sonlar massivi nums va butun son berilgan bo'lsa target, ikki raqamning indekslarini shunday qilib qaytaringki , ular qo'shilibtarget .

Siz har bir kirishda aynan bitta yechim bo'ladi deb taxmin qilishingiz mumkin va siz bir xil elementni ikki marta ishlata olmaysiz .

Javobni istalgan tartibda qaytarishingiz mumkin.

 

1-misol:

Kirish: nums = [2,7,11,15], maqsad = 9
 Chiqish: [0,1]
 Tushuntirish: chunki nums[0] + nums[1] == 9, biz [0, 1] ni qaytaramiz.
2-misol:

Kirish: raqamlar = [3,2,4], maqsad = 6
 Chiqish: [1,2]
3-misol:

Kirish: raqamlar = [3,3], maqsad = 6
 Chiqish: [0,1]
 

Cheklovlar:

2 <= nums.length <= 104
-109 <= nums[i] <= 109
-109 <= target <= 109
Faqat bitta to'g'ri javob mavjud.

```python
def twoSum(nums: list, target: int) -> list: 
        l = len(nums)
        for i in range(l):
            n = nums[i]
            d = target - n
            if d in nums[i+1:]:
                return [nums.index(n), i + nums[i+1:].index(d) + 1]

```