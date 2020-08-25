---
layout: page
title: Satellite Observations
---

![Example Image](/projects/sat_obs/example_output.png)

Following in the footsteps of Marco Longbroek at [SatTrackCam](https://sattrackcam.blogspot.com/), I've started putting together a LEO satellite observation setup, consisting of:
* Watec 902H2 Supreme Low Light Camera
* Samyang f1.4/85mm Lens
* GPS Timestamper
* Yotocap AV USB capture
* A ball head tripod

It was surprisingly easy to get all of this working - I was worried about converting formats from the Watec security camera into something that could be captured, but it's in fact all composite video and everything just works.

So far, I've captured a few satellites but I haven't been particularly successful at capturing any specific satellites or measuring anything about them.

### Current issues:
* Where am I pointing the camera? 
* What's the field of view of the camera?
* Focus
* Light pollution
* Tripod wobble
* An annoying amount of setup/wires involved

### Things to investigate:
* Composite cable interference
* Building the system into a Pelican case
* Standalone DVR system with screen
* Plate solving to figure out pointing
* Image stacking and processing
* Movement tracking
* OCR of timestamps


## Pointing:
I have tried to use ATSAP and Astrometry.net's plate solvers to figure out what the camera is pointed at. So far, every run has failed, even though they seem to succeed on things that aren't even images of the sky. I am concerned that the field of view is so tiny that these systems can't work. 

Trying to calculate the angle of view - I have an 85mm lens for an EF mount with an APS-C sensor, with a 1.6 crop factor to a 35mm lens. 1/2" C mount sensors have a crop factor of 5.36. Does this mean the equivalent focal length of my 85mm focal length EF lens is (5.36*85mm/1.6) = 285 mm? That would provide for an angle of view of 1.28 x 0.97 degrees, which is small but not that small. However, I'm not sure that this conversion makes sense - it likely depends upon the definition of these numbers (is the listed focal length of the lens a 35 mm equivalent number?).

Per Stellarium, the angle of view is roughly 4.25x3.25 degrees, which matches up well with the view of the camera once I had it aligned.

### Setup
There are a ton of wires and currently I'm just pulling everything out of a small crate. I'd like to setup a Pelican case with a power distribution system, a small screen and a small DVR to record everything. I'd also like to convert from composite (analog) to digital as early in the process as possible.