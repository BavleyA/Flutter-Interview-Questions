# 📘 Flutter Interview Questions & Answers (From Basic to Advanced)

---

## 🟢 BASIC LEVEL

### 1. What is Flutter?
**Answer:**  
Flutter is an open-source UI toolkit developed by Google for building natively compiled applications for mobile, web, and desktop from a single codebase.

---

### 2. What language does Flutter use?
**Answer:**  
Flutter uses **Dart**, a client-optimized language developed by Google for fast apps on any platform.

---

### 3. What is the difference between `StatelessWidget` and `StatefulWidget`?
**Answer:**  
- `StatelessWidget`: UI does **not change** once built.
- `StatefulWidget`: UI **can change dynamically** during runtime using `setState()`.

---

### 4. What is a Widget in Flutter?
**Answer:**  
A widget is the **basic building block** of a Flutter UI. Everything in Flutter is a widget: layouts, text, images, buttons, etc.

---

### 5. What is hot reload?
**Answer:**  
Hot reload allows developers to inject updated source code files into a running Dart VM so changes reflect instantly without restarting the app.

---

### 6. What is the use of `pubspec.yaml`?
**Answer:**  
`pubspec.yaml` manages:
- Project metadata (name, description, version)
- Dependencies (plugins/packages)
- Assets (images, fonts)
- Environment settings

---

### 7. Difference between `final`, `const`, and `var`?
**Answer:**
- `var`: Variable whose type is inferred.
- `final`: Initialized only once; value set at runtime.
- `const`: Compile-time constant; deeply immutable.

---

### 8. What is `setState()` used for?
**Answer:**  
`setState()` tells Flutter that the internal state of a widget has changed and the UI should be rebuilt.

---

### 9. What are keys in Flutter?
**Answer:**  
Keys preserve state when widgets are moved within the widget tree. Useful in list views and performance optimizations.

---

### 10. How to create a simple layout in Flutter?
**Answer:**  
Using widgets like `Column`, `Row`, `Container`, `Padding`, etc.

```dart
Column(
  children: [
    Text('Hello'),
    ElevatedButton(onPressed: () {}, child: Text('Click')),
  ],
)
```````

## 🟡 INTERMEDIATE LEVEL

### 11. What is State Management?

**Answer:**  
State management is how you **handle data changes** and reflect them in the UI. Examples: `setState`, Provider, BLoC, Riverpod.

---

### 12. What is Provider and how does it work?

**Answer:**  
Provider is a wrapper around InheritedWidgets. It exposes data to widgets down the tree and rebuilds them when data changes.

---

### 13. What is BLoC?

**Answer:**  
**B**usiness **Lo**gic **C**omponent separates UI from business logic using Streams and Sinks. It’s useful in large scalable applications.

---

### 14. What is Navigator and how does routing work?

**Answer:**  
Navigator uses a stack to manage navigation and routes. You can push and pop routes (screens) to move through the app.

*Example*

```dart
Navigator.push(context, MaterialPageRoute(builder: (_) => NextPage()));
```

---
### 15. Difference between `pushNamed` and `push`?

**Answer:**

- `push`: Uses direct widget reference.

- `pushNamed`: Uses named route declared in `MaterialApp` (Uses a predefined named route).

---

### 16. How to make responsive UI?

**Answer:**

- Use `MediaQuery`, `LayoutBuilder`, and responsive widgets.

- Use `Expanded`, `Flexible`, `FittedBox`, and `Wrap`.
 ---
 
### 17. What is `Future`, `async`, and `await`?

**Answer:**  
Used for asynchronous operations.

- `Future`: A delayed computation.

- `async`: Marks a function as asynchronous.

- `await`: Waits for the completion of a Future.

*Example*

```dart
Future<void> fetchData() async {
  var data = await http.get(Uri.parse('url'));
}
```

### 18. What is `StreamBuilder`?

**Answer:**  
A widget that listens to a stream and rebuilds the UI each time it receives a new event.

## 🔵 Advanced Level

### 19. What is Clean Architecture?

**Answer:**  
It separates an app into three layers:

- **Presentation**: UI

- **Domain**: Business logic

- **Data**: APIs, databases

### 20. What are Mixins in Dart?

**Answer:**  
Mixins allow code reuse across multiple classes without using inheritance.


```dart
mixin Logger {
  void log(String msg) => print(msg);
}

```

### 21.  Difference between Future and Stream?

**Answer:**

- **Future**: One-time async result.

- **Stream**: Sequence of asynchronous events (e.g., sockets).

### 22. What is InheritedWidget?

**Answer:**  
A low-level widget used to efficiently pass data down the widget tree without rebuilding the entire tree.

---

### 23. How does Flutter render UI?

**Answer:**  
Flutter uses Skia, a 2D rendering engine, to draw UI directly on a canvas, not using native UI elements.

---

### 24. How to optimize Flutter app performance?

**Answer:**

- Use `const` constructors

- Minimize rebuilds

- Use `ListView.builder` for lists
 
- Avoid heavy operations in the build method
 
---

### 25. What is Flutter DevTools?

**Answer:**  
A suite of debugging and performance tools that include UI inspection, timeline view, memory analysis, and more.

---

### 26. What are Isolates in Dart?

**Answer:**  
Isolates enable parallel execution in Dart. Each isolate has its own memory and event loop, used for heavy tasks.

---

### 27. Difference between `final`, `const`, and `late`?

**Answer:**

- `final`: Value set once at runtime.

- `const`: Compile-time constant.

- `late`: Initialized later (non-nullable).

---

### 28. What is CI/CD in Flutter?

**Answer:**  
CI/CD automates testing, building, and deployment. Tools include:

- GitHub Actions

- Codemagic    

- Bitrise

- Fastlane

---

### 29. What are options for local storage?

**Answer:**

- `SharedPreferences`: For simple key-value pairs.

- `Hive`: Lightweight NoSQL DB.
 
- `SQLite`: For structured relational data.

---

### 30. How to handle push notifications?

**Answer:**  
Use `firebase_messaging`:

- Configure Firebase

- Request notification permissions

- Listen for messages using `onMessage`, `onLaunch`, and `onResume`
 
---

### 31. How does Flutter communicate with native code?

**Answer:**  
Using **Platform Channels** (`MethodChannel`) to invoke native Android/iOS methods from Dart.

---

### 32. What is Riverpod?

**✅ Answer:**  
A modern and safe state management library that:

- Is compile-time safe

- Doesn’t rely on `BuildContext`
 
- Replaces Provider with more features

---

### 33. Difference between `ConsumerWidget`, `HookWidget`, and normal widgets?

**Answer:**

- `ConsumerWidget`: Used in Riverpod for reading providers.

- `HookWidget`: From flutter_hooks for using hooks like `useState`.
 
- `Stateless`/`Stateful`: Native Flutter widgets.

