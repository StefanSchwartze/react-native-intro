#### An introduction to
# React Native

Stefan Schwartze
---

## What is React Native?

* a JavaScript bridge for native modules<!-- .element: class="fragment" -->
* building components with JavaScript, React and JSX knowledge<!-- .element: class="fragment" -->
---

## Basic components

* `View`, `Scrollview`, `Text`, `Image`, ...
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

* Composition with spreading
----

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
<!-- .element: class="stretch" -->
----

## How does it work?
----
<!-- .slide: data-background-image="https://miro.medium.com/max/1600/1*331KENPILKOregPuYFbzZw.png" data-background-size="contain" -->
----

<!-- .slide: data-background-image="https://image.slidesharecdn.com/introtoreactnative-170424104444/95/introduction-to-react-native-rendering-charts-graphs-9-1024.jpg" data-background-size="contain" -->
---

## Getting started with 

React Native CLI | **Expo CLI**

----

### 1. Install Expo CLI
![Install](./images/install.svg)
Note:
```bash
npm install -g expo-cli
```
----

### 2. Bootstrap
![Init](./images/init.svg)
Note:
```bash
expo init
```
----
### 3. Download app
![Expo Icon](https://is4-ssl.mzstatic.com/image/thumb/Purple123/v4/65/24/19/652419e4-053e-d24a-1850-da1073f092e6/AppIcon-0-0-1x_U007emarketing-0-0-0-7-0-0-sRGB-0-0-0-GLES2_U002c0-512MB-85-220-0-0.png/460x0w.png)
  * [Android](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=de) | [iOS](https://apps.apple.com/de/app/expo-client/id982107779)
----
### 4. Develop!
Note:
* Show example app with simulator
----

## Why use Expo?
----

* Default way to get started without any know-how<!-- .element: class="fragment" -->
* Live-Reload<!-- .element: class="fragment" -->
* Fast testing on any device<!-- .element: class="fragment" -->
  * Also for non-devs!
* Playground for snippets (snack.expo.io)<!-- .element: class="fragment" -->
* OTA updates!<!-- .element: class="fragment" -->
----

## When don't use Expo?

* Custom native code or modules required<!-- .element: class="fragment" -->
* Small app size matters<!-- .element: class="fragment" -->
Note:
* It's always possible to eject
---

## Wrapping up
----

### Pros

* Getting started without any native skills is easy<!-- .element: class="fragment" -->
* Develop once, run everywhere<!-- .element: class="fragment" -->
* Whole power of npm modules can be used<!-- .element: class="fragment" -->
* Huge community (but not that huge like for React)<!-- .element: class="fragment" -->
----

### Cons

* It's alyways better to know how the native modules work<!-- .element: class="fragment" -->
* UX- and navigation patterns differ from web<!-- .element: class="fragment" -->
* Not usable for game development<!-- .element: class="fragment" -->
* Not all implementations perform the same on Android & iOS<!-- .element: class="fragment" -->
Note:
* Browsers do a lot of optimization out of the box for us (e.g. caching)
---

Develop once, run **REALLY** everywhere

## React-Native-Web<br/>
# 🤯<!-- .element: class="fragment" -->
Note:
* Integrates perfectly with Next.js
* Used by Twitter, Uber, The Times, ...
----

### 👉 [Snack](https://snack.expo.io/@stefan.schwartze/react-native-web-swiper)
---

## Sources

* [React Native Docs](https://facebook.github.io/react-native/)
* [Expo Docs](https://docs.expo.io/versions/latest/)
* [Flutter vs React Native — Vitaly Kuprenko](https://levelup.gitconnected.com/flutter-vs-react-native-comparing-the-features-of-each-framework-f61bfd146a90)
* [Introduction to React Native & Rendering - Rahat Khanna](https://www.slideshare.net/rahatkhanna/introduction-to-react-native-rendering-charts-graphs)
* [React Native Web](https://github.com/necolas/react-native-web)