![image](https://github.com/VicHazewinkel/AndroidTV_ComposeNavigation/assets/74927171/18fe2763-f501-4f6e-b5cb-4c7ba7cc1438)

Compose for TV is our recommended approach for building Android TV user interfaces. It unlocks all the benefits of Android's Jetpack Compose for your TV apps, making building beautiful and functional UIs for your app much easier. Some specific benefits of using Compose for TV are:

Flexibility: Compose can be used to create any type of UI, from simple layouts to complex animations. Components work out of the box but can also be customized and styled to fit your app's needs.
Simplified & Accelerated Development: Compose is compatible with existing code and enables developers to more efficiently build apps with less code.
Intuitive: Compose uses a declarative syntax that lets you to make changes to your UI, debug, understand and review your code.

<h1>Setup</h1>
Using Jetpack Compose on Android TV is similar to using Jetpack Compose for any other Android project. The main difference is that Compose for TV adds libraries that offer TV optimized components and make it easier to create user interfaces tailored to TV. In some cases those components share the same name as their non-TV counterparts, such as androidx.tv.material3.Button and androidx.compose.material3.Button.

<h1>Jetpack Compose toolkit dependencies</h1>
To use Compose for TV, you need to include Jetpack Compose toolkit dependencies in your app's build.gradle file as follows:

dependencies {
   val composeBom = platform("androidx.compose:compose-bom:2024.03.00")
   implementation(composeBom)

   // General compose dependencies
   implementation("androidx.activity:activity-compose:1.8.2")

   implementation("androidx.compose.ui:ui-tooling-preview")
   debugImplementation("androidx.compose.ui:ui-tooling")

   // Compose for TV dependencies
   val tvCompose = "1.0.0-alpha10"
   implementation("androidx.tv:tv-foundation:$tvCompose")
   implementation("androidx.tv:tv-material:$tvCompose")
}
