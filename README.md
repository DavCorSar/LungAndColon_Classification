# LungAndColon_Classification
Classification of lung and colon cancer histopathological images using a CNN.  

This Notebook uses a dataset of lung and colon histopathological images, made with the objective to detect cancer. You can find this same dataset on *Kaggle* following the next link: https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images  

This dataset contains 25,000 histopathological images with 5 classes [[1]](#1). All images are 768 x 768 pixels in size and are in jpeg file format.
The images were generated from an original sample of HIPAA compliant and validated sources, consisting of 750 total images of lung tissue (250 benign lung tissue, 250 lung adenocarcinomas, and 250 lung squamous cell carcinomas) and 500 total images of colon tissue (250 benign colon tissue and 250 colon adenocarcinomas) and augmented to 25,000 using the Augmentor package.  
There are five classes in the dataset, each with 5,000 images, being:  

* Lung benign tissue  
* Lung adenocarcinoma  
* Lung squamous cell carcinoma  
* Colon adenocarcinoma  
* Colon benign tissue  



Once you've downloaded the dataset and placed it in the same folder as the notebook, you must modify the folder containing the data to make sure it follows the next structure:  

  ├── lung_colon_image_set  
  │   ├── lung_image_sets          # Folder downloaded from kaggle as default  
  │   |     ├── lung_aca  
  │   |     ├── lung_n  
  │   |     ├── lung_scc  
  │   ├── colon_image_sets         # Folder downloaded from kaggle as default  
  │   |     ├── colon_aca  
  │   |     ├── colon_n  
  │   └── combined_image_sets      # Folder created containing all the previous subfolders of the 5 classes of images  
  │   |     ├── colon_aca  
  │   |     ├── colon_n  
  │   |     ├── lung_aca  
  │   |     ├── lung_n  
  │   |     ├── lung_scc  
  └── ...  

Inside the notebook, the first objective is to create a 5-class classifier, finally obtaining an overall accuracy of 95%. After that, we will split this model into two different ones. The first one used for lung classification, obtaining an overall accuracy of 96%. Finally, the last model, used for colon classification obtained an overall accuracy of 95%.  


## References  
<a id="1">[1]</a>
Borkowski AA, Bui MM, Thomas LB, Wilson CP, DeLand LA, Mastorides SM. Lung and Colon Cancer Histopathological Image Dataset (LC25000). arXiv:1912.12142v1 [eess.IV], 2019
