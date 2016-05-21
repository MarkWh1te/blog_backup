# 刷题的正确姿势

刷题是指通过大量题目进行针对性的训练，如果掌握了有效方法不但可以有效地巩固学过的知识而且也可以在这个过程中收获很多的快乐！

很多人认为刷题就是单纯地做题，这个认识是片面的。就像我之前说，刷题是__针对性的训练__。做题只是这个训练的表现形式。而一次正确训练过程应该是包括目标制定，执行操作，结果分析三个部分的。

拿我在leecode上遇到的这道happy number来举例：


![leecode](http://7xq2dq.com1.z0.glb.clouddn.com/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202016-05-21%20%E4%B8%8B%E5%8D%8811.30.25.png)

简单分析一下题目的大意，就是编写一个算法判断某个数字是否是“快乐数”。

快乐数的定义过程如下：从任意一个正整数开始，将原数替换为其每一位的平方和，重复此过程直到数字=1（此时其值将不再变化），或者进入一个不包含1的无限循环。那些以1为过程终止的数字即为“快乐数”。（就想图片中那个example中的19一样）

* 目标制定

 我们有看到题目中hash table的标签，那么我们这次训练目标自然是巩固hash这个知识点了。我们可以把每次各位平方和的结果储存在一个集合（hash table）中，如果某次各位平方和结果在这个集合中已经储存过了，那么说明已经进入循环了，则这个数不是happy number，反正如果到最后结果是1，这个数就是happy number。
* 执行操作

  如果有清晰的想法，coding会变得轻松很多，python代码如下所示：
  
    
    class Solution():
      def isHappy(self, n):
          numSet = set()
          while n != 1 and n not in numSet:
              numSet.add(n)
              sum = 0
              while n:
                  digit = n % 10
                  sum += digit * digit
                  n /= 10
              n = sum
          return n == 1

* 结果分析
  
  如果对我们目前才用的方法是对是用两个while的循环完成了需求，我们知道所有循环都是可以用递归改写的，很多时候递写法会让代码更加优雅和可读，那么我们尝试来用递归解这道题目:


    class Solution():
        def __init__(self):
            self.past = set()
        def isHappy(self, n):
          intermediate = sum(int(i) ** 2 for i in str(n))
          if intermediate == 1:
              return True
          elif intermediate in self.past:
              return False
          else:
              self.past.add(intermediate)
              return self.isHappy(intermediate)

  显而易见，在对变量进行恰当的命名和用递归重构后，这段代码看起来更加具有可读性了。而在这次训练中我不仅复习了hash的用法，还巩固了递归和循环相互转化。
  

合理地制定训练目标，认真地执行训练过程再加上对结果冷静反思，才是刷题的正确姿势。happy coding！ ：P
  
  
  
  
  
  
  