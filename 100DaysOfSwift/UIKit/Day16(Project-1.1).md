# Day16 [Project]

## Begin to the IOS 

## Subjects

- Project Setup for UIKit
- Listing images with FileManager
- Designing our interface

## FileManager

A piece of code that tells where the contents are, although I find it very interesting

```swift
let fm = FileManager.default
let path = Bundle.main.resourcePath!
let items = try! fm.contentsOfDirectory(atPath: path)
```
Of course, we must find the truth of these contents and transfer them to our collection list.

```swift 
    var pictures = [String]()
```

```swift
        for item in items {
            if item.hasPrefix("nssl") {
                // this is a picture to load!
                pictures.append(item)
            }
        }
```

## User Interface Design 

class ViewController: UIViewController to:  class ViewController: UITableViewController

```swift 
// We say how many rows the UITableViewController we created on the Storyboard has.
    override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return pictures.count
    }
    // Here we create  the text of the cells and send our cells to our table. And we do this by row index.
    override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
       let cell = tableView.dequeueReusableCell(withIdentifier: "Picture", for: indexPath)
        cell.textLabel?.text = pictures[indexPath.row]
        return cell
    }
```
## Result 
<img
    src="![UserInterface_Design](https://github.com/Fred052/100DaysOfSwift/assets/125974539/ff8fa1c4-7db6-461d-acb1-1bbe6e3d11f0)
" width=355>




