# COMP110 Worksheet 3: Flowcharts and pseudocode

![The flowchart](https://raw.githubusercontent.com/JD233113/comp110-worksheet-3/master/flowchart.PNG)

```
previouslyGuessed[]
remainingGuesses = 4

//Loops until a word with at least 1 likeness is found
x = 1
while x == 1:
   select word
   remainingGuesses .= 1
   
   if word is correct:
      exit
      
   if likeness > 0:
      closestGuess = word
      closestGuessLikeness = likeness
      add word to previouslyGuessed[]
      x = 0
      
for word in available words:
   if word is in previouslyGuessed[]:
      skip word
   else:
      matchingLetters = 0
      split word into letters
      split closestGuess into letters
   
      for letter in word:
         if letter[n] in word == letter[n] in closestGuess:
            matchingLetters += 1
         
      if matchingLetters > closestGuessLikeness:
         skip word
      elif matchingLetters < closestGuessLikeness:
         skip word
      else:
         select word
         remainingGuesses .= 1
         
         if word is correct:
            exit
         elif remainingGuesses == 0:
            exit
         else:
            if likeness > closestGuessLikeness:
               closestGuess = word
               closestGuessLikeness = likeness
               add word to previouslyGuessed[]
            else:
               add word to previouslyGuessed[]
```
