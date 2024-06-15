# Day 18

## Begin to the IOS

## Subjects
- Wrap up
- Challenge

## Challenge

In your main table view, show the image names in sorted order, so “nssl0033.jpg” comes before “nssl0034.jpg”.

```swift
        pictures.sort()  //This is easy because swift provides a list sorting feature
```

Rather than show image names in the detail title bar, show “Picture X of Y”,
where Y is the total number of images and X is the selected picture’s position in the array. Make sure you count from 1 rather than 0.

```swift
// I added that on my DetailViewController
  var selectedPictureNumber = 0
    var totalPictures = 0

// And this is how I set the text of my detail view

 title = "Picture \(totalPictures + 1) of \(selectedPictureNumber) "
```

```swift
  override func tableView(_ tableView: UITableView, didSelectRowAt indexPath: IndexPath) {
        if let vc = storyboard?.instantiateViewController(withIdentifier: "Detail") as? DetailViewController {
            vc.selectedImage = pictures[indexPath.row]
            navigationController?.pushViewController(vc, animated: true)

 // Here I have sent the number of elements of the list and the index of the selected image to the other page.
            vc.selectedPictureNumber = self.pictures.count
            vc.totalPictures = indexPath.row
        }
    }
```


