# Day22

## Begin to the IOS

## Subjects

- UIActivityViewController explained
- Wrap Up (Challenges)

## UIActivityViewController explained

Actually, that's all the codes that affect this subject

```swift
 let vc = UIActivityViewController(activityItems: [image], applicationActivities: [])
        vc.popoverPresentationController?.barButtonItem = navigationItem.rightBarButtonItem
        
        present(vc, animated: true)
```

But besides that, there is a navigation button that we run these codes and we just learned.

```swift
 navigationItem.rightBarButtonItem = UIBarButtonItem(barButtonSystemItem: .action, target: self, action: #selector(shareTapped))
```

And of course our sample of data we get to be able to import and save the pictures.

```swift
guard let image = imageView.image?.jpegData(compressionQuality: 0.8) else
       {
           print("No image found")
           return
       }
```

