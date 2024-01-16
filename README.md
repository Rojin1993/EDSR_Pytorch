# EDSR_Pytorch
Firstly, create low-resolution images from high resolution. For this step, simply use the `resize.py` file. Please note that high-resolution images are located in the HR folder, and the LR2 folder contains the low-resolution images. The width and height of images are reduced by half using the bicubic method. You can adjust this according to your requirements.
To test this method on low-resolution images, utilize the `EDSRtest.ipynb` file. Pay attention to the following warnings to obtain accurate results.
After cloning the GitHub repository to your Google Drive, navigate to the `src` folder within it. Open the `demo.sh` file in the this folder and uncomment the line:
python main.py --data_test Demo --scale 4 --pre_train download --test_only --save_results
Next, go to option.py and, for --dir_demo, choose the folder location of the low-resolution images. Now, you can execute the last part of EDSRtest.ipynb. The results of super resolution will be saved in the experiment/test/results-Demo folder. You can find the results of my test in the results folder.
As I tested this method on noisy images, I added the code for adding noise in the 'NoisyImages.ipynb' notebook. The first cell contains Gaussian noise, and the second cell adds 'salt and pepper' noise to the images.
To improve file clarity, I will outline the steps. Initially, I examined images of individuals, and the results of this method on these images can be found in "EDSR_results.zip". Within this folder, there are two sub-folders: "LR_2", containing super-resolution on images with a 1/2 reduction in width and height, and "LR_4", containing super-resolution on images with a 1/4 reduction in width and height. It should be noted that the original images for these are in the folder "HighResolution_original.zip."
The method's results on noisy and low-resolved images with a 1/2 reduction in width and height were over sized to locate on github. Additionally, the outcomes of this method on another set of images, low-resolved by a 1/4 reduction in width and height, are available in "EDSR_SR4.rar". The original images of this set are in "HighResolution.rar".
