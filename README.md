# Bible-JSON
The Bible in JSON format.

# Structure:
This is what it would look like if you were to open up `./JSON/Psalms/3.json`.
```json
{
    "info": "(A Psalm of David, when he fled from Absalom his son.)",
    "verses": [  
        {
            "book_id": "PSA",
            "book_name": "Psalms",
            "chapter": 3,
            "verse": 1,
            "text": "Psalms 3:1 - LORD, how are they increased that trouble me! many are they that rise up against me."
        },
        ...
    ]
}
```
`info` is a string of additional information about the chapter, such as "A Psalm of David" above a Psalm. I don't believe any chapters outside of the Psalms use this but I may be wrong.

`verses` is an object array. Inside `verses` are object with these:

- `book_id` is a string which is a short 3-letter abbreviation of the the chapter's book's name. This is good for calling an API maybe?
- `book_name` is a sting containing the name of the book of which this chapter is from.
- `chapter` is an integer which is also the chapter's number.
- `verse` is an integer which is the verse number.
- `text` is a string containing the text of the verse. You will find `<span style="color:red;">` and `</span>` wrapping around Jesus' words as well as `<em>` and `</em>` around italicized words.