# SwiftUI practice creating a resume
They say the best way to learn something is actually doing it, by getting your hands dirty.<br>
So, let's build a simple static resume to put in practice all the learnt things so far.<br>
* VStack, HStack, ZStack
* Spacer
* Images
* Sizes
* Offset x,y
* Shapes
* Alignment
* Padding
* etc.
  
![Screenshot 2024-03-03 at 6 49 30 AM](https://github.com/danielurra/Swift-UI-practice-creating-a-resume/assets/51704179/9e333b3a-fe45-4777-94e7-a06dc3790d82)<br>
## Grab the code
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack(alignment: .leading, spacing: 0) {
            HStack {
                Image("NickSquare")
                    .resizable()
                    .aspectRatio(contentMode: .fit)
                    .clipShape(Circle())
                    .frame(height: 100)
                    .background {
                        Circle()
                            .foregroundColor(.blue)
                            .offset(x: 10, y: 10)
                    }
                    .background {
                        Circle()
                            .foregroundColor(.red)
                            .offset(x: -10, y: 10)
                    }
                    .background {
                        Circle()
                            .foregroundColor(.green)
                            .offset(x: 0, y: -10)
                    }
                    .padding(.horizontal, 10)
                
                VStack(alignment: .leading) {
                    Text("Nick Walter")
                        .font(.largeTitle)
                    Text("Programmer")
                        .foregroundStyle(.secondary)
                }
            }
            
            Spacer()
            Group {
                Text("Skills")
                    .font(.title)
                Rectangle()
                    .frame(height: 1)
                    .padding(.bottom, 8)
                
                HStack {
                    Text("App Developer")
                        .bold()
                    Spacer()
                    Text("2 Apps in Store")
                }
                HStack {
                    Text("Swift")
                        .foregroundStyle(.secondary)
                    Spacer()
                }
                HStack {
                    Text("We Developer")
                        .bold()
                    Spacer()
                    Text("Personal Website")
                }
                HStack {
                    Text("Python/Django")
                        .foregroundStyle(.secondary)
                    Spacer()
                }
            }
            Spacer()
            
            Group {
                Text("Work Experience")
                    .font(.title)
                Rectangle()
                    .frame(height: 1)
                    .padding(.bottom)
                HStack {
                    Text("ZappyCode")
                        .bold()
                    Spacer()
                    Text("2014-Present")
                }
                HStack {
                    Text("Commander-in-Chief")
                        .foregroundStyle(.secondary)
                    Spacer()
                }
                HStack {
                    Text("Taco Bell")
                        .bold()
                    Spacer()
                    Text("2022")
                }
                HStack {
                    Text("Service Champion")
                        .foregroundStyle(.secondary)
                    Spacer()
                }
            }
            
            Spacer()
            Group {
                Text("Education")
                    .font(.title)
                Rectangle()
                    .frame(height: 1)
                    .padding(.bottom, 8)
                
                HStack {
                    Text("Bachelor's Degree")
                        .bold()
                    Spacer()
                    Text("2007-2014")
                }
                HStack {
                    Text("Information Systems")
                        .foregroundStyle(.secondary)
                    Spacer()
                    Text("BYU")
                }
            }
            Spacer()
            
            Group {
                Text("Interests")
                    .font(.title)
                Rectangle()
                    .frame(height: 1)
                    .padding(.bottom)
                
                HStack {
                    Spacer()
                    VStack {
                        Text("🏊‍♀️")
                            .font(.system(size: 70))
                        Text("Swimming")
                            .bold()
                    }
                    Spacer()
                    VStack {
                        Text("🎮")
                            .font(.system(size: 70))
                        Text("Videogames")
                            .bold()
                    }
                    Spacer()
                    VStack {
                        Text("💻")
                            .font(.system(size: 70))
                        Text("Coding")
                            .bold()
                    }
                    Spacer()
                }
            }
        }
        .padding()
    }
}

#Preview {
    ContentView()
}

```

