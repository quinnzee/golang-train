# golang-train
Session1
in this session, we learn about basic language from GOLANG


    basic knowledge used on terminal :
    -cd.. (going back to previous folder)

    -go mod init <nama-project> (used for made Go Mofules or Initialising a project)
    -go run (used for execution a files)
    -go build (used for making a new file on the same folder)
    -go get (used for downloading new package)

    basic knowledge :
    -fmt.Print = (basic output)
    -fmt.Printf = (the output is depends from flag that we used and have the same function with Println but need extra on naming structure; ex : %T (to knew data types from variable), %s (mostly used on string), %d (used to formatting interger data type from 0-9)) (extra information = https://pkg.go.dev/fmt) (and add \n at the end to make new line(like Println))
    -fmt.Println = (having the same function with Printf but more neat)

    1. Variables (var)
        Naming : use camelCase (ex: favoriteColor ="blue")
        -Variable WITH data type : (tbh im not sure how to explain the variable with data type, but its more like more clearly because after u use var, you add the specific data types on it; ex : <var name string = "Golang">)

        -Variable WITHOUT data type : (we can make some variables without adding the data types, and its called Type Inference that the system from golang will choose on its own the data types based from the value that we add before on variable)
            ex : 
            var name = "Golang"
            var age = 25

            fmt.Printf("%T, %T", name, age)
            (the output will shown as <string, int>)

        -Variable WITHOUT data types (Short Declaration) (:=)
            we can make variables using Short Declaration (:=) without using var 
            ex :
            name := "Golang"
            age := 23

            fmt.Printf("%T, %T", name, age)
            (the output will shown as Golang 23)

        -Multiple Variables Declaration : (we can make more than one variables in one line)
        
        -Underscore Variable : (well basicly adding underscore (_)just to avoid error from useless variables)

    2. Data Types
        -Interger (int = number) : (interger is a non-decimal numeric data type in the GO Language)
        They are again arithmetic types and they represents a> interger types or b> floating point values throughout the program.
            -uint(8,16,32,64) : unsigned 8/16/32/64-bit intergers (0 to xxx)
            -int(8,16,32,64) : signed 8/16/32/64-bit intergers (-xxx to xxx)

        -Float  (the value of an n-bit interger is n bits and is represented using two's complement arithmetic operations.)
            -float32 : IEEE-754 32-bit floating-point numbers
            -float64 : IEEE-754 64-bit floating-point numbers
            -complex64 : complex numbers with float32 real and imaginary parts
            -complex128 : complex numbers with float64 real and imaginary parts

            -verb%f : used to format decimal numbers to 6 digit
            -verb%.nf : used to reduce the decimal numbers depends on 'n'
        (tbh i still dont get the float, maybe used for higher function?)

        -Bool (in Go, bool is the single type representing Boolean Values. it is widely used in logical and conditional operations. it can accept only two values wich are "true" or "false")

        -String (a string type represents the set of string values. its value is a sequence of bytes. strings are immutable types that is once created, it is not possible to change the conttents of a string. the predeclared string type is string.)

        -Nil & Zero Value
            -Zero value from string is ""
            -Zero value from bool is false
            -Zero value from non-decimal numeric is 0
            -Zero value from decimal numeric is 0.0
    
    3. Constants & Operators
        -Constant (conts) on Go language means the value is absolute. for example : Phi, gravity, speed of light, ect.

        -Operators (Arithmetic Operators) basicly using basic math inside the codes.
            - + (adds two operands)
            - - (substracts second operand from the first)
            - * (multiples both operands)
            - / (divides the numerator by the denominator)
            - % (modulus operator; gives the remainder after an interger division)
            - ++ (increment operator. it increases the interger value by one)
            - -- (decrement operator. it decreases the interger value by one)

        -Operators (Relational Operators) we can use relational operators / comparison operators to check the truth of a condition which will produce a value with boolean data type.
            - == (it checks if the values of two operands are equal or not; if yes, the condition becomes true)
            - != (it checks if the values of two operands are equal or not; if the values are not equal, then the condition becomes true)
            - > (it checks if the value of left operands is less than the value of the right operand; if yes, the condition becomes true)
            - < (it checks if the value if the left operands is less than the value of the right operand; if yes, the condition becomes true)
            - >= (it checks if the value of the left operand is greater than or equal to the value of the right operand; if yes, the condition becomes true)
            - <= (it checks if the valur of left operand is less than or equal to the value of right operand, if yes, the condition becomes true)
        
        -Operators (Logical Operators) the logical operators perform the logical operation on Boolean values. these are basically used to check more than one condition together
            The following table shows all the logical operators supported by Go Language. Assume variable A holds true and variable B holds false, then-
            - && (called logical AND operator. if both the operands are false, then the condition becomes false)
            - || (called logical OR operator. if any of the two operands is true, then the condition becomes true)
            - ! (called logical NOT operator. use to reverses the logical state of its operand. if a condition is true, then logical NOT operator will make it false)

Session 2
in this session we learn about scalable web service with Golang


    1. Conditions
    Conditionals in programming can be used to control the flow of a program. In Go language, there are 2 conditionals that we can used, 'if else' and 'switch' for example :
    - if statement (and if statement consists of a boolean expression followed by one or more statements)
    - if.. else statement (an if statement can be followed by an optional else statement, which executes when the boolean expression is false)
    - nested if statements (you can use one if or else if statements inside another if or else if statements)
    - switch statement (a switch statement allows a variable to be tested for equality againts a list of values)
    - select statement (a select statement is similar to switch statement with different that case statements refers to channel communications)

        -Conditions (Temporary variable) in Go language, we can create a variable where the variable can only be accessed and used in the block scope of a conditional.

        -Switch (a switch statement allows a variable to be tested for equality against a list of value. Each value is called a case, and the variable being switched on is checked for each Switch case)
            -basic switch
            -switch with relational operators
            -switch fallthrough keyword
        
        -Nested (nested conditionals are a conditional process that inside there is a return conditional process. we can use IF, ELSE IF, ELSE, SWITCH or combine all of them)

    2.Looping (Looping or repitition is a repetitive process where the process will stop if it meets a condition. the Go language only has one loop, )
        -first way of looping (the loop will work as long as the cariable i has a value less than 3) it should be noted here that we must not forget to add the variable i as in the 'try on code' where i++ is the same as i = i+1. if the variable i is not added, it will cause an infinite loop or a repeating process that will not stop.

        -second way of looping (the second way to do looping in Go language is by inserting conditionals like in looping using the while keyword)

        -third way of looping (the third way to loop in Go language is to loop without giving any conditions using break keyword)

        -break and continue keywords (after we tried the break keyword to stop the looping process, now we use continue keyword to continue the process)

        -nested (nested looping is a looping process that has another looping inside the looping)

        -label (in nested loops, the break and continue keywords will only apply to the loop block where they are used. there is a way for these two keywords to be directed to the outermost loop or a specific loop, namely by utilizing the labeling technique)

    3. Array 
    Array in Go language is a data type to store a collection of data. The data that we store in an array in Go language must have the same data type, unless we store it as an empty interfave. Array in the Go language have a fixed-length nature or have a fixed length that we must determine from the start when we create the array. We can create an array in 2 ways, namely by declaring it first without giving it any value and we can also declare it and immediately initialize it by giving it a value.
        
        -modify element through index(we can also modify the elements contained in an array by accessing their index)

        -loop through elements(there are 2 ways of writing so that we can do looping to access the elements contained in an array)
            -first way is using range loop. by using range loop, we can easily access all elements in an array and also get their index at the same time.
            -the second way is we can use regular looping and we need to use the help of the len function to get the length of the array by writing len(<array name>).
        
        -multidimensional array(we can also create a multidimensional array which means there is an array within an array. the array contained by the balances variable is a multidimensional array.)
    
    4. Slice
    Slice is a data type that is similar to the array data type, which also has the function of storing one or more data. However, the slice and array data types have different properties. Slice does not have a fixed-length property, which means that the length of the slice is not fixed so that we can freely determine the length of the slice. Slice is included in the reference type category where if we copy a slice, and we change the elements of what we copied, then the original slice will also be changed.

        - Slice (make function) we can also create a slice by using the make function.

        - Slice (append function) if we want to add an element to the slice of the variable fruits, we can do by accessing its index. If you want it easier, then we can use the append function. The append function will return the value of slice that it adds, therefore we must store the append function into variable.
            - SLice (append function with ellipsis) if we want to insert all the elements in an array into another array, then we can use the ellipsis (...)
        
        - Slice (copy function) we can also use the copy function to copy all elements in a slice. it should be noted here that when we try to copy a slice into another slice, all elements in the other slice will be replaced by the copied elements.

        - Slice (Slicing) there is another way that we can get elements from a slice and we can also fetermine the element from which index we want to get. The way is by using slicing. The way of writing in doing slicing is same as [start:stop]. Start is the same as the beginning of the index we want to access and stop means the end index. 
            - [x:x] to get element from index x to x
            - [x:] to get element from index x to end
            - [:x] to get element from index first to x
            - [:] to get all of the element

        - Slice (Combining slicing and append) we can also combine the append function with slicing. 
        












        

