# Kotlin_Programing_Questions-Answers
Kotlin_Programing_Questions &amp; Answers

# Reverse the String using for loop
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

