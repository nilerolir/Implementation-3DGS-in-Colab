# Implementation 3DGS in Colab
To test the use of 3D Gaussian Splatting technology, I implemented the original code developed by graphdeco-inria in Google Colab, as I do not have a suitable graphics card. Just follow the comments below and Colab file

| Title | Info | Link |
|----------------|----------------|---------------|
| Implementation of 3DGS | Just  open the link and play |https://colab.research.google.com/drive/1gNFL0c-cmz13nPXzrn1aVRYBbiouBaD2#scrollTo=Xs2TxvsbvFWg|
| 3DGS Render Blender Addon by KIRI Engine | Add-on to use file.ply in Blender| https://github.com/Kiri-Innovation/3dgs-render-blender-addon |


#3DGS Render Addon by KIRI Engine for Blender

## PLY file in Blender
![imagen](https://github.com/user-attachments/assets/f583d649-55e1-4d14-9835-89689547103f)

## PLY file edited in Blender
![imagen](https://github.com/user-attachments/assets/a8038708-391e-40c5-9db5-1f6193326ea5)






1. First, download and upload the Colab file to your own Colab account.
2. Just follow the comments below and the Colab file.

## Comments
1. If you have your own dataset, you can modify the code in the "Dataset download and preparation" section and add the link to your dataset.zip, or if it is a video, use the commented option and provide the link to a video.mp4. For this, use the command `!wget -O dataset.mp4 <link>` and `!ffmpeg -i dataset.mp4 -qscale:v 1 -qmin 1 -vf fps=<change the number of frames per second> %04d.jpg`
2. For the following dataset <https://www.dropbox.com/scl/fi/8uqjqbqtzj9gazb4hat98/VID_planta_16012025_000.zip?rlkey=5l612v5rlxmctmmvcma9a2wwd&st=h1e7snz2&dl=1>, which contains 300 images of a plant, I performed 7,000 iterations (each additional iteration improves the quality of the representation). The execution time was around 2.5 hours, with COLMAP configuration alone taking at least 1 hour. As a result, the following metrics were achieved: L1 = 0.0301, PSNR = 26.6, and a point count of 192,409 points.

3. To download the folder with the results, you need to know the name of the folder, as it is generated arbitrarily. For this, the command `!ls /content/gaussian-splatting/output` will display the name of the folder containing the results.

## PSNR (Peak Signal-to-Noise Ratio)
Is a metric used to measure the quality of a reconstructed or compressed image compared to its original version and higher values generally indicate better image quality and less distortion.

## L1 Loss (Mean Absolute Error - MAE)
Also known as Mean Absolute Error, measures the average absolute difference between predicted and true values. In image reconstruction tasks, it calculates how close the reconstructed image's pixel values are to the original image's pixel values. A smaller L1 value indicates better accuracy.

## Main Repo
https://github.com/graphdeco-inria/gaussian-splatting

## Page
https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/

## Paper 3D Gaussian Splatting for Real-Time Radiance Field Rendering
https://arxiv.org/abs/2308.04079

## Implementation of another user in Colab
https://github.com/camenduru/gaussian-splatting-colab
