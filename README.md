# KrystalZhang-Handheld Business Watcher News App
A neat-designed iOS Newsfeed application which contains richful most-recent news about business stocks, built from scratch in UIkit, incorporated with newapi.org APIs to a custom UI and cache images and CGRect.
## ***[Copyright and Commercial Use Disclaimer](https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/README.md#please-carefully-read-licensemd-about-the-open-source-restrictions-and-the-personal-use-policy-of-this-project-under-gpl-30-license-any-commericial-uses-on-this-project-by-other-than-the-owner-krystalzhang612-or-the-authorized-users-and-organizations-including-unauthorized-modifications-forks-pull-requests-and-other-commercial-related-uses-will-be-subjected-to-copyright-violation-with-sebsequent-legal-concerns)***

⏬

### ***Please carefully read [LICENSE.md](https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/LICENSE) about the Open Source restrictions and the personal use policy of this project under [GPL-3.0 license](https://www.gnu.org/licenses/gpl-3.0.en.html), any commericial uses on this project by other than the owner [@KrystalZhang612](https://github.com/KrystalZhang612) or the authorized users and organizations, including unauthorized modifications, forks, pull requests, and other commercial-related uses will be subjected to copyright violation with sebsequent legal concerns.***

## Handheld Business Watcher News App Overview:
<p align = "center">
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview1.png" width = "401.8181" height ="839.090"/>&nbsp; 
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview2.png" width = "380" height ="841.8181"/> 
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview3.png" width = "380" height ="841.8181"/>&nbsp;
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview4.png" width = "380" height ="841.8181"/>
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview5.png" width = "380" height ="841.8181"/>&nbsp;
        <img src ="https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld%20Business%20Watcher%20News%20App%20overview%206.png" width = "380" height ="841.8181"/>       
</p> 

# Build

[Method to Run & Test the Project Locally](https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/README.md#method-to-run--test-the-project-locally)<br/>
[Prerequisites & Setups](https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/README.md#prerequisites--setups)<br/> 
[Debugging&Troubleshooting]()<br/> 
[Synchronous Developing Notes]()<br/> 
[Testing Result]()<br/> 

# Contribution
[Author]()

# Compatibility
|   OS             | Supported          |
| -------          | ------------------ |
| iOS 10-iOS 15.5  | :white_check_mark: |
| iOS 16+          | :x:                |
| macOS Mojave     | ✅                 |
| macOS Monterey   | ✅                 |

# Method to Run & Test the Project Locally
### Download the entire project to local directory
### Xcode must be 13.4 and higher versions with all Xcode dependencies updated.
### Compatible with `iOS 10-iOS 15.5` 
### Not compatiable with `iOS 16+`
### Run the project, choose Simulator `iPhone 12 Pro Max iOS 14.4` for best compatiability.

# 🛠️ Developing Languages, Tools, and Techniques Needed
[Xcode 13.4.1 iOS 10-15.5 (iOS 16 causes Assertion Errors)](https://developer.apple.com/documentation/xcode-release-notes/xcode-13_4_1-release-notes)<br/>
Best testing simulator version to avoid errors: `iPhone12 Pro Max iOS 14.4`<br/>
[News API](https://newsapi.org/docs/get-started#search)<br/> 
[SwiftUI](https://developer.apple.com/xcode/swiftui/)<br/> 
[SafariServices Documentation](https://developer.apple.com/documentation/safariservices Swift 5 https://developer.apple.com/swift/)<br/>
`Note: Xcode project renaming rule: change info.plist File in Build Settings.`<br/>
<div>
        <img src ="https://github.com/devicons/devicon/blob/master/icons/xcode/xcode-plain.svg" title="Xcode" alt ="Xcode" width = "60" height= "60"/>&nbsp; 
        <img src = "https://github.com/devicons/devicon/blob/master/icons/swift/swift-original.svg" title = "Swift 5" alt = "Swift 5" width = "60" height= "60"/>&nbsp; 
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-RepliFlix/blob/main/swift%20ui%20symbol%20logo.png" title = "SwiftUI" alt= "SwiftUI" width = "60" height= "60"/>&nbsp; 
        <img src = "https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/news%20api%20logo.png" title = "NewsAPI" alt = "NewsAPI" width = "210" height = "60"/>&nbsp; 
</div>

# Prerequisites & Setups
Obtain an API url from newsapi.org for the most-recent TechCrunch news.<br/> 
Create a new object to call APIs [APICaller.swift](https://github.com/KrystalZhang612/KrystalZhang-Handheld-Business-Watcher-News-App/blob/main/Handheld-Business-Watcher-News-App/APICaller.swift):<br/>
Handle potential errors with completion method, resume task:
```Swift
  public func getTopStories(completion: @escaping{...) {
...
  
if let error = error{
    completion(.failure(error))
}
else if let data = data {
    do {
        let result = try JSONDecoder().decode(String.self,
} catch {
        completion(.failure(error))
    }
   task.resume() 
```










