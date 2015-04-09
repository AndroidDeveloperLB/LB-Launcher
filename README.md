# LB-Launcher
A truly open sourced launcher app, based on the same launcher app that comes with Android.

**Notes about the launcher**

 - It's the exact same launcher as "Launcher3" currently (**Kitkat** version, to allow most people use it, and because I had issues importing the Lollipop version), and I assume it has the same issues as the normal one.
 - Only thing I've changed is the name and package name, so that it won't interfere with other launchers. 
 - Minimum API to be able to launch the app : 16 (Jelly Bean) . I think it should suffice for now, but I would really love to see it get updated.

**Todo/wishes**
What I'd like this launcher to be is :

 - Always stay open sourced and free for all. Donation feature might be added (but only optional for users) in the future though, but credits will be given for everyone. :)
 - Always be up-to-date.
 - Have all the cool features from other launchers: themes, widgets list, backup&restore, gestures, ...
 - No BloatWare installed or allegedly installed.
 - Maybe have the ability to replace the locker (if the user accepts, of course), and have its own features too.


**Background**

This project was imported from the official Android "Launcher3" app (from [here](https://android.googlesource.com/platform/packages/apps/Launcher3)), by following the instructions written [here](https://plus.google.com/+fabiolobrutto/posts/KJeyKMBHVT7).

If you wish to import the "Launcher3" app too, or you wish to upgrade the one here, you can follow those steps that I've made:

1. clone the "Launcher3" project from [here](https://android.googlesource.com/platform/packages/apps/Launcher3) .
2. Note the "protos/backup.proto" folder. you need to compile it using "protoc" tool. get the latest one from [here](https://github.com/google/protobuf/releases) (or stable one from [here](https://developers.google.com/protocol-buffers/docs/downloads)), and run this command on the cloned folder:

    protoc –javanano_out=src/ -I protos protos/backup.proto
    
3. Since there are going to be some conflicts in java files, move all of the "wallpaperPicker" java files (in "src" folder) into the main folder. 
4. Get the "proto-nano" library and use it within the project. You can get the latest one [here](https://github.com/google/protobuf/releases) (search for "protobuf-javanano...") .
4. import the projects into Eclipse, and make the main one use the "wallpaperPicker" project as an Android library project. 
5. Errors fixing time. Fix all errors that you find. 
6. Run the app on the emulator/device. If you wish to see what I got on this phase, the original project folder before converting to Android-Studio is on the repository.
7. You can try to convert it to Android-Studio project.


**Why I've made this project**

Well, there are a couple of reasons:
 - I always wanted to create a launcher app, but I've noticed that a lot of work was done by Google, so I've decided to import it instead.
 - There isn't even a single launcher on the Play Store that's fully open sourced.
 - I hope developers would help making this an awesome launcher, and also keep it up-to-date.
