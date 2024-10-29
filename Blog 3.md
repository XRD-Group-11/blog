# Blog 3 - Starting implementation( QR Code, Path Finder, Occlusion ), Model, Testing

## Implementation

We started off by using the 3D model of VIA's 3rd floor and 4th floor, Added the `NavMesh` to the floor itself for the 3rd floor.

### QR Code

We have printed a physical QR code on a A4 paper. We have imported the same image of the QR code in to unity and made a `ReferenceImageLibrary` prefab that contained the Physical image size, and the image it self. After that step we have proceeded to create a `ARCameraCalibration` script that leverages `ARTrackedImageManager` script to find the QR code image in the real world. After the image has been found we perform calculations to calibrate the players orientation and position.
<br/><br/>
Our calibration calculation were not working. Our assumptions are that the `NavAgent` and AR camera are changing the position and rotation of the main camera and overwriting the calculations from the calibration script. Also we assume that there might be some sort of offset when we preform the calibration calculation, we do not know what is causing this offset. We have also experienced a lot of jittering when the calibration happens, we assume that the `ARTrackedImageManager` is not producing very accurate calculations and also the phones camera is not very stable when is held in the hands of a person that is walking.
<br/><br/>
At the end of the day we have tested the calibration and we have decided that the calibration is not working as we expected it too.

### Path Finder

Path finding was started off by adding the `NavAgent` that is going to use that `NavMesh` , then adding an line renderer that is going to point to the destination, that is set manually for the `NavAgent` and `NavAgent` needs to follow the line to the destination. We had to play with the `NavAgent` width and height so all of the places in the 3d model were accessible once we bake the `NavMesh`. We were experiencing some issues when the `NavAgent` is out of the `NavMesh` due to for example calibration , then the line would be bugged and wont lead to destination.

### Occlusion

We were trying to play around with the inspector of the cameras in hopes to find some way to hide the model walls from the camera only, while the path line would still "see" those walls. Essentially we are trying to find how to do Occlusion. We attempted to set the walls into a layer, and hide that layer from the camera through disabling a custom created layer in the Camera `Culling Mask`, but we weren't able to get a proper result. We also attempted to make a custom Shader as per the teacher suggestion, but it did not work as expected thus we kept attempting to look for other solutions.

## Conclusion

After the session we figured that since most of the part were not working as expected we decided to split the workload to each of the team members and then do it in our own free time and then in the next session to merge it and hope for the best.
