# Capturing User Email and User Name Across Lines

This regular expression is used to capture **two related fields that may appear on separate lines** in a JSON response, such as XDR organization or identity payloads.

```regex
"user-email":\s*"([^"]*)",[\s\S]*?"user-name":\s*"([^"]*)"
```

# Purpose

The goal of this pattern is to:

- Find a "user-email" field

- Capture its value

- Continue scanning forward across line breaks

- Find the next "user-name" field

- Capture its value

This is useful when:

- JSON fields are not guaranteed to be on the same line

- There may be other fields or whitespace between them

- You want to extract logically related identity attributes from API responses
                                                    
