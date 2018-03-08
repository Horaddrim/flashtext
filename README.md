
# flashtext




## What's it
------------
Flashtext is a simple and fast keyword extract tool in go.

It was inspired by the paper [Medium](https://medium.freecodecamp.org/regex-was-taking-5-days-flashtext-does-it-in-15-minutes-55f04411025f)
, here is the python implement:   [Link](https://github.com/vi3k6i5/flashtext>)


-----------------------------------------------------------------------------------------------------------------------------
## Installation

    $ go get github.com/Horaddrim/flashtext


-----------------------------------------------------------------------------------------------------------------------------
## Usage
Extract keywords
```
    package main

    import (
        "fmt"

        "github.com/Horaddrim/flashtext"
    )

    func main() {
        processor := flashtext.NewKeywordProcessor()
        // set the caseSensitive to false
        processor.SetConfig(false)

        processor.AddKeyword("Sao Paulo", "Brazil")
        processor.AddKeywordAndName("java", "Java")
        // set to find the longest keywords
        res := processor.Extracts("I worked with java, at Sao Paulo, Brazil", true)
        fmt.Printf("res => %#v\n", res)
    }
```

To Remove keywords

    processor.RemoveKeywords("Brazil")
-----------------------------------------------------------------------------------------------------------------------------
## Test

    $ go test


