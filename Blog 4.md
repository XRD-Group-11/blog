# Blog 4 - Continuing Implementation ( QR Code, Path Finder, Occlusion ), Testing in real life

## Implementation

Catching up with all of the team members and their respective efforts, we gathered that overall we were not so successful in applying the expected work without any kind of error, thus we used this session to fix what was needed, and afterwards merge the code and test the final version.

We started off by trying to merge the branch off each person to main , so we can test the result of each merge.

### QR Code

The issues that we have faced the previous time were due to local and global positioning. We have taking in account once we do the calibration calculation to convert the local position to global. This has fixed our calibration, but we were still left with some small jittering. We have figured out tht we are updating the position of camera to many times. We have figured out that we can make a threshold, once exceeded it should trigger a new calculation, and we also used interpolation the transitions between old and new values would be smooth. After tweaking the values for interpolation speed and thresholds we have ended up with a pretty good result that looks and feels natural.

### Path Finder

When we started to search for some solution that will even though the `NavAgent` is out of the `NavMesh` the destination is still locked and that the path will lead to the destination properly , that was confusing to work on because it was hard to find an solution that handles that use case. One of the ways of fixing it is having the calibration to be precise then it wont even happen in first place. Another one is rewriting the `NavAgent` code so he would handle all those edge cases but it was felt it would be tedious process and it we wont be able to finish it on time so therefore we made small changes to the `NavAgent` code, and after merging with updated changes to the other parts it was working good enough, for the environment that we set for the location.

### Occlusion

After digging into the internet and trying to understand how the Occlusion would work, we found ourselves again being advised to use Shaders. With that said, the first working attempt of Occlusion was a `Unlit Shader` that had `Color Mask` of 0 and `ZWrite` enabled. We then also added all of the Model Walls into a custom layer called `Transparent`, and created a second camera that was a child of Main Camera, whereas the Main Camera would not include `Transparent` layer, and the Second Camera would include only `Transparent`. Later on, when we were merging, we found out that we did not need the second camera, and the custom layer, and that, in fact, all we needed was the Shader script.

## Conclusion

With everything merged, we went on to test our AR app. It worked in a satisfying way, though it is not dynamic, and the locations are hard coded, though what is the core of our project is the part of the guidance, which meant we did have success on it. We also ran out of time, otherwise we would have made it dynamic and perhaps being able to navigate to the 4th floor of VIA using some solution that will allow to go through elevator or stairs to the destination.
