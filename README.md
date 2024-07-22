# work-buddy-research

Research about XR, computer vision, AI and company plans.

## Table of Contents

- [Examples of XR augmenting workers IRL. What are we building? ](#examples-of-xr-augmenting-work-irl-what-are-we-building)
- [Headset Comparisons. Do we need to make our own headset? ](#headset-comparisons-do-we-need-to-make-our-own-headset)
  - [Quest 3](#quest-3)
  - [Apple Vision Pro](#apple-vision-pro)
  - [Pico 4 Enterprise](#pico-4-enterprise)
  - [Varjo XR-4](#varjo-xr-4-enterprise)
  - [Magic Leap 2](#magic-leap-2)

## Examples of XR augmenting work IRL. What are we building?

The inspiration for an AI enhanced XR Work Buddy HUD is best sourced from Master Chief in HALO video games.
![image](https://github.com/user-attachments/assets/03ad1055-2169-415a-b536-ff445a69cc5a)

Note the emphasis on functional realtime systems to help the wearer perform their tasks.
Master Chief wasn't playing much Youtube 360s in his headset. XR can and should be so much more then it is today.

Work Buddy wants to adapt similar HUD concepts such as minimap, materials counts, object tracking, 3D world scanning, multi-user communications, points of interest, and the Cortana voice assistant AI to augment human workers with useful help.

Note that in HALO all of the weapons also interfaced uniquely with the wearer. "Smart Tools" has a future with Work Buddy.

### Work Buddy HUD Concepts:

#### Fast Food Worker
![image](https://github.com/user-attachments/assets/d64b970c-d239-407f-86a5-68301dec0f76)

#### Shipping Container Operator
![image](https://github.com/user-attachments/assets/8b41bfa9-e2f6-4cf4-afe2-1a1b8d975d64)

## Headset Comparisons. Do we need to make our own headset?

Let's evaluate...

We **need** raw camera access to create custom XR software. This is an unmovable fact.

### Which headsets allow raw camera access?

#### Quest 3

**_NO / NOT YET_**

![image](https://github.com/user-attachments/assets/246c5f39-e691-4bb3-be40-1df7ea0188dc)

https://www.uploadvr.com/metas-cto-thoughts-quest-developers-raw-camera-access/

Meta CTO thoughts verify Work Buddy dream:

> "The serious answer is we can all imagine phenomenally useful use cases if a developer has direct access to
> the camera. **You're a mechanic and you're looking at an engine** that you're not familiar with and a developer
> could build the types of tools to help you see the overlays in the schematic, even diagnose the problem." - Meta CTO

> "**Meta is never going to build that**, and the developer can't upload to us every possible configuration of image that we might see for us to build a classifier on, that's not credible either. That's a use case that goes underserved if you don't build out the capability." - Meta CTO

#### Apple Vision Pro

**_MAYBE / ENTERPRISE PRIVATE ACCESS ONLY_**

![image](https://github.com/user-attachments/assets/502eee5a-5aef-431b-89b7-45a732ba9d6b)

https://www.uploadvr.com/apple-vision-pro-enterprise-raw-camera-access/

> "Today at WWDC Apple announced Enterprise APIs for visionOS 2, which will give businesses access to advanced features not available in consumer apps."

Amazing news Apple! But...

> "Apple makes clear that these features can only be used in apps **"for use in a business setting only"**, and apps using them can only be distributed as proprietary in-house apps or custom apps made for a specific business using **Apple Business Manager**, _not on the App Store_. A _managed entitlement is required_, alongside a license file tied to your Apple _developer account_."

Major headache, always at the whim of being shutdown whenever Apple feels like. We cannot tolerate any risks to our product or ask permission to make new technology.

#### PICO 4 Enterprise

**_MAYBE / ENTERPRISE PRIVATE ACCESS ONLY_**

![image](https://github.com/user-attachments/assets/332144b7-2734-4561-9c23-e37d83222121)

https://www.uploadvr.com/pico-4-enterprise-announced/

> "Pico 4 Enterprise is based on the Pico 4 Pro sold to consumers in China, with 256GB storage instead of 512GB. But Pico told us Enterprise will only be sold to registered businesses, not individuals. Even if you somehow got your hands on one, it doesn’t access the consumer app store."

Reviewing the Pico 4E web page:  
https://www.picoxr.com/global/products/pico4e

A lot of _"contact us"_ and _"coming soon"_.
Some international restrictions on countries allowed.

Pico Enterprise Offerings:

- PICO Business Suite (coming soon)
- Enterprise OS (coming soon)
- PICO Business Store (coming soon)

Looking forward to seeing Pico Enterprise demos. Some potential here, but so far, not a solution for Work Buddy's custom requirements to start building today.

#### Varjo XR-4 Enterprise

**_YES_**

![image](https://github.com/user-attachments/assets/36239624-7939-41c3-b06b-588bd2ddb140)

https://developer.varjo.com/docs/native/adjusting-camera-settings#getting-raw-camera-images  
https://developer.varjo.com/lab-tools  
https://developer.varjo.com/docs/native/varjo-native-sdk

**Varjo does allow raw camera access.**

Varjo is the technical leader in the industry.  
They make a very good headset, with best in-class native SDK enterprise support.

_However_ we have some warning notes:

**_Image Quality_**

`The resolution of the image will be lower than what you are able to see through VST.`  
We would have to see the results. Low resolution images may handicap us.

**_Price_**

The Varjo XR-4 Enterprise edition is **retailing for ~$10,000 USD**.
Creating a business margin on-top of that high hardware price could be difficult, but possibly doable in Enterprise scenarios with investment funding and a Varjo partnership.

**_Form Factor_**

We think the best XR headset platform for augmenting IRL workers needs to be light weight and built tough for outdoor and indoor use. The Varjo is a fine piece of tech, but fragile in outdoor use. It is more for simulators and indoor use currently. We need to build our own PC pack for the Varjo as they recommend Nvidia GPU PC hardwire connections, but Work Buddy needs to be battery powered for mobility. Can't plug a cord into the Work Buddy from the wall during use.
We have goals of making Work Buddy safety rated, impact resistant and waterproof in a hardhat helmet, this would require heavy modifications to the Varjo hardware.

A new Varjo XR-Outdoor edition + Work Buddy collab would be ideal but let's stay in reality.

> Varjo is definitely a potential headset candidate for v0 Work Buddy alpha development to get moving, but not going to happen home brewed without funding / partnerships.

#### Magic Leap 2

**_YES_**

![Screenshot from 2024-07-20 09-50-54](https://github.com/user-attachments/assets/1835c0d7-c78e-484c-964c-372f05509ef9)

https://developer-docs.magicleap.cloud/docs/guides/ml2-overview/  
https://developer-docs.magicleap.cloud/docs/guides/features/android-camera/

> The Magic Leap 2 supports the Android Camera2 NDK APIs.

- 0 - Main Camera - provides access to compressed video and still images.
- 1 - CV Camera - best used for Computer vision scenarios, uncompressed, raw frames.
- 3 - Mixed Reality Capture Camera - provides the ability to capture virtual and mixed reality content.

This is quite impressive from Magic Leap to be honest.
They have the best open docs about raw camera access.

Magic Leap 2 may be our best choice if we did not make our own hardware.

**Reasons why Magic Leap is good:**

- Transparent AR Lens. Passthrough XR using cameras is not the best for IRL work. VR support is not a priority for Work Buddy.
- Compute and Battery hip pack. This is the only logical way to make XR glasses for best heat / weight. It would be unsafe if battery due to impact exploded on your face.
- Dynamic Dimmer lens. This is needed for bright outdoor use in XR.
- Price is only $3500 USD. For the amount of features and quality of XR hardware, this is a great price compared to say the Varjo.

**Some areas to improve:**

- Pack is a bit small, heard it gets very hot. We think we can go 2-4x bigger with the Pack and create a toolbelt harness attachment like many tradesworker use. This would offer near Desktop level XR performance.
- Waterproofing, durability, safety hardhat integrations. It is mostly indoor use only, a fragile headset.

**Similar Dream to Work Buddy:**

https://www.youtube.com/watch?v=5X6BXRUacBo

Magic Leap is already working on similar tech with functioning demos. However, XR would benefit greatly by being open-source.  
We think headset companies are too limited using only cameras to do everything. "Smart Tools" with headset pairing is the next-gen for precise AR tracking.  
XR will have to get over trying to do everything with Computer Vision.

### Other Factors with 3rd Party Headsets:

**Performance**

We have concerns on performance sacrifices for running in other companies 3rd party OSes and if actually allowed to run custom AI / ML models on device in raw camera access mode fully.
XR OSes usually come jam packed with social features, web browsers and miscellaneous software kits. Work Buddy needs to focus only on it's use-case to be successful and utilize it's hardware purely for assisting workers in realtime. Not having iMessage calls in background and playing Youtube 360s in side panel. Entertainment features are not our priority.

**Privacy and Security**

**Monetization**
