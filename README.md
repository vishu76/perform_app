App performance enhancement
1. flutter lint for basic rule for coding
2. Avoid creating methods that return Widgets
   Text createTextWidget() {
   return  Text( 'Widget created inside a method. I);
  }
   A method that returns a widget has a
   negative impact on performance.
   The method's content is always executed, so
   it will always generate a new widget.
solution: always used statelessWidget
3. For lists, prefer ListView.builder()
   return   Scaffold(
  body: ListView(
   children: [
   // Long list of widgets...
]));
   Passing widgets directly to a ListView works
   with few items, but doesn't scale well.

   Flutter will instantiate all elements in
   memory, even if they are not visible on the
   screen.
Solution: use ListView.builder
4. Avoid heavy calculations in the build() method
   build() can be called multiple times per
   second.
   Adding repetitive heavy calculations within
   build() makes no sense.
Solution: use initState()
5. Use Isolates for heavy computations
   Running heavy operations on the main
   thread can slow down common tasks like
   rendering your interface.
   By using an Isolate, we move code execution
   to a separate thread.
Solution: await
6. Optimize your images for performance
   Use the 3 variants for images: xl, x2 and x3

   assets/ images/ la rge_image. png  // lx - 300X3ØO px
   assets/ images/ 2. Ox/ large_image. png // 2x - 600X6ØØ px
   assets/ images/ 3. Ox/ large_image. png // 3x - 9ØØX9ØØ px

• PNG for images requiring transparency
• JPEG for photos and complex images
• WebP for modern, highly compressed
images that support both transparency and photos

Compress your images and match their
resolution to how they're displayed. Loading
oversized assets wastes memory and hurts
performance

______________________________________________________
Performance Optimization:

Minimize Rebuilds:
Avoid unnecessary widget rebuilds by using const widgets where possible, optimizing state management, and using ListView.builder for efficient list rendering.
Efficient Layouts:
Use flexible and expanded widgets, and consider adaptive design to ensure your app adapts well to different screen sizes and orientations.
Asynchronous Code:
Leverage async/await for network calls and other long-running operations to prevent UI freezing.
Optimize Images:
Reduce image size, use optimized image formats, and leverage caching mechanisms to improve loading times.
State Management:
Choose an appropriate state management library (e.g., Provider, Riverpod, BLoC) to manage application state effectively and minimize rebuilds.
Use Flutter DevTools:
Utilize Flutter DevTools to monitor performance, identify bottlenecks, and debug issues.
Code Splitting:
For larger apps, consider code splitting to load parts of the app only when needed, reducing the initial load time.
Code Organization:
Clear Structure:
Organize your code into well-defined modules, folders, and packages to improve readability and maintainability.
Separation of Concerns:
Separate UI logic from business logic to make your code more modular and testable.
Maintainability:
Use consistent coding styles, document your code, and write unit tests to ensure code quality and make it easier to maintain.
User Experience:
Responsiveness:
Ensure your app is responsive and adapts to different screen sizes and orientations.
Animations:
Use animations sparingly but effectively to enhance the user experience and provide visual feedback.
Testing and Debugging:
Thoroughly test your app on different devices and screen sizes, and use debugging tools to identify and fix issues.
Minimize App Size:
Reduce the size of your application by removing unnecessary assets and optimizing code.
User Feedback:
Gather user feedback and use it to improve the app's design and functionality.
---------------------------------------------------------
Here's a more detailed breakdown:
1. Performance Optimization:
   Minimize Widget Rebuilds: Use const for widgets that don't change, ListView.builder for efficient lists, and StatelessWidget for widgets without state.
   Optimize Image Loading: Use CachedNetworkImage or other caching libraries, and optimize image sizes and formats.
   Asynchronous Programming: Use async/await for long-running operations to avoid blocking the UI thread.
   Efficient Layouts: Avoid overdraw and use optimized layout strategies.
   Profiling Tools: Utilize Flutter DevTools to identify performance bottlenecks.
2. Code Structure and Readability:
   Modular Architecture: Organize code into modules for better maintainability and scalability.
   State Management: Choose a suitable state management library (e.g., Provider, Riverpod, BLoC) to manage app state efficiently.
   Code Analysis: Use a code analyzer to identify potential issues and improve code quality.
   Constants: Use the const keyword for constants, grouping them in a class, and utilizing enums.
3. User Experience:
   Adaptive Design: Make the app look good on various screen sizes and devices.
   Animations: Add animations for a smoother user experience.
   Splash Screen: Use a splash screen to provide a visually appealing introduction while the app loads.
   Accessibility: Design the app to be accessible to users with disabilities.
4. Other Considerations:
   Keep Flutter Up-to-Date:
   Regularly update Flutter to benefit from performance improvements and bug fixes.
   Use Packages:
   Leverage Flutter packages to avoid reinventing the wheel and save development time.
   Test Thoroughly:
   Test the app on various devices and screen sizes to ensure a consistent user experience.

-----------------------------
Performance metrics:
Speed
Responsiveness
Memory usage
CPU usage
Battery consumption
Offline functionality
Crash rate
Error rate
Minimal lag
Startup time
Background processing
Predictable and reliable
user behavior
------------------
Performance - Flutter
UI
Minimum Ul rebuilds
Usage of Expensive Widget
Use builders
Use State management
Optimize scrolls
Minimize Tree Complexity

Memory
Destroy unused objects
Use stateless Widgets
Do not leak objects
Use better Data Structure
Use compressed assets
Code splitting
Object Pooling

CPU
Isolate Long-Running tasks
Cache network calls
Use Method Channels
Use FFI
Use Futures, Streams,


Flutter dev tools
Flutter inspector
Performance view
CPU profiler view
Memory view
Network view 
s-----
## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
