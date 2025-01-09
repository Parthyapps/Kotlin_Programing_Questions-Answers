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
