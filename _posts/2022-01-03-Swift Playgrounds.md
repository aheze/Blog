---
title: Swift Playgrounds
author:
  name: Andrew Zheng
  link: https://github.com/aheze
date: 2022-01-03 20:17 -0800
categories: [Getting Started]
tags: [Swift Playgrounds, Swift, SwiftUI, iOS]
---

### Overview

Swift Playgrounds is a code editor that runs on iPad [(download)](https://apps.apple.com/us/app/swift-playgrounds/id908519492). So it's an app that lets you make apps.

![](/assets/SwiftPlaygrounds.webp){: w="100" }
*The app*

Open it, and select a project (or create a new one with the plus button). The interface is split into 3 parts:

- **Left:** The sidebar, which shows all your files
- **Center:** The place where you write code
- **Right:** The app preview, which shows the result of your code

![](/assets/playgroundsUI.PNG)

At the top, there's some more buttons:

1. Return to the app gallery
2. Hide/show the sidebar
3. Create a new file
4. Run your code in a separate window
5. Browse the presets library
6. More options
7. Expand the preview to full-screen
8. Hide the preview

![](/assets/playgroundsTopBar.png)

When you write code, the app preview will automatically update. If there's a compile error, another button will appear at the top that lists out the errors.

In a brand-new project, there will be 2 files on the left sidebar: `ContentView` and `MyApp`. The file names don't matter and are only used for organizing, unlike Java, which requires it to be the same as the class name.

## MyApp
`MyApp` contains the main starting point of your app. You can rename this to whatever you want -- as long as it has the `@main` attribute, it will be the starting point.

```swift
import SwiftUI

@main /// <-- indicates that this is the starting point of your app.
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView() /// This is what Swift Playgrounds will display.
        }
    }
}
```

For now, ignore `struct`, `some Scene`, `WindowGroup`, and all the other keywords. Just know that your SwiftUI goes inside `WindowGroup { }`.

## ContentView
Your SwiftUI code goes here. Here's the default, placeholder code:

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Image(systemName: "globe")
                .imageScale(.large)
                .foregroundColor(.accentColor)
            Text("Hello, world!")
        }
    }
}
```

We'll go over this in the next section, but for now, notice how the result appears on the right:

![](/assets/PlaygroundsResult.png){: .shadow }


That's pretty much it! Swift Playgrounds is very modern and abstracts away all the redundant steps.