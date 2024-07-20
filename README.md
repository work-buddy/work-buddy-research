# work-buddy-research
Research about XR, computer vision, AI and company plans.

## Do we need to make our own headset?

Let's evaluate...

We **need** raw camera access to create custom XR software. This is an unmovable fact.

### Which headsets allow raw camera access?

#### Quest 3 - **NO / NOT YET**
![image](https://github.com/user-attachments/assets/246c5f39-e691-4bb3-be40-1df7ea0188dc)

https://www.uploadvr.com/metas-cto-thoughts-quest-developers-raw-camera-access/

Meta CTO thoughts verify Work Buddy dream:

> "The serious answer is we can all imagine phenomenally useful use cases if a developer has direct access to 
the camera. **You're a mechanic and you're looking at an engine** that you're not familiar with and a developer
could build the types of tools to help you see the overlays in the schematic, even diagnose the problem." - Meta CTO

> "**Meta is never going to build that**, and the developer can't upload to us every possible configuration of image that we might see for us to build a classifier on, that's not credible either. That's a use case that goes underserved if you don't build out the capability." - Meta CTO

#### Apple Vision Pro  - **MAYBE / ENTERPRISE PRIVATE ACCESS ONLY**
![image](https://github.com/user-attachments/assets/502eee5a-5aef-431b-89b7-45a732ba9d6b)

https://www.uploadvr.com/apple-vision-pro-enterprise-raw-camera-access/

> "Today at WWDC Apple announced Enterprise APIs for visionOS 2, which will give businesses access to advanced features not available in consumer apps." 

Amazing news Apple! But...

> "Apple makes clear that these features can only be used in apps **"for use in a business setting only"**, and apps using them can only be distributed as proprietary in-house apps or custom apps made for a specific business using **Apple Business Manager**, *not on the App Store*. A *managed entitlement is required*, alongside a license file tied to your Apple *developer account*."

Major headache, always at the whim of being shutdown whenever Apple feels like. We cannot tolerate any risks to our product or ask permission to make new technology.

#### PICO 4 Enterprise - **MAYBE / ENTERPRISE PRIVATE ACCESS ONLY**
![image](https://github.com/user-attachments/assets/332144b7-2734-4561-9c23-e37d83222121)

https://www.uploadvr.com/pico-4-enterprise-announced/

> "Pico 4 Enterprise is based on the Pico 4 Pro sold to consumers in China, with 256GB storage instead of 512GB. But Pico told us Enterprise will only be sold to registered businesses, not individuals. Even if you somehow got your hands on one, it doesn’t access the consumer app store."

Reviewing the Pico 4E web page:  
https://www.picoxr.com/global/products/pico4e

A lot of *"contact us"* and *"coming soon"*.
Some international restrictions on countries allowed.

Pico Enterprise Offerings:
- PICO Business Suite (coming soon)
- Enterprise OS (coming soon)
- PICO Business Store (coming soon)

Looking forward to seeing Pico Enterprise demos. Some potential here, but so far, not a solution for Work Buddy's custom requirements to start building today.

#### Varjo XR-4 Enterprise - YES 

![image](https://github.com/user-attachments/assets/36239624-7939-41c3-b06b-588bd2ddb140)

https://developer.varjo.com/docs/native/adjusting-camera-settings#getting-raw-camera-images  
https://developer.varjo.com/lab-tools  
https://developer.varjo.com/docs/native/varjo-native-sdk

**Varjo does allow raw camera access.**

Varjo is the technical leader in the industry.  
They make a very good headset, with best in-class native SDK enterprise support.

*However* we have some warning notes:

***Image Quality***

`The resolution of the image will be lower than what you are able to see through VST.`   
We would have to see the results. Low resolution images may handicap us.

***Price***

The Varjo XR-4 Enterprise edition is **retailing for ~$10,000 USD**.
Creating a business margin on-top of that high hardware price could be difficult, but possibly doable in Enterprise scenarios with investment funding and a Varjo partnership.

***Form Factor***

We think the best XR headset platform for augmenting IRL workers needs to be light weight and  built tough for outdoor and indoor use. The Varjo is a fine piece of tech, but fragile in outdoor use. It is more for simulators and indoor use currently. We need to build our own PC pack for the Varjo as they recommend Nvidia GPU PC hardwire connections, but Work Buddy needs to be battery powered for mobility. Can't plug a cord into the Work Buddy from the wall during use.
We have goals of making Work Buddy safety rated, impact resistant and waterproof in a hardhat helmet, this would require heavy modifications to the Varjo hardware.

A new Varjo XR-Outdoor edition + Work Buddy collab would be ideal but let's stay in reality.

> Varjo is definitely a potential headset candidate for v0 Work Buddy alpha development to get moving, but not going to happen home brewed without funding / partnerships.


### Other Factors with 3rd Party Headsets:

**Performance**

We have concerns on performance sacrifices for running in other companies 3rd party OSes and if actually allowed to run custom AI / ML models on device in raw camera access mode fully.
XR OSes usually come jam packed with social features, web browsers and miscellaneous software kits. Work Buddy needs to focus only on it's use-case to be successful and utilize it's hardware purely for assisting workers in realtime. Not having iMessage calls in background and playing Youtube 360s in side panel. Entertainment features are not our priority.

**Privacy and Security**

**Monetization**
