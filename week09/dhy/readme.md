## Week 9
### 👀 [1801](https://leetcode.com/problemset/all/?search=1801&page=1)(Medium)
####
####
### 👀 [1802](https://leetcode.com/problemset/all/?search=1802&page=1)(Medium)
####
####
### 👀 [1803](https://leetcode.com/problemset/all/?search=1803&page=1)(Hard)
####
####
### 👀 [1805](https://leetcode.com/problemset/all/?search=1805&page=1)(Easy)
####
[solution](https://github.com/DohyunYoun/study/blob/master/1805-number-of-different-integers-in-a-string/1805-number-of-different-integers-in-a-string.kt)
####
### 👀 [1806](https://leetcode.com/problemset/all/?search=1806&page=1)(Medium)
####
####
### 👀 [1807](https://leetcode.com/problemset/all/?search=1807&page=1)(Medium)
####
> 타임아웃
```kotlin
   fun evaluate(s: String, knowledge: List<List<String>>): String {
  var result = ""
        var innerText: String? = null

        val knowledgeMap = mutableMapOf<String, String>()
        knowledge.forEach {
            knowledgeMap[it[0]] = it[1]
        }

        s.forEach {

            when {
                it == '(' -> innerText = ""
                innerText == null -> result += it
                innerText != null -> innerText += it
                it == ')' -> {
         if(innerText != null && innerText!=""&& knowledgeMap.containsKey(innerText)){
                        result += knowledgeMap[innerText]
                    } else {
                        result += "?"
                    }
                    innerText = null
                }
            }
        }

//        knowledge.forEach {
//            str = str.replace("(${it[0]})", it[1])
//        }

        return result
    }
```
####
### 👀 [1808](https://leetcode.com/problemset/all/?search=1808&page=1)(Hard)
####
####
