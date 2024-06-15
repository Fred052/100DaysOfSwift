#  Day17

## Begin to the IOS

## Subjects

- Building a Detail Screen
- Loading image with UIImage
- Image and Navigation Properties

## Building a Detail Screen

I created a new Cocoa touch class and bound my storyBoard page with this class

```swift

import UIKit

class DetailViewController: UIViewController {

    @IBOutlet var imageView: UIImageView!
    var selectedImage: String?
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        title = selectedImage
        navigationItem.largeTitleDisplayMode = .never

        if let imageToLoad = selectedImage {
            imageView.image = UIImage(named: imageToLoad)
        }
    }
    override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        navigationController?.hidesBarsOnTap = true
    }
    
    override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        navigationController?.hidesBarsOnTap = false
    }
}
```
## Loading image with UIImage 

I sent the image names to the Cocoa touch class I just created 

```swift
    override func tableView(_ tableView: UITableView, didSelectRowAt indexPath: IndexPath) {
        if let vc = storyboard?.instantiateViewController(withIdentifier: "Detail") as? DetailViewController {
            vc.selectedImage = pictures[indexPath.row]
            navigationController?.pushViewController(vc, animated: true)
        }
    }
```

```swift
        if let imageToLoad = selectedImage {
            imageView.image = UIImage(named: imageToLoad)
        }
```

## Image and Navigation Properties

```swift
    override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        navigationController?.hidesBarsOnTap = true
    }
    
    override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        navigationController?.hidesBarsOnTap = false
    }
```

```swift
        navigationItem.largeTitleDisplayMode = .never
```

```swift
        title = "Storm Viewer"
        navigationController?.navigationBar.prefersLargeTitles = true
```

## Result

![Simulator Screenshot](https://github.com/Fred052/100DaysOfSwift/raw/main/images/Simulator%20Screenshot%20-%20iPhone%2015%20Pro%20-%202024-06-15%20at%2014.52.27.png)



/Users/ferid.suleymanzade05icloud.com/Desktop/Simulator Screenshot - iPhone 15 Pro - 2024-06-15 at 14.52.17.png


/Users/ferid.suleymanzade05icloud.com/Desktop/Simulator Screenshot - iPhone 15 Pro - 2024-06-15 at 14.52.19.png
