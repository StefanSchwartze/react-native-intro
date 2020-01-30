#### An introduction to
# React Native

Stefan Schwartze
---

## What is React Native?

* a JavaScript bridge for native modules
* building components with JavaScript, React and JSX knowledge
---

## Basic components

* `View`, `Scrollview`, `Text`, `Image`
----

## Styling à la CSS
----

* Scoped styles out of the box
```jsx
...
    <Text style={styles.heading}>Hello world!</Text>
...
const styles = StyleSheet.create({
    text: {
        fontFamily: 'Arial',
        fontSize: 16
    }
});
```
----

* Layout with Flexbox
```jsx
...
    <View style={{ flex: 1, justifyContent: 'center' }}>
        <Text>Hello world!</Text>
    </View>
...
```
----

Composition with spreading

```jsx

return (
    <Text style={styles.heading}>Hello world!</Text>
);

const styles = StyleSheet.create({
    text: {
        fontFamily: 'Arial',
        fontSize: 16
    },
    largeText: {
        fontSize: 22
    },
    heading: {
        ...text,
        ...largeText,
        fontWeight: 800
    }
});
```
----

## How does it work?
----

![React Native Architecture](https://miro.medium.com/max/1600/1*331KENPILKOregPuYFbzZw.png)
----

![React Native Communication](https://image.slidesharecdn.com/introtoreactnative-170424104444/95/introduction-to-react-native-rendering-charts-graphs-9-1024.jpg?cb=1493030762)
---

## Getting started with Expo
----

1. Bootstrap
2. Download app
3. Develop!
Note:
* Show example app with simulator
----

## Why use Expo?

* Default way to get started without any know-how
* Live-Reload
* Fast testing on any device
  * Also for non-devs!
* Playground for snippets (snack.expo.io)
* **OTA** updates!
----

## When don't use Expo?

* Custom native code or modules required
* Small app size matters
Note:
* It's always possible to eject
---

## Wrapping up
----

### Pros

* Getting started without any native skills is easy
* Develop once, run everywhere
* Whole power of npm modules can be used
* Huge community (but not that huge like for React)
----

### Cons

* It's alyways better to know how the native modules work
* UX- and navigation patterns differ from web
* Not usable for game development
* Not all implementations perform the same on Android & iOS
Note:
* Browsers do a lot of optimization out of the box for us (e.g. caching)
---

Develop once, run **REALLY** everywhere

## 👉 React-Native-Web
# 🤯
Note:
* Integrates perfectly with Next.js
* Used by Twitter, Uber, The Times, ...
---

## Sources

* [React Native Docs](https://facebook.github.io/react-native/)
* [Expo Docs](https://docs.expo.io/versions/latest/)
* [Flutter vs React Native — Vitaly Kuprenko](https://levelup.gitconnected.com/flutter-vs-react-native-comparing-the-features-of-each-framework-f61bfd146a90)
* [Introduction to React Native & Rendering - Rahat Khanna](https://www.slideshare.net/rahatkhanna/introduction-to-react-native-rendering-charts-graphs)
* [React Native Web](https://github.com/necolas/react-native-web)