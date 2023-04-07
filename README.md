# Lily On Rockets 👩‍🚀🔛🚀


LilyOnRockets is a pseudo-code format that uses Python-like indentation, camelCase syntax, and emojis as keywords. Keywords still work as expected though. Scopes{} are optional and not used by default.

It is influenced by Kotlin, JavaScript, TypeScript, Dart, Java, Python and Rust and intends to be used to convert pseudo-code to viable code on these languages. The idea is you prototype your solution using Lily and then transpile (using GPT4 for example) lily code to your desired output. 

This file also serves as formatting/indentation style reference for humans and AI.

Features
- 🎭 Define traits and replaces 'implements' keyword
- 🏷️ Define enums
- 🧩 Define classes and replaces 'extends' keyword
- 📥 Works as assign operator "="
- 🗿 Immutable variables
- 📦 Mutable variables
- 🚀 Functions with or without arguments
- ↩️ Same as "return" keyword
- 🔐 Immutable collections prefix
- 📋 Define lists
- 🔑 Define maps
- 🃏 Define sets
- 🚦 Define observable variables
- 🧐 Define observer variable or function
- ➡️ “then” keyword in conditional statements
- 🪵 Applies (toString and prints to log) on every object and primitive found on this log line
- ❓ Works as a Kotlin when (condition) {} block, but simpler: condition ❓

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
    🗿 cat	📥 Cat("Whiskers", 3, "Jane")   
    🗿 horse	.saddleSetup..sound("Neigh")
    🗿 cat	.purr(mutableNumber)..sound("Meow")
    
    
    📋 list		📥 🔐	[1, 2, 3, 4]
    🔑 map		📥	{ "key1" to "value1", "key2" to "value2" }
    🃏 set		📥 🔐	{ "item1", "item2", "item3" }
    
    
    🪵 list, map, set
    
    
    // ternary is preferable over if else
    // booleans are simplified to either ❌false or ✅true primitives and corresponding emoji
    📦 isBalenciaga ↩️ isH&M or isC&A ❓ ❌ : ✅
    
    
    myAge ❓
        > 18		➡️ show "You are an adult"
        myAge > 0	➡️ show "You are a minor"
        else		➡️ show "Invalid age"
    
    
    someValue ❓
        1		➡️ show "Value is 1"
        2		➡️ show "Value is 2"
        3		➡️ show "Value is 3"
        else		➡️ show "Value is something else"
    
    
    repeat mutableNumber 🔁 show "Meow number $it"
      
```

# Examples:
```prompt
Use the above pseudo-model to create a cute cat fetch and present app
```
```lily

🏷️ API_URL
    📥 "https://api.thecatapi.com/v1/images/search"

🧩 CatImage(Text url, Text id)
    📦 url 📥 url
    📦 id  📥 id

🚀 fetchCatImage() 🚧
    📦 response 📥 🚧 fetch(API_URL)
    ⏰ 1000
    📩 response.json()

🚀 displayCatImage(CatImage catImage) 🚧
    🪵 "🐱 Cute Cat Image 🐱"
    🪵 "ID: ${catImage.id}"
    🪵 "URL: ${catImage.url}"

🚀 main() 🚧
    📦 catImageData 📥 await fetchCatImage()
    🗿 catImage 📥 CatImage(catImageData[0].url, catImageData[0].id)
    displayCatImage(catImage)

```
