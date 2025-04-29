# Relativity in GPS: How Satellites Determine Your Smartphone's Location

## Slide 1: Title

Hello everyone. Today I'll be talking about "Relativity in GPS" - specifically, how artificial satellites determine your smartphone's location and the crucial role that Einstein's theory of relativity plays in this technology.

## Slide 2: Self-Introduction

Let me briefly introduce myself. I'm a freelance software engineer with expertise in computer vision, spatial information processing, and cloud infrastructure design.

## Slide 3: Today's Topics

Today, we'll cover the following topics:
- How GNSS (Global Navigation Satellite Systems) like GPS determine position
- The effect of special relativity on positioning
- The effect of general relativity on positioning

By the end, you'll understand what's happening behind the scenes when your smartphone's map app shows your location!

## Slide 4: Assumptions

To simplify our discussion, we'll make several assumptions:
- The Earth is a perfect sphere
- The Earth does not rotate
- The Earth is electrically neutral
- The Earth's mass distribution is uniform
- There is no atmosphere (vacuum)
- No other celestial bodies (like the Moon) exist

These assumptions are far from reality, but they make the problem more straightforward while still yielding reasonably accurate results.

## Slide 5: Technical Terminology

Let's clarify some terminology. GNSS (Global Navigation Satellite System) is the general term for satellite-based positioning systems. GPS (Global Positioning System) is just one type of GNSS. Others include GLONASS, Galileo, BeiDou, and QZSS. Today, I'll use the term GPS since it's most familiar to most people, though it's a bit like a mother who calls all game consoles "Nintendo" regardless of the brand.

## Slide 6: Position Measurement Using Geometric Optics

Now, let's explore the fundamental principles of position measurement using geometric optics.

## Slide 7: Simple Example of Distance Measurement

Consider a simple example: At time t equals 0 seconds, an object starts moving from point A to point B at a speed of v equals 10 meters per second. The object reaches point B at time t equals 10 seconds. What's the distance between A and B?

Using the basic formula, distance equals speed times time, we get:
AB equals 10 meters per second times 10 seconds = 100 meters.

This illustrates the fundamental principle that the distance between two points can be calculated using speed and time.

## Slide 8: Distance Measurement Using Light

In GPS, we use light that travel at speed c equals three point zero times ten to the eighth meters per second. If a satellite transmits a signal from point P at time t zero, and a smartphone receives this signal at point Q at time t zero + delta t, the distance between P and Q is:

PQ = c times delta t

The principle remains the same: distance equals speed multiplied by time.

## Slide 9: Positioning with One Satellite

With a single satellite, here's what happens: Satellite 1 transmits a signal from point P1 at time t0, and delta t later, a smartphone receives the signal at point Q. The distance between P1 and Q is R1 = c times delta t.

## Slide 10: Where is the Smartphone?

Based on this information alone, where is the smartphone? It must be somewhere on the surface of a sphere S1 with center P1 and radius R1. With just one satellite, we can only narrow down the location to somewhere on this spherical surface.

## Slide 11: Positioning with Two Satellites

Now let's add a second satellite. If we measure distances from two satellites, the smartphone must be on the surface of sphere S1 AND on the surface of sphere S2.

## Slide 12: Narrowing Down the Smartphone's Position

When two spheres intersect, they form a circle. Therefore, the smartphone must be somewhere on the circumference of circle C. By adding a second satellite, we've further narrowed down the possible location.

## Slide 13: Positioning with Three Satellites

Adding a third satellite gives us sphere S3. The intersection of circle C and sphere S3 gives us two points, Q1 and Q2. So now we know the smartphone is at one of these two points.

## Slide 14: Positioning with Four Satellites

Finally, with a fourth satellite, we get sphere S4. This sphere will pass through only one of our two candidate points. In this example, Q1 is the correct position. With four satellites, we can uniquely determine the smartphone's position.

## Slide 15: Summary of Satellite Positioning System

To summarize what we've learned so far:
- One satellite places you somewhere on a spherical surface
- Four satellites allow you to determine a precise position
- In practice, when we know the device is on Earth's surface, we can sometimes use three satellites, with Earth itself serving as the fourth constraint
- For aircraft and other applications where altitude matters, the fourth satellite is crucial

## Slide 16: Special Relativity Effects

Now let's explore how Einstein's special theory of relativity affects GPS measurements.

## Slide 17: Key Assertion of Special Relativity

One of the fundamental assertions of special relativity is that for objects moving at high speeds, time passes more slowly compared to stationary observers. This is an extremely simplified explanation, but sufficient for our discussion today.

## Slide 18: Concrete Example of Special Relativity

Let's consider a rocket moving at velocity v relative to Earth in a straight line at constant speed. From Earth's perspective, the rocket's clock runs slower than Earth's clock. For example, when Earth's clock shows that one hour has passed, the rocket's clock might only show 59 minutes.

## Slide 19: Lorentz Factor

This time dilation can be expressed mathematically.
If the rocket's clock advances by t prime seconds, during the same period, Earth's clock advances by t seconds.
The factor gamma is called the Lorentz factor.

## Slide 20: Simple Example of Time Dilation

Let's use some concrete numbers. If the rocket's velocity is v = 4.2 × 10^7 m/s, then when 1 second passes on Earth, only 0.99 seconds pass on the rocket. From Earth's perspective, the rocket's clock runs slower by 0.01 seconds.

## Slide 21: Time Delay Due to Special Relativity

Now let's apply this to GPS satellites. GPS satellites orbit at an altitude of about 20,000 km with a velocity of approximately 3.9 km/s. For simplicity, we'll assume the satellite is moving in a straight line at constant speed locally. Under these conditions, when a clock on Earth advances by 1 second, the satellite's clock falls behind by about 8.5 × 10^-11 seconds due to special relativity.

## Slide 22: Time Difference Over One Day

One day consists of 86,400 seconds. Therefore, the daily time delay for a GPS satellite clock is approximately 7.3 microseconds. Converted to distance, this represents about 2.2 km of positioning error. This is a significant error that cannot be ignored for accurate positioning. GPS measurements must account for this time difference.

## Slide 23: General Relativity Effects

Next, let's consider the effects of general relativity.

## Slide 24: Key Assertions of General Relativity

General relativity makes several key assertions:
- Mass creates curvature in spacetime
- This spacetime curvature is gravity
- Time runs slower in stronger gravitational fields

## Slide 25: How Gravity Affects Clock Rate

How does gravity affect clock rates? Time passes more slowly in stronger gravitational fields and faster in weaker gravitational fields. Earth's surface is close to Earth's center where gravity is strong, so clocks run slower. Satellites are 20,000 km above Earth's surface where gravity is weaker, so their clocks run faster.

## Slide 26: Schwarzschild Metric

The simplest mathematical expression for spacetime curvature (gravity) is the Schwarzschild metric, where G is the gravitational constant, M is the mass of the celestial body, and r is the distance from the center of the celestial body. Earth's gravity can be approximated using this metric.

## Slide 27: Why Earth's Gravity Can Be Approximated with the Schwarzschild Metric

The Schwarzschild metric assumes that the celestial body is spherically symmetric, stationary, non-rotating, and electrically neutral. Our simplified Earth satisfies these conditions. Even the actual Earth is close enough to these assumptions that the approximation works well.

## Slide 28: Further Simplification of the Schwarzschild Metric

The smartphone using GPS moves very slowly compared to the speed of light, so we can consider it essentially stationary. Therefore, we can ignore the spatial components of the Schwarzschild metric. Time dilation is caused solely by gravity.

## Slide 29: Time Dilation Due to Earth's Gravity

Mathematically, when 1 second passes at Earth's center, more time passes at radius r. This is because clocks run slower in stronger gravitational fields.

## Slide 30: Time Difference Between Earth's Surface and Satellites

Let R be Earth's radius and h be the GPS satellite's altitude. The satellite's distance from Earth's center is R + h. We can calculate the time difference between clocks on Earth's surface and those on GPS satellites.

## Slide 31: Values Used in Time Difference Calculation

Here are the values we'll use for our calculation:
- Gravitational constant G = 6.674 × 10^-11 m^3 kg^-1 s^-2
- Earth's mass M = 5.972 × 10^24 kg
- Earth's radius R = 6.378 × 10^6 m
- Satellite altitude h = 2.0 × 10^7 m
- Speed of light c = 3.0 × 10^8 m/s

## Slide 32: Time Difference Calculation Results

The calculation shows that over one day, a GPS satellite's clock runs approximately 45.5 microseconds faster than a clock on Earth's surface due to general relativity effects. This is larger than the time delay caused by special relativity effects.

## Slide 33: Total Time Difference

The time difference due to special relativity is -7.3 microseconds (delay), while the time difference due to general relativity is +45.5 microseconds (advance). Combining these effects, GPS satellite clocks run about +38.2 microseconds faster per day compared to Earth's clocks.

## Slide 34: What Happens If We Ignore the Time Difference?

What would happen if we ignored this time difference? A daily difference of 38.2 microseconds translates to about 11.5 km in distance. Over 35 days, this would accumulate to about 400 km of error—roughly the distance between Tokyo and Osaka! Your navigation system would be completely unusable.

## Slide 35: How the Correction is Implemented

So how do we solve this problem? The solution is surprisingly simple. The satellite's clock is deliberately set to run 38.2 microseconds slower per day before launch. In practice, this is achieved by using a clock with a different frequency. While the theoretical calculations are elegant, the solution is remarkably straightforward. GNSS is a perfect marriage of elegant theory and practical simplicity.

## Slide 36: Summary

To summarize what we've learned today:
- GPS determines position by measuring the time it takes for signals to travel from satellites to your device
- The more satellites, the more precisely we can determine position
- Accurate positioning requires correcting for time differences caused by both special and general relativity
- Special relativity causes satellite clocks to run slower
- General relativity causes satellite clocks to run faster
- Relativity is not just an abstract theory—it's actively used in technology we rely on daily!

## Slides 37-39: References

Please refer to the slides for the complete list of references. In particular, Neil Ashby's survey paper "Relativity in the Global Positioning System" was a key resource for understanding the time correction methods in GNSS.

## Slide 40: Call for Lightning Talk Presenters

The Physics Meetup is looking for lightning talk presenters! Any topic is welcome. If you're interested, please contact us via the Physics Meetup Discord server.

## Slide 41: Announcements

Our next meeting is scheduled for May 3rd. We plan to watch physics-related YouTube videos together. If you have any suggestions for videos you'd like to watch with the group, please let us know!
