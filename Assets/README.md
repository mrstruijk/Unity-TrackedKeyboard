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

