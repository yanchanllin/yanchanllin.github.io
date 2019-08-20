---
layout: post
title:      "Interesting Regax"
date:       2017-11-05 01:50:39 -0400
permalink:  interesting_regax
---


I just learned Regax and Rubular, and found Regax interesting. It is like a .collect iterater collects all the data, word,letter,and numbers etc. then return what we looking for example: when we want to find any words start with a vowel:aeiou 

    `def starts_with_a_vowel?(word)
         if word.match(/^[aeiouAEIOU]+\w/)
          then
           return true
        else
          return false
         end
      end `

    `def words_starting_with_un_and_ending_with_ing(text)
         text.scan(/un+\w+ing\b/)
       end`

    `def words_five_letters_long(text)                     
		    text.scan(/\b\w{5}\b/)
		  end`

      `def first_word_capitalized_and_ends_with_punctuation?(text)
            if text.match(/^[A-Z].+[\.!?]$/)
              then
                return true
           else
              return false
           end
       end`

     `def valid_phone_number?(phone)
          if phone.match(/([0-9] *?){10}|(\([0-9]{3}\)(([0-9]{3}-[0-9]{4})|[0-9]{7})\b)/)
            then
             return true
           else
              return false
          end
      end`



