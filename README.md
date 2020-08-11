# Mobile-Image-Aesthetics
A project with the long term goal of creating a real time image aesthetic scorer that could be incorporated into a smartphone camera.

Data was obtained form the [AVA dataset](http://refbase.cvc.uab.es/files/MMP2012a.pdf), this contains 255,000 photos collected from https://www.dpchallenge.com/, where they were scored from 1 to 10 and the score distributions are available.

With the goal in mind, initial proof of concept is to train a MobileNetV2 model (a low parameter convnet desigined for use on mobile hardware) to score the photographs based of the aesthetic scores.

Care must be taken to incorperate the right photo classes eg phones do not have macro lenses => macro photos are not applicable, and to make sure the net learns what a nice photo is rather than what is in a nice photo. Both are potentially useful, however, if the model is to help you take a nice photo of yourself, for instance, the aesthetic quality  needs to be based on composition, lighting, etc rather than the presence/absence of "aesthetic" objects that happen to correlate with well scored photos.
