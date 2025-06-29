# Fingerprint Recognition
The inspiration for this project is from a tv show called "Dexter". Dexter is a forensic expert in a blood spatter analyst, most of the time fingerprint matching is a Masuka's job, but some time Dexter have to deal with the finger print for his own secret side project. 😈 <br><br>
<img src="https://github.com/user-attachments/assets/932b0826-5cf5-46ff-9220-b2dba11da459" width="100%" alt="DexterandVince"> <br><br>

# Overview
In this project am gonna try to make a fingerprint matching between two image to see how the match of these fingerprint from scale 0%-100%, like a miami police department fingerprint matching system. This might include some of a image processing knowledge about image preparation and feature mathcing. There are plenty of a technique that i could think of for example ORB, SIFT, FLANN. Or even using CNN but i dont wanna dig that deep into a machine learning. So in this repository am gonna try to find the best method that suit this project. <br><br>
<img src="https://github.com/user-attachments/assets/7cf48143-abb8-4e0b-a441-9571cc47d6d1" width="100%" alt="Fingerprintsearching"> <br><br>

# Experimentation 
## FLANN 
### Sample 1 (0.96%)
<img src="https://github.com/user-attachments/assets/f35160b3-350b-4d6f-b80d-c09c22bd3b0c" width="49%" height="300px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/696cf3db-0452-4269-991e-8b6801a3a012" width="49%" height="300px" alt="Sample1"> <br>

### Sample 2 (11.89%)
<img src="https://github.com/user-attachments/assets/5d68f2a7-dcf2-4560-9ea2-987f66fc0ba0" width="49%" height="300px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/d15628bb-2273-4436-a625-afa659cfa5a4" width="49%" height="300px" alt="Sample2"> <br>

### Sample 3 (0.28%)
<img src="https://github.com/user-attachments/assets/71ce41f0-951c-4894-afb1-cb245d41d8c3" width="49%" height="300px" alt="Sample3">
<img src="https://github.com/user-attachments/assets/1eddedb7-e9ad-44ce-8586-269bf95fbdfe" width="49%" height="300px" alt="Sample3"> <br><br>

As you can see, i tried this technique and it performance is pretty poor. I also tried to tune the FLANN parameter or even preprocessing image before matching feature to make it work, but i think it's likely impossible to implement the project with this method. So i wonder what kind of technique do the police like Miami Police Department in Dexter using? <br><br>

## Minutiae Based
### Sample 1 (81.88%)
<img src="https://github.com/user-attachments/assets/37fd224d-f7b2-4f08-98d0-48ee87dd57ae" width="32%" height="200px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/0323a3ad-848a-4f25-ad34-d3850bf58fe8" width="32%" height="200px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/b6da19bf-a6c9-4399-b683-a8a7794c23bd" width="32%" height="200px" alt="Sample1"> <br>

### Sample 2 (31.62%)
<img src="https://github.com/user-attachments/assets/a3ccef27-44c2-433a-b8e9-d3d9602341fc" width="32%" height="200px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/97fd50d9-7509-49a5-b30f-e5a994f5f9c9" width="32%" height="200px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/bc70ede8-6573-4cee-834c-8c21793cff8e" width="32%" height="200px" alt="Sample2"> <br>

### Sample 3 (80.08%) (High Resolution Fingerprint)
<img src="https://github.com/user-attachments/assets/5d791d60-705d-4577-b3f1-b064486b8fc2" width="32%" height="200px" alt="Sample3">
<img src="https://github.com/user-attachments/assets/990c31ff-1688-48e5-a271-c366e7c0289d" width="32%" height="200px" alt="Sample3">
<img src="https://github.com/user-attachments/assets/286e6988-5620-47bf-b5d5-14d4d6e07e78" width="32%" height="200px" alt="Sample3"> <br><br>

I think this is the closest method that the real police use to find the match called "Minutiae Based". This include Histogram Equalization to distribute the color equally, then Tresholding to make image only black or white pixel (no gray or shade), then skeleton the image and extract minutiae points and compares them to find a match.  <br><br>

# Conclusion
My fingerprint recognizer using minutiae based method accuracy seem fine. But there's two major problem. <br>

1. The two image format have to be the same format. But i assume that the police is already organize image format before find match, so this shouldn't be a concern. <br>
2. Fingerprints cannot be rotated too much, or the method will fail to match them correctly. <br>

<img src="https://github.com/user-attachments/assets/eff61c99-bf5e-4f20-b7bd-dfb3eeb79ea5" width="100%" alt="DexterMickey"> <br><br>

# Source
<a href="https://youtu.be/xD88Qs_DZp4?si=36H1jLFSzvrj2B5j">Fingerprint Recognition - Computerphile</a>
<br>

<a href="https://www.intechopen.com/chapters/16502">Minutiae-based Fingerprint Extraction and Recognition | IntechOpen</a>
<br>

<a href="https://www.udemy.com/course/python-for-computer-vision-with-opencv-and-deep-learning/?couponCode=25BBPMXINACTIVE">Python for Computer Vision with OpenCV and Deep Learning</a>
<br>

<a href="https://www.researchgate.net/figure/Difficulty-in-fingerprint-matching-a-and-b-have-the-same-global-configuration-but_fig2_5597678">Fingerprint Sample 1</a>
<br>

<a href="https://www.researchgate.net/figure/a-Fingerprint-image-108-5-from-DB1-B-in-FVC2000-b-Enhanced-version-of-fingerprint_fig1_235447407">Fingerprint Sample 2</a>
<br>

<a href="https://www.newscientist.com/article/2412199-ai-can-tell-if-prints-from-two-different-fingers-belong-to-same-person/">Fingerprint Sample 3</a>
<br>

