# Glioma Radiomics Feature Extraction
DICOM → GLCM texture + first-order + shape features

✓ GLCM Texture: Contrast, Homogeneity  
✓ First-order: Mean, Std, Skewness  
✓ Shape: Area, Perimeter, Eccentricity  
**Ready for SVM/RF classification**


<img width="308" height="263" alt="image" src="https://github.com/user-attachments/assets/ca7a96ab-6681-4471-914a-ff7283bd7dc6" />


# Quick Demo

I = dicomread('brain.dcm');
I = mat2gray(I);
mask = roipoly(I);  % Draw tumor ROI
features = extractRadiomics(I, mask);  % 8 features instantly!

# WorkFlow Pipeline 

1. DICOM Read → Normalize → ROI Segmentation   
2. GLCM Texture + First-order + Shape Features
  
ML-ready feature table (.csv)

<img width="340" height="97" alt="image" src="https://github.com/user-attachments/assets/a213e5bb-b4b0-4bb3-9c19-356d8f863fd5" />

