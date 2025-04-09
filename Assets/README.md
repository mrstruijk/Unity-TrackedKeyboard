# Unity-TrackedKeyboard
Quick summary of project

## Purpose

I wanted to find out how a physical keyboard can be used in Unity when running a task as a build on the Quest HMD.


## Description

Meta released the [Unity-TrackedKeyboard project](https://github.com/oculus-samples/Unity-TrackedKeyboard), which incorporates both the mixed-reality keyboard tracking feature (to see an outline of the keyboard, or a passthrough version), and that works just fine.

It does seem to require the now old-old input system, and is not willing to run completely on the "new" input system. 

However, it turns out that if you can forego the entire MR / passthrough, you don't need anything special at all. It is all handled through the Meta OS, and has very little to do with the Unity project. 

See for example the `SOSXR_Keyboard_input_demo` in the `Assets/_SOSXR` folder. 

I don't know if I'm happy with a passthroughless version though. I'm thinking it could make it a little too interesting to try to type on it.

One of the major upsides of the passthrough keyboard tracker is that it also helps in setting the desk height to where it detects the keyboard to be. 

What I do see is that some of the nitty-gritty is really dependent on the Meta XR plugin, such as the use of the OVR Passthrough layer. Does Unity XRITK work with these types of things too? 
- Updating the Meta tools from V70 to V74 wants me to switch to using OpenXR pretty exclusively, which makes me quite happy.
- Added LeftHand and RightHand to the Hand Material Property Blocks, on the MRPassThroughHandVisualize... which strangely enough only exists on the left hand?
- It wanted to opdate the AndroidSDK to 32, and at least it seemed like, was happy to do this automatically.
- Make sure that "Show My Keyboard" is enabled in the Quest headset settings!!
- It seems to take a measure of the keyboard at starting of the app, and then later it is reasonably happy to switch keyboards, but it will not rescale the keyboard size. That doesn't matter though.
- The app did crash when doing the above.
- I also noticed some jitter in the space while I was typing. It wasn't just the textfield, it was the whole room. It wasn't due to a BT keyboard, because wired was the same issue. I could be due to what's in front of me while I was testing? I'm looking at a bunch of monitors, and a big window to my left. Not the best surfaces tbh.
- Everything worked still very well with the latest SDK updates, even when I thus had to switch to OpenXR. So it now runs on OpenXR with a Meta XR feature group. 
- 
- Still not a 100% on what to do with these separate systems. I am happy that we can use the OpenXR framework now, that is good. However we are going to need to use an OVR rig and other Meta OVR systems if we wanna go forward there. Again, not a problem, but I'm mostly thinking about flexibility (both between projects, and in starting a new project). Because when I start a new project and I want to start working with the Unity XRIT, there's the sample scene right there, setup and ready to go. But now if I want to use the keyboard passthrough (or even any kind of passthrough? I don't know), I need to use an OVR rig, and I need to get these from somewhere.
  - I think this may be multiple projects. One being: combining the 360 webview and the passthrough keyboard, the other being to find out how to make the OVR system into a convenient package. 
      - On that latter front, would that then be a completely separate package? Would that be a 'Sample' in an XR package? I don't really know yet.
        - What's the hestition though? I think it mostly has to do with not wanting to make yet again more double work, but that is partly nonsense, because I simply don't yet know what should or should not be included in a package. The only way to figure this out is through trying it out.
          - What I can do is this: get a fresh(-ish) Project with the tracked keyboard as a base. Then add the 360 video, configdata, etc to that package, and build a new 360 video version which includes the keyboard. 
            - And with Fresh-ish package: that can really simply be fork / branch of my current keyboard repo? Ask Elaine?



## Getting Started

### Dependencies

* Describe any prerequisites, libraries, OS version, etc., needed before installing program.
* ex. MacOS
* ex. Oculus Quest 3
* ex. Unity 2022.3

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets

``` Csharp
code blocks for commands
```

## Help

Any advise for common problems or issues.

``` Csharp
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. SOSXR

## Version History Summary

Using [Semantic Versioning](https://semver.org/) .

See CHANGELOG.md for details

* 0.1.0
    * Major breaking changes
* 0.0.2
    * Various bug fixes and optimizations
* 0.0.1
    * Initial Release

## License

[Choose an Open Source License](https://choosealicense.com/).

Add the license to the LICENSE.md file

## Acknowledgments

Inspiration, code snippets, etc.

* [Readme template](https://gist.github.com/DomPizzie/7a5ff55ffa9081f2de27c315f5018afc)

