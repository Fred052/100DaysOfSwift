# Day20

## Begin to the IOS

## Subjects

- Guess which flag: random numbers
- From outlets to actions: creating an IBAction

## Guess which flag: random numbers

Let's shuffle our list and set a correct answer after each shuffle.

```swift
 var correctAnswer = 0

  countries.shuffle()
        correctAnswer = Int.random(in: 0...2)
```

Sync the title to the correct answer

```swift
title = countries[correctAnswer].uppercased()
```

## From outlets to actions: creating an IBAction

