# Differences-between-sealed-class-and-enum
##  DIFFERENCES BETWEEN ENUM AND SEALED CLASS
An enum is a special "class" that represents a group of constants (unchangeable variables, like final variables).
To create an enum, the enum keyword is used (instead of class or interface), and the constants are separate with a comma. The constants in an enum should be in uppercase letters. 
Example:
	enum Level {
		LOW,
		MEDIUM,
		HIGH
	     }
The constants of an enum can be accessed by the dot syntax. E.g:
Level myVar = Level.MEDUIM;

A sealed class on the other hand is used when a value can have only one of the types from a limited set (restricted hierarchies). To create a sealed class, the keyword sealed class is used.
Example:
	sealed class Currency {
		val name: String
		get() = when (this) {
		 	is Euro -> “Euro”
			is Dollar  -> “Dollars”
			is Crypto -> “Nerdcoin”
		}
	}
A sealed class like other classes can have attributes and methods but cannot instantiate an object.
## SUMMARY
1.	The major difference between enum and sealed class is that enum can have just a single instance, whereas a subclass of a sealed class can have multiple instances.
2.	A sealed class can be extended whereas, an enum cannot be extended.
3.	Child classes of a sealed class can be of different types like: data, object or normal class
4.	A sealed class can extends other classes but an enum can only implement interfaces.
5.	A sealed class is created with the sealed class keyword while an enum is created with the enum keyword.  

## REFERENCES
1.	Java Enums: https://www.w3schools.com/java/java_enums.asp
2.	Enums Types(The Java™ Tutorials): https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html
3.	Kotlin Sealed Classes: https://www.studytonight.com/kotlin/kotlin-sealed-class#
4.	Sealed Classes: https://kotlinlang.org/docs/reference/sealed-classes.html
5.	Kotlin Sealed Classes: https://www.programiz.com/kotlin-programming/sealed-class
 
