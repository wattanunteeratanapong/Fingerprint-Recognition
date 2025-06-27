# Fingerprint Recognition
The inspiration for this project is from a tv show called "Dexter". Dexter is a forensic expert in a blood spatter analyst, most of the time fingerprint matching is a Masuka's job, but some time Dexter have to deal with the finger print for his own secret side project. 😈 <br><br>
<img src="https://github.com/user-attachments/assets/932b0826-5cf5-46ff-9220-b2dba11da459" width="100%" alt="DexterandVince"> <br><br>

# Overview
In this project am gonna try to make a fingerprint matching between two image to see how the match of these fingerprint from scale 0%-100%, like a miami police department fingerprint matching system. This might include some of a image processing knowledge about image preparation and feature mathcing. There are plenty of a technique that i could think of for example ORB, SIFT, FLANN. Or even using CNN but i dont wanna dig that deep into a machine learning. So in this repository am gonna try to find the best method that suit this project. <br><br>
<img src="https://github.com/user-attachments/assets/7cf48143-abb8-4e0b-a441-9571cc47d6d1" width="100%" alt="Fingerprintsearching"> <br><br>

# Experimentation
## FLANN 
### Sample 1
<img src="https://github.com/user-attachments/assets/f35160b3-350b-4d6f-b80d-c09c22bd3b0c" width="49%" height="300px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/696cf3db-0452-4269-991e-8b6801a3a012" width="49%" height="300px" alt="Sample1"> <br>

### Sample 2
<img src="https://github.com/user-attachments/assets/5d68f2a7-dcf2-4560-9ea2-987f66fc0ba0" width="49%" height="300px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/7164faf5-b12f-446a-96d3-138f5a223155" width="49%" height="300px" alt="Sample2"> <br><br>

As you can see, i tried this technique and it performance is pretty poor. I also tried to tune the FLANN parameter to make it work, but i think it's likely impossible to implement the project with this method. So i wonder what kind of technique do the police like Miami Police Department in Dexter using? <br><br>

## Minutiae Based
### Sample 1
<img src="https://github.com/user-attachments/assets/37fd224d-f7b2-4f08-98d0-48ee87dd57ae" width="32%" height="200px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/0323a3ad-848a-4f25-ad34-d3850bf58fe8" width="32%" height="200px" alt="Sample1">
<img src="https://github.com/user-attachments/assets/b6da19bf-a6c9-4399-b683-a8a7794c23bd" width="32%" height="200px" alt="Sample1"> <br>

### Sample 2
<img src="https://github.com/user-attachments/assets/a3ccef27-44c2-433a-b8e9-d3d9602341fc" width="32%" height="200px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/97fd50d9-7509-49a5-b30f-e5a994f5f9c9" width="32%" height="200px" alt="Sample2">
<img src="https://github.com/user-attachments/assets/bc70ede8-6573-4cee-834c-8c21793cff8e" width="32%" height="200px" alt="Sample2"> <br><br>

I think this is the closest method that real the police use to find the match called "Minutiae Based". This include Histogram Equalization to distribute the color equally, then Tresholding to make image only black or white pixel (no gray or shade), then skeleton the image and extract minutiae points and compares them to find a match.  <br><br>

# Conclusion
Minutiae Based method accuracy seem fine. But there's one major problem, the two image format have to be the same format. But i assume that the police is already prep image format already before find match, so this shouldn't be a big concern. <br><br>

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
