<!-- # Markdown: Syntax

*   [Overview](#Overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#Inline HTML)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL](/projects/markdown/syntax.text).

---- -->

## Overview Questions

### What is JAVA and its features.
Java is a programming language and a platform. Java is a high level, robust, object-oriented and secure programming language.
Java was developed by Sun Microsystems (which is now the subsidiary of Oracle) in the year 1995.

Platform: Any hardware or software environment in which a program runs, is known as a platform. Since Java has a runtime environment (JRE) and API, it is called a platform.

Application:
-   Desktop Applications such as acrobat reader, media player, antivirus, etc.
-   Web Applications such as irctc.co.in, javatpoint.com, etc.
-   Enterprise Applications such as banking applications.
-   Mobile
-   Embedded System
-   Smart Card
-   Robotics
-   Games, etc.

Types of Java Applications:

There are mainly 4 types of applications that can be created using Java programming:

1.   **Standalone Application:** Standalone applications are also known as desktop applications or window-based applications. These are traditional software that we need to install on every machine. Examples of standalone application are Media player, antivirus, etc. AWT and Swing are used in Java for creating standalone applications.
2.   **Web Application:** An application that runs on the server side and creates a dynamic page is called a web application. Currently, Servlet, JSP, Struts, Spring, Hibernate, JSF, etc. technologies are used for creating web applications in Java.
3.   **Enterprise Application:** An application that is distributed in nature, such as banking applications, etc. is called an enterprise application. It has advantages like high-level security, load balancing, and clustering. In Java, EJB is used for creating enterprise applications.
4.   **Mobile Application:** An application which is created for mobile devices is called a mobile application. Currently, Android and Java ME are used for creating mobile applications.

Java Platforms / Editions: 

There are 4 platforms or editions of Java:

1.   **Java SE (Java Standard Edition):** It is a Java programming platform. It includes Java programming APIs such as java.lang, java.io, java.net, java.util, java.sql, java.math etc. It includes core topics like OOPs, String, Regex, Exception, Inner classes, Multithreading, I/O Stream, Networking, AWT, Swing, Reflection, Collection, etc.
2.   **Java EE (Java Enterprise Edition):** It is an enterprise platform that is mainly used to develop web and enterprise applications. It is built on top of the Java SE platform. It includes topics like Servlet, JSP, Web Services, EJB, JPA, etc.
3.   **Java ME (Java Micro Edition):** It is a micro platform that is dedicated to mobile applications.
4.   **JavaFX:** It is used to develop rich internet applications. It uses a lightweight user interface API.

### Basic understanding of IDE, JDK, JVM & JRE.
What is IDE? (Integrated Development Environment)
> An integrated development environment (IDE) is a software application that helps programmers develop software code efficiently. It increases developer productivity by combining capabilities such as software editing, building, testing, and packaging in an easy-to-use application. Just as writers use text editors and accountants use spreadsheets, software developers use IDEs to make their job easier.

JVM
>JVM (Java Virtual Machine) is an abstract machine. It is called a virtual machine because it doesn't physically exist. It is a specification that provides a runtime environment in which Java bytecode can be executed. It can also run those programs which are written in other languages and compiled to Java bytecode.
>
>JVMs are available for many hardware and software platforms. JVM, JRE, and JDK are platform dependent because the configuration of each OS is different from each other. However, Java is platform independent. There are three notions of the JVM: specification, implementation, and instance.
>
>The JVM performs the following main tasks:
>
>1.   Loads code
>2.   Verifies code
>3.   Executes code
>4.   Provides runtime environment

JRE
>JRE is an acronym for Java Runtime Environment. It is also written as Java RTE. The Java Runtime Environment is a set of software tools which are used for developing Java applications. It is used to provide the runtime environment. It is the implementation of JVM. It physically exists. It contains a set of libraries + other files that JVM uses at runtime.
>
>The implementation of JVM is also actively released by other companies besides Sun Micro Systems.

JDK
>JDK is an acronym for Java Development Kit. The Java Development Kit (JDK) is a software development environment which is used to develop Java applications and applets. It physically exists. It contains JRE + development tools.
>
>JDK is an implementation of any one of the below given Java Platforms released by Oracle Corporation:
>
>-   Standard Edition Java Platform
>-   Enterprise Edition Java Platform
>-   Micro Edition Java Platform
>-   The JDK contains a private Java Virtual Machine (JVM) and a few other resources such as an interpreter/loader (java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), etc. to complete the development of a Java Application.

How Java Code Gets Executed
>The Java compiler takes Java code and compiles it down to Java Bytecode which is a cross-platform format. When we run Java applications, Java Virtual Machine (JVM) gets loaded in the memory. It takes our bytecode as the input and translates it to the native code for the underlying operating system. There are various implementations of Java Virtual Machine for almost all operating systems.

Architecture of Java Applications
>The smallest building blocks in Java programs are methods (also called functions in other programming languages). We combine related methods in classes, and related classes in packages. This modularity in Java allows us to break down large programs into smaller building blocks that are easier to understand and re-use.

### Basics of Java (Variables, Data Types, Type Casting, Unicode, Operators)
Java Variables
> >A variable is a container which holds the value while the Java program is executed. A variable is assigned with a data type.
> >
> >Variable is a name of memory location. There are three types of variables in java: local, instance and static.
> >
> >There are two types of data types in Java: primitive and non-primitive.

> Variable
> >A variable is the name of a reserved area allocated in memory. In other words, it is a name of the memory location. It is a combination of "vary + able" which means its value can be changed.
> >
> >     int data=50;//Here data is variable 
>
> Types of Variables
> >There are three types of variables in Java:
> >
> >1.   local variable
> > > A variable declared inside the body of the method is called local variable. You can use this variable only within that method and the other methods in the class aren't even aware that the variable exists.
> > > 
> > > A local variable cannot be defined with "static" keyword.
> >2.   instance variable
> > > A variable declared inside the class but outside the body of the method, is called an instance variable. It is not declared as static.
> > > 
> > > It is called an instance variable because its value is instance-specific and is not shared among instances.
> >3.   static variable
> > > A variable that is declared as static is called a static variable. It cannot be local. You can create a single copy of the static variable and share it among all the instances of the class. Memory allocation for static variables happens only once when the class is loaded in the memory. 
> >
> > > Example to understand the types of variables in java
> > > 
> > >     public class A  
> > >     {  
> > >        static int m=100;//static variable  
> > >        void method()  
> > >        {    
> > >            int n=90;//local variable    
> > >        }  
> > >        public static void main(String args[])  
> > >        {  
> > >            int data=50;//instance variable    
> > >        }  
> > >    }//end of class   

Data Types in Java
> Data types specify the different sizes and values that can be stored in the variable. There are two types of data types in Java:
>
>1.   Primitive data types
> > The primitive data types include boolean, char, byte, short, int, long, float and double.
> > 
> > In Java language, primitive data types are the building blocks of data manipulation. These are the most basic data types available in Java language.
> > 
> > There are 8 types of primitive data types:
> >-    boolean data type | Default value = false | 1 bit 
> >
> >     Boolean one = false  
> >-    byte data type | Default value = '\u0000' | 2 byte
> >
> >     byte a = 10, byte b = -20  
> >-    char data type | Default value = 0 | 1 byte
> >
> >     char letterA = 'A'    
> >-    short data type | Default value = 0 | 2 byte
> >
> >     short s = 10000, short r = -5000     
> >-    int data type | Default value = 0 | 4 byte
> >
> >     int a = 100000, int b = -200000 
> >-    long data type | Default value = 0L | 8 byte
> >
> >     long a = 100000L, long b = -200000L  
> >-    float data type | Default value = 0.0F | 4 byte
> >
> >     float f1 = 234.5f  
> >-    double data type | Default value = 0.0D | 8 byte
> >
> >     double d1 = 12.3  
>2.   Non-primitive data types: 
> > The non-primitive data types include Classes, Interfaces, and Arrays.

Type Casting
> In Java, type casting is a method or process that converts a data type into another data type in both ways manually and automatically. The automatic conversion is done by the compiler and manual conversion performed by the programmer.
> 
> Type casting
> > Convert a value from one data type to another data type is known as type casting.
> Types of Type Casting
>
> >1.   Widening Type Casting
> > Converting a lower data type into a higher one is called widening type casting. It is also known as implicit conversion or casting down. It is done automatically. It is safe because there is no chance to lose data. It takes place when:
> >
> > Both data types must be compatible with each other.
> > The target type must be larger than the source type.
> > 
> >     byte -> short -> char -> int -> long -> float -> double  
> >2.   Narrowing Type Casting
> >
> > Converting a higher data type into a lower one is called narrowing type casting. It is also known as explicit conversion or casting up. It is done manually by the programmer. If we do not perform casting then the compiler reports a compile-time error.
> > 
> >     double -> float -> long -> int -> char -> short -> byte  

Unicode System
> Unicode is a universal international standard character encoding that is capable of representing most of the world's written languages.

Operators in Java
> Operator in Java is a symbol that is used to perform operations. For example: +, -, *, / etc.
>
> There are many types of operators in Java which are given below:
>
> https://www.javatpoint.com/operators-in-java
>
>-   Unary Operator,
>-   Arithmetic Operator,
>-   Shift Operator,
>-   Relational Operator,
>-   Bitwise Operator,
>-   Logical Operator,
>-   Ternary Operator and
>-   Assignment Operator.

### Java Keywords OR Java Reserved Keywords
> Java keywords are also known as reserved words. Keywords are particular words that act as a key to a code. These are predefined words by Java so they cannot be used as a variable or object name or class name.
>
>List of Java Keywords
> >A list of Java keywords or reserved words are given below:
> >
> >-   abstract: Java abstract keyword is used to declare an abstract class. An abstract class can provide the implementation of the interface. It can have abstract and non-abstract methods.
> >-   boolean: Java boolean keyword is used to declare a variable as a boolean type. It can hold True and False values only.
> >-   break: Java break keyword is used to break the loop or switch statement. It breaks the current flow of the program at specified conditions.
> >-   byte: Java byte keyword is used to declare a variable that can hold 8-bit data values.
> >-   case: Java case keyword is used with the switch statements to mark blocks of text.
> >-   catch: Java catch keyword is used to catch the exceptions generated by try statements. It must be used after the try block only.
> >-   char: Java char keyword is used to declare a variable that can hold unsigned 16-bit Unicode characters
> >-   class: Java class keyword is used to declare a class.
> >-   continue: Java continue keyword is used to continue the loop. It continues the current flow of the program and skips the remaining code at the specified condition.
> >-   default: Java default keyword is used to specify the default block of code in a switch statement.
> >-   do: Java do keyword is used in the control statement to declare a loop. It can iterate a part of the program several times.
> >-   double: Java double keyword is used to declare a variable that can hold 64-bit floating-point number.
> >-   else: Java else keyword is used to indicate the alternative branches in an if statement.
> >-   enum: Java enum keyword is used to define a fixed set of constants. Enum constructors are always private or default.
> >-   extends: Java extends keyword is used to indicate that a class is derived from another class or interface.
> >-   final: Java final keyword is used to indicate that a variable holds a constant value. It is used with a variable. It is used to restrict the user from updating the value of the variable.
> >-   finally: Java finally keyword indicates a block of code in a try-catch structure. This block is always executed whether an exception is handled or not.
> >-   float: Java float keyword is used to declare a variable that can hold a 32-bit floating-point number.
> >-   for: Java for keyword is used to start a for loop. It is used to execute a set of instructions/functions repeatedly when some condition becomes true. If the number of iteration is fixed, it is recommended to use for loop.
> >-   if: Java if keyword tests the condition. It executes the if block if the condition is true.
> >-   implements: Java implements keyword is used to implement an interface.
> >-   import: Java import keyword makes classes and interfaces available and accessible to the current source code.
> >-   instanceof: Java instanceof keyword is used to test whether the object is an instance of the specified class or implements an interface.
> >-   int: Java int keyword is used to declare a variable that can hold a 32-bit signed integer.
> >-   interface: Java interface keyword is used to declare an interface. It can have only abstract methods.
> >-   long: Java long keyword is used to declare a variable that can hold a 64-bit integer.
> >-   native: Java native keyword is used to specify that a method is implemented in native code using JNI (Java Native Interface).
> >-   new: Java new keyword is used to create new objects.
> >-   null: Java null keyword is used to indicate that a reference does not refer to anything. It removes the garbage value.
> >-   package: Java package keyword is used to declare a Java package that includes the classes.
> >-   private: Java private keyword is an access modifier. It is used to indicate that a method or variable may be accessed only in the class in which it is declared.
> >-   protected: Java protected keyword is an access modifier. It can be accessible within the package and outside the package but through inheritance only. It can't be applied with the class.
> >-   public: Java public keyword is an access modifier. It is used to indicate that an item is accessible anywhere. It has the widest scope among all other modifiers.
> >-   return: Java return keyword is used to return from a method when its execution is complete.
> >-   short: Java short keyword is used to declare a variable that can hold a 16-bit integer.
> >-   static: Java static keyword is used to indicate that a variable or method is a class method. The static keyword in Java is mainly used for memory management.
> >-   strictfp: Java strictfp is used to restrict the floating-point calculations to ensure portability.
> >-   super: Java super keyword is a reference variable that is used to refer to parent class objects. It can be used to invoke the immediate parent class method.
> >-   switch: The Java switch keyword contains a switch statement that executes code based on test value. The switch statement tests the equality of a variable against multiple values.
> >-   synchronized: Java synchronized keyword is used to specify the critical sections or methods in multithreaded code.
> >-   this: Java this keyword can be used to refer the current object in a method or constructor.
> >-   throw: The Java throw keyword is used to explicitly throw an exception. The throw keyword is mainly used to throw custom exceptions. It is followed by an instance.
> >-   throws: The Java throws keyword is used to declare an exception. Checked exceptions can be propagated with throws.
> >-   transient: Java transient keyword is used in serialization. If you define any data member as transient, it will not be serialized.
> >-   try: Java try keyword is used to start a block of code that will be tested for exceptions. The try block must be followed by either catch or finally block.
> >-   void: Java void keyword is used to specify that a method does not have a return value.
> >-   volatile: Java volatile keyword is used to indicate that a variable may change asynchronously.
> >-   while: Java while keyword is used to start a while loop. This loop iterates a part of the program several times. If the number of iteration is not fixed, it is recommended to use the while loop.

### Flow control statements(If-Else, Switch, For Loop, While Loop, Do While Loop, Break, Continue, Comments)
Java Control Statements | Control Flow in Java
> Java compiler executes the code from top to bottom. The statements in the code are executed according to the order in which they appear. However, Java provides statements that can be used to control the flow of Java code. Such statements are called control flow statements.
> Java provides three types of control flow statements.
> 
>1.   Decision Making statements
> >-   if statements
> >-   switch statement
>2.   Loop statements
> >-   do while loop
> >-   while loop
> >-   for loop
> >-   for-each loop
>3.   Jump statements
> >-   break statement
> >-   continue statement
If-Else
>
> The Java if statement is used to test the condition. It checks boolean condition: true or false. There are various types of if statement in Java.
> 
>     if(condition){  
>          //code to be executed  
>     }  
Switch
>
> The Java switch statement executes one statement from multiple conditions. It is like if-else-if ladder statement.
> 
>     switch(expression){    
>        case value1:    
>        //code to be executed;    
>        break;  //optional  
>        case value2:    
>        //code to be executed;    
>        break;  //optional  
>        ......    
>        default:     
>        code to be executed if all cases are not matched;  
>     }    
>
For Loop
>
>
>
>
>
>

While Loop
>
>
>
>


Do While Loop
>
>
>
>


Break 
>
>
>
>


Continue
>
>
>
>

Comment
>
>
>
>

### Functions
### Access Modifiers
### OOPS concepts and features
### Collection Frameworks
### File and exception handling
### Cloud Computing
### VCS
### SQL
### Agile
### Web frameworks like Spring and Hibernate(basic understanding)
### SOME BASIC CODING LOGICS AND SYNTAX

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext](http://docutils.sourceforge.net/mirror/setext.html), [atx](http://www.aaronsw.com/2002/atx/), [Textile](http://textism.com/tools/textile/), [reStructuredText](http://docutils.sourceforge.net/rst.html),
[Grutatext](http://www.triptico.com/software/grutatxt.html), and [EtText](http://ettext.taint.org/doc/) -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

## Block Elements

### Paragraphs and Line Breaks

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be indented with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a `<br />` tag.

When you *do* want to insert a `<br />` break tag using Markdown, you
end a line with two or more spaces, then type return.

### Headers

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.)


### Blockquotes

Markdown uses email-style `>` characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a `>` before every line:

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the `>` before the first
line of a hard-wrapped paragraph:

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of `>`:

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


### Lists

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

*   Red
*   Green
*   Blue

is equivalent to:

+   Red
+   Green
+   Blue

and:

-   Red
-   Green
-   Blue

Ordered lists use numbers followed by periods:

1.  Bird
2.  McHale
3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

If you instead wrote the list in Markdown like this:

1.  Bird
1.  McHale
1.  Parish

or even:

3. Bird
1. McHale
8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

To make lists look nice, you can wrap items with hanging indents:

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be indented by either 4 spaces
or one tab:

1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

*   This is a list item with two paragraphs.

    This is the second paragraph in the list item. You're
only required to indent the first line. Lorem ipsum dolor
sit amet, consectetuer adipiscing elit.

*   Another item in the same list.

To put a blockquote within a list item, the blockquote's `>`
delimiters need to be indented:

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

*   A list item with a code block:

        <code goes here>

### Code Blocks

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both `<pre>` and `<code>` tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab.

This is a normal paragraph:

    This is a code block.

Here is an example of AppleScript:

    tell application "Foo"
        beep
    end tell

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (`&`) and angle brackets (`<` and `>`)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.

```
tell application "Foo"
    beep
end tell
```

## Span Elements

### Links

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

This is [an example](http://example.com/) inline link.

[This link](http://example.net/) has no title attribute.

### Emphasis

Markdown treats asterisks (`*`) and underscores (`_`) as indicators of
emphasis. Text wrapped with one `*` or `_` will be wrapped with an
HTML `<em>` tag; double `*`'s or `_`'s will be wrapped with an HTML
`<strong>` tag. E.g., this input:

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

### Code

To indicate a span of code, wrap it with backtick quotes (`` ` ``).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

Use the `printf()` function.
