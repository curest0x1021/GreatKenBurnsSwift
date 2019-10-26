# Ken Burns

![burns](KenBurns.gif)

A simple yet configurable Ken Burns effect using a single image looping over itself. Really draws the user’s attention, much more so than a static image.

### Usage

`KenBurns` is written in Swift, but you can use `KenBurnsImageView` from Swift or Objective-C.  Examples are in Swift 3.0:

```swift
func newKenBurnsImageView(url: URL) -> KenBurnsImageView {
    let ken = KenBurnsImageView()
    ken.fetchImage(url: url, placeholder: UIImage(named: "placeholder"))
    ken.startAnimating()
    return ken
}

func stop(ken: KenBurnsImageView) {
    ken.stopAnimating()
}

func pause(ken: KenBurnsImageView) {
    ken.pause()
}

func resume(ken: KenBurnsImageView) {
    ken.resume()
}
```

You can also initialize with a direct `UIImage` rather than a URL, and there are some paramaters you can set to configure the appearance:

```swift
func newKenBurnsImageView(image: UIImage) -> KenBurnsImageView {
    let ken = KenBurnsImageView()
    ken.setImage(image: image)
    ken.zoomIntensity = 1.5
    ken.setDuration(min: 5, max: 13)
    ken.startAnimating()
    return ken
}
```

Due to unfortunate circumstances, Calm has no direct affiliation with [Ken Burns](https://en.wikipedia.org/wiki/Ken_Burns) himself 😞
