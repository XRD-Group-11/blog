# Idea

We have came up with an initial ideas to solve indoor navigation for big airports, hospitals, educational institutions ect.

---

# Approach

## GPS

When testing the GPS signal indoors, we found out that the phone can only connect to 1 or 2 GPS satellites in most indoor situations. That gives a high unreliability for the positioning tracking. The margin of error is approximately 20 meters. In our case that was to much. That is why we have chosen not to proceed with that option.

## Bluetooth Beacons

While researching online some ways of implementing the Bluetooth Beacons, we came up with a few issues like the high cost of each bluetooth beacon, the extra requirement of maintenance due to the fact that a beacon has a battery, the lack of orientation that would be a problem and, the need for implementing the beacon into the existent models which would require a higher amount of work than any other solution.

## Wifi Routers

Since VIA has decent amount of WiFi routers that are spread around the VIA floor but the issue comes as the amount the implementation needed to understand at all times where is the user and his orientation and also strength of the Wifi signal.

## Magnetic Field

While it would be a smarter option, after looking up further information online, we found out that it would become pretty unreliable and useless the more people would be in a spot. This is because the existence of many metallic items or other common commodity items would affect the magnetic waves, thus turning the data unreliable.

## QR Code

This solution proved to be the best option for us because we can calibrate our position and orientation to the QR code. The QR codes must be unique and placed approximately 10 meters from each other. They have to be both modeled in the real world and the 3d models. Then once we scan the QR code we can anchor our position and orientation in the virtual world.

## Landmark Recognition

One of the reasonable solutions, but due to the requirement that a landmark must be easy to see and easy to recognize, it makes its usage too hard for an application that is supposed to help guide people.

---

# Conclusion

Our final decision was to use the QR code approach.

---

# Prototypes

THe 3d models for the prototype we got from a previous group that was trying to solve a similar problem. We have models of third and fourth floor of VIA. The models only contain corridors which are useful for occlusion and for the path finding. Additionally we have implemented navigation using Unity's NavMesh, and we have displayed the optimal route with Unity's line render.
