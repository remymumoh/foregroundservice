# Fore-ground services
In this tutorial, I will explain about foreground service android, How does work? What are the advantages and implementation? At last, I will prepare a foreground service sample app. So let’s get started.
What is Foreground Service

For more clarity let’s takes example Gmail, You are just using Gmail app and listening to music that is being played by Music Player application. So Music Player is basically using the foreground service to play the music. The foreground service always uses the notification to notify the user and using the notification you can actually interact with the service or the ongoing operation such as pause the music or play the next music.

So whenever in your app you see a notification that is performing some long running tasks that service is basically the foreground service and Foreground Service is always noticeable to the user that is the user is aware of this ongoing process.
Step up to writing implementation

    Initial Project Setup
    Create a subclass of Service – ForgroundService.java
    Create Notification Channel
    Override methods
        onStartCommand
            Mandatory to override for Foreground Service
        onBind
            Mandatory to override for Foreground Service
            Must return null for Foreground Service
        onCreate
            Optional to override
            Call only once, when Service is being created for the first time
        onDestory
            Optional to override
            Call when background service is destroyed
    Declare your service in Manifest.xml
