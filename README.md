# Scala-Conditions

I explore the conditions notions (if ... else), pattern matching, loops and some functions notions. 

Some exercises to apply the conditions:

1.I begin with Scala Strings. In Scala, as in Java, a string is an immutable object, that is, an object that cannot be modified. A string in input, write a matching pattern that will return the same string if it is not empty, or the string "n/a" if it is empty.

```
val chaine:String=""
chaine match{
  case "" =>"n/a"
  case _ => chaine
}
```

2. Given a double, write an expression to return "larger" if it is greater than zero, "even" if it is zero, and "less" if it is less than zero. Can you write that with the conditional blocks if ... else blocks? 

```
val num = 4
num match {
  case x if x>0 => "grand"
  case x if x<0 => "petit"
  case _ => "egal"
}
```

3. Write an expression to convert one of the cyan, magenta, yellow input values to their six-character hexadecimal equivalents as a string?

```
val couleur = "cyan"


couleur match {
  case "cyan" =>"off"
  case "magenta" =>"ffo"
  case "yellow" =>"fof"
}
```

4. Print the numbers from 1 to 100, each line containing a group of five digits. For example: 1, 2, 3, 4, 5,
6, 7, 8, 9, 10?

```
for( a <- 1 to 100 by 5){
  for (i <-a to a+4) {
    print(i+", ")
  }
  println("")
}
```


5. Write an expression to print numbers from 1 to 100, except for multiples of 3, print "type" and for multiples of 5, print "safe". For multiples of 3 and 5, write "typesafe".

```
for (i <- 1 to 100)
  i match{
    case i if i%3 == 0 =>print("type")
    case i if i%5 == 0 =>print("safe")
    case i if i%3 == 0 && i%5 ==0 =>println("typesafe")
    case i =>println(i)
  }
  ```
  
 6. Write a function that calculates the area of a circle according to its radius.
 
 ```
 val pi:Double=3.14
 def area (r: Double)=pi*(r*r)
 area(4.5)
 ```
 
 7. Provide another form of the function in Exercise 6 that takes the radius as a string. What happens if your function is invoked with an empty string?

```
def area (r: String)=pi*(r.toDouble *r.toDouble)
area("2")
```

8. Write a recursive function that prints values from 5 to 50 by five, without using the for or while function in the loops. Can you make it recursive? With the scala recursion optimizer?

```
def req2 (d:Int) : Unit = {
  if (d>=5){if (d%5==4){
    req2(d-1)
    print(d+","+"\n")}
    else {
    req2(d-1)
    print(d+",")}}
}

req2(49)
```


