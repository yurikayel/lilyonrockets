Lily On Rockets 👩‍🚀🔛🚀


LilyOnRockets is a programming language that uses Python-like indentation, camelCase syntax, and emojis as keywords. Scopes ({}) are optional and not used by default. It is influenced by Kotlin, JavaScript, TypeScript, Dart, Java, Python, and Rust.

This file also serves as formatting/indentation style reference.

Features
- 🎭 Define traits and replaces 'implements' keyword
- 🏷️ Define enums
- 🧩 Define classes and replaces 'extends' keyword
- 📥 Use the 📥 emoji for type inference
- 🗿 Use the 🗿 emoji for immutable variables
- 📦 Use the 📦 emoji for mutable variables
- 🚀 Define functions with or without arguments
- ↩️ Use the ↩️ emoji for the return keyword
- 🔐 Use the 🔐 emoji to define immutable collections
- 📋 Define lists with the 📋 emoji
- 🔑 Define maps with the 🔑 emoji
- 🃏 Define sets with the 🃏 emoji
- 🚦 Define observable variables
- 🧐 Define observer variables
- ➡️ Use the ➡️ emoji for the “then” keyword in conditional statements
- 🪵 Applies (toString and prints to log) on every object and primitive found on this log line
- ❔ Works as a Kotlin when (condition) {} block, but simpler: condition ❔

```lily    
    🏷️ Color
    	    🟠 orange
    	    🟢 green
    	    🔵 blue
    	    🟣 purple
    	    🟤 brown


    🎭 Saddle
	        🚀 saddleSetup  ↩️ show "This is method X1"
	        🚀 ride         ↩️ show "You ride something..."
    
    🧩 Horse(Text name, Number age, Text owner)
    	🧩 Animal(name, age, owner)
        🎭 Saddle
        🎭 Jockey
          🚀 makeSound  ↩️ show "The horse makes a sound"
          🚀 ride       ↩️ show "🏇"
    
    🧩 Cat(Text name, Number age, Text owner)
        🧩 Animal(name, age, owner)
        🎭 Purr
          🚀 makeSound  ↩️ show "The horse makes a sound"
          🚀 purr       (Number intensity)
                        ↩️ show "$name is purring with intensity $intensity"
                          

    🗿 number         📥 42
    🗿 text           📥 "Hello, world!"
    📦 mutableNumber  📥 10
    
    
    🚀 noArg      ↩️ show "No-arg function has no argument list"
    🚀 add        (Number x, Number y)  ↩️ x + y
    🚀 greeting   (Text name)           ↩️ show "Hello, $name!"


    🚀 fetchData() 🚧
    	📦 response 📥 🚧 fetch("https://example.com/data")
    	⏰ 1000
    	📩 response.text()


    🚀 main() 🚧
    	📦 data 📥 await fetchData()
    	show data

    
    🗿 horse	📥 Horse("Bucephalus", 12, "Alexander the Great")
    🗿 cat		📥 Cat("Whiskers", 3, "Jane")   
    🗿 horse	.saddleSetup..sound("Neigh")
    🗿 cat		.purr(mutableNumber)..sound("Meow")
    
    
    📋 list		📥 🔐	[1, 2, 3, 4]
    🔑 map		📥		{ "key1" to "value1", "key2" to "value2" }
    🃏 set		📥 🔐	{ "item1", "item2", "item3" }
    
    
    🪵 list, map, set
    
    
    myAge ❔
        > 18		  	➡️ show "You are an adult"
        myAge > 0		➡️ show "You are a minor"
        else		  	➡️ show "Invalid age"
    
    
    someValue ❔
        1		  	➡️ show "Value is 1"
        2		  	➡️ show "Value is 2"
        3		  	➡️ show "Value is 3"
        else		➡️ show "Value is something else"
    
    repeat mutableNumber 🔁 show "Meow number $it"
      
