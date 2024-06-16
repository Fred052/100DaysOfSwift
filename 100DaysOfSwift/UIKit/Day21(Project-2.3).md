## Day21

## Begin to the IOS

## Subjects

- Wrap up
-  Challenge

## Challenge

Try showing the player’s score in the navigation bar, alongside the flag to guess.

```swift
   title = countries[correctAnswer].uppercased() + "     Current Score:" + String(score)
```

Keep track of how many questions have been asked, and show one final alert controller after they have answered 10. This should show their final score.

```swift
var howManyQuestion = 0
```

```swift
func askQuestion(action: UIAlertAction! = nil) {
        howManyQuestion += 1
        }
```

When someone chooses the wrong flag, tell them their mistake in your alert message – something like “Wrong! That’s the flag of France,” for example.

```swift
title = "Wrong choice\n" + "That's the flag of: \(countries[sender.tag])"
            score -= 1
```
