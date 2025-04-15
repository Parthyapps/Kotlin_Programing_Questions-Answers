# Kotlin_Programing_Questions-Answers
Kotlin_Programing_Questions &amp; Answers

# 1.Reverse the String using for loop
 ```kotlin
    fun main() {
    val string = "ihtrap"
    println(reverse(string))
   }
  fun reverse(string: String):String{
      val char = CharArray(string.length)
      for (i in string.indices){
          char[i] = string[string.length- i -1]
      }
      return String(char)
  }
```
# 2. Find the 3rd Largest Number
   ```kotlin
         fun main() {
         val array = intArrayOf(22,31,26,3,55,12)
         println(  findmax(array))
         }
         fun findmax(array: IntArray): Int{   
             var first =Int.MIN_VALUE
             var second = Int.MIN_VALUE
             var third = Int.MIN_VALUE
             
             for (num in array){
                 if (num > first){
                     third = second
                     second = first
                     first = num
                 }else if( num > second && num != first){
                     third  = second
                     second = num
                 } else if( num > third && num != second){
                     third = num
                 }
             }
             
             return first
         }

// find second largest number

fun main() {
    val array = intArrayOf(3,1,34,12,43)
    val result = secondLargestNum (array)
    println(result)
}

fun secondLargestNum (array: IntArray) : Int{
    var first = Int.MIN_VALUE
    var second = Int.MIN_VALUE
    println(first)
    println(second)
    for (num in array){
        if (num > first){
            second = first
            first = num
        }
    }
    return first
}
   ```

# 3.Check if a string is a palindrome without shortcuts.
   ```kotlin
     
      fun main() {
           val kotlin = "madam"
           println(isPalindrom(kotlin))
       }
    
      fun isPalindrom(kotlin: String): Boolean{
       
       val n = kotlin.length
        
        for (i in 0 until n/2){
            if(kotlin[i] != kotlin[ n - i -1]) {
                return false
        }
        }  
        return true
    }
   ```
# 4.Problem: Find the largest number without built-ins.
```kotlin
fun main() {
    val array = intArrayOf(64,2,34,12,33,56)
    println(findLargestNum(array))
}

fun findLargestNum(array: IntArray):Int{
    var maximum = Int.MIN_VALUE
    for(i in array){
        if(i > maximum){
            maximum = i
        }
    }
    return maximum
}
```
# 5.Check if a number is prime manually.

```kotlin
fun main() {
    val number = 23
    println(isPrime(number))
}

fun isPrime(number: Int): Boolean{
    
    if (number<=1) return false
    
    for (i in 2 until number){
        
        if (number % i == 0) return false
    }
    return true
}
```
# 6.Problem: Find the factorial of a number iteratively.
```kotlin
fun main() {
    val number = 5
    println(findFactorial(number))
}

fun findFactorial(number: Int):Long{
    
    var result = 1L
    
    for(i in 1..number){
        result *= i
    }
    
    return result
}
```
# 7.Print Prime Odd Numbers (1 to 100)
```kotlin
fun main() {
    for(i in 1..100){
        if(i % 2 !=0 && isPrime(i)){
            println(i)
        }
    }
}

fun isPrime(num : Int):Boolean{
   
    if(num <=1) return false
    for (i in 2 until num){
        if(num % i ==0){
            return false
        }
    }
    return true
}
```
# 8.Remove Duplicate Elements from Array

```kotlin
fun main() {
    val array = intArrayOf(1,1,2,1,24,1,2,5,5)
    val result = removeDuplicateArray(array)
    println("removed duplicates : ${result.joinToString(" ,")}")
}

fun removeDuplicateArray(array: IntArray): IntArray{
    val list = mutableListOf<Int>()
    for (i in array){
        if(i !in list){
            list.add(i)
        }
    }
    return list.toIntArray()
}
```

# 9.Problem: Sort an array without using built-in methods.

```kotlin
fun main() {
    val array = intArrayOf(64, 34, 25, 12, 22, 11, 90)
    
    val result = bubbleSort(array)

    println("sort: ${result.joinToString(", ")}")
}

fun bubbleSort(array: IntArray): IntArray{
    val n = array.size
     for (i in 0 until n-1){
         for (j in 0 until n-i -1){
         if (array[j] > array[j+1]){
             val temp = array[j]
             array[j] = array[j+1]
             array[j+1] = temp
          }
         }
     }
     return array
}
```
# 10.Count Character Occurrence
```kotlin
fun main() {
    val string = "Hell0 kotlin count"
    
    var count = 0
    val char = 'o'
    for (c in string){
        
        if(char == c) count++
    }
    println(count)
}
```


