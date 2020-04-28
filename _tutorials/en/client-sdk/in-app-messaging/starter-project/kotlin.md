---
title: The Starter Project
description: In this step you will clone the starter project
---

# The Starter Project

To make things easier, we are providing a `Starter` project for you. It is a simple Android Studio project that contains an application with the following two screens:

```screenshot
image: public/assets/images/tutorials/client-sdk/android-in-app-messaging-chat/app_intro.gif
```

1. Clone this [Github project](https://github.com/nexmo-community/client-sdk-android-tutorial-messaging).
2. Open the project in the `Android Studio` - navigate to menu `File -> Open` and select the `kotlin-start` folder from cloned repository.

All files that will be modified during this tutorial are located in the `app/src/main/java/com/vonage/tutorial/messaging/chat` directory:

![Project files](/assets/images/client-sdk/android-in-app-messaging-chat/project-files.png)

Now it's time to fill previously generated `conversation ID` and `JWT` tokens.

Open `Config.kt` file and add fill:

1. `Jane`'s user Id and JWTs
1. `Joe`'s user Id and JWTs
1. `CONVERSATION_ID` you've created on the previous steps:

```kotlin
package com.vonage.tutorial.messaging

data class User(
    val name: String,
    val jwt: String
)

object Config {

    const val CONVERSATION_ID: String = "" // TODO: set conversation Id

    val jane = User(
        "Jane",
        "" // TODO: "set Jane's JWT token"
    )
    val joe = User(
        "Joe",
        "" // TODO: set Joe's JWT token"
    )
}

```

Notice that we hardcoded these cons and values to store the properties of users. This might feel a bit out of place but makes it easier to use later on in this tutorial.