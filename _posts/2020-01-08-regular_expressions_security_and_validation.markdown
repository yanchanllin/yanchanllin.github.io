---
layout: post
title:      "Regular expressions security & validation"
date:       2020-01-09 01:50:09 +0000
permalink:  regular_expressions_security_and_validation
---

I learned the basics of writing Regular Expressions in Ruby long time ago, it's a review for me to use regular expressions with Regex.

The scan method returns an array of all items in your string that match a given Regular Expression. For example:
    
```
"The rain in Spain lies mainly in the plain".scan(/\w+ain/)
=> ["rain", "Spain", "main", "plain"]
```

The match method returns the first item in your string that matches a given Regular Expression as a MatchData object. For example:

```
"The rain in Spain lies mainly in the plain".match(/\w+ain/)
=> #<MatchData "rain"> 
 
"The rain in Spain lies mainly in the plain".match(/France/)
=> nil
```

Reminder note: https is secured communication protocol is encrypted by transport layer security(TLS) or secure socket layer(SSL). Https is an extension of (HTTP)hypertext transfer protocol. 


