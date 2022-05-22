# Auto_Checkout_Counter_with_Merchandise_Classification
This auto checkout counter aimed to utilize state-of-art computer vision algorithm in embedded systems to implement automation on selling merchandise. This concept is similar to unmanned store performed by Alibaba and Amazon, but have some further optimization on this. We attempted to operate all the transaction on the phone. More specifically, customer is expected to take a photo of the products they want and published to our interface (or application). In that platform, server classifies the stuff and marks it on the list, which would require the assistance of cloud computing. Customer only needs to press checkout button as long as they finish shopping. This could significantly eliminate human resource on daily stores. 

We researched on this for a whole semester, there were models we worked on, respectively ResNet (nearly all type of layers), you only look once v2 (YOLOv2), and YOLOv4. ResNet structure was from open source. YOLOv2 and YOLOv4 were referred to [darkflow](https://github.com/thtrieu/darkflow) and [darknet](https://github.com/pjreddie/darknet). I also put their introduction and files here for quick view. Since this project operated on embedded systems, the computing loading of model was an important contribution for successfully executing. We therefore focused on the lightweight or tiny version of ResNet, YOLOv2, and YOLOv4. Detailed introduction exhibited in the following sections.

## Dataset
Our dataset is composed of merchandise with various backgrounds because customer is not constrainted to take the photo in a specific environment. We are eager to train a robust model that could accomodate to diversified images. There are three major types of backgrounds, indoor, market & store, and pure color. Each type contains 80 photos, there are 240 images in total.  

## Models
**ResNet34**, **tiny-YOLOv2**, and **tiny-YOLOv4** are main models we researched on. A small batch training conducted in advance to compare performance (accuracy and frame rate) between models. Tiny-YOLOv4 surpassed the other two models in these aspects with huge gap.

*Darkflow Weight&Img (Darknet's are inside the directory): https://drive.google.com/drive/folders/12Zaba2ZmzIQqDfZrd6Eup72dORZuPKx_?usp=sharing*

## Training
Training specs are shown below (there are set up to be surroundings like real embedded system):
- Batch size: 16
- Epoch: 100
- OpenCV, GPU = 1
- Input photo size (normalized): 416x416

Early-stopping was employed, thus the stored checkpoint with best performance might not be the last training epoch if there happens overfitting afterwards.

## Testing
Tiny-YOLOv4 model achieved 95.22% of accuracy within 2 seconds detection time. 

## Conclusion
Our experiment exhibited that tiny-YOLOv4 was compatible to classify products in light-loaded server. Even plus the respond time between server and users, it could handle the computing requirement to determine objects in this case. Besides, we could optimize the server with parallelization to accelerate the image processing. Conclusively, this project shows that auto checkout counter implemented by light-weight machine learning model has a promising future. 

## Contact Info
Author: Chun-Sheng Wu, MS student in Computer Engineering @ Texas A&M University  
Email: jinsonwu@tamu.edu  
LinkedIn: https://www.linkedin.com/in/chunshengwu/

*This project was in collaboration with Jung-Te Lin under the supervision of Dr. Jiun-In Guo at Intelligent Vision Lab, National Chiao Tung University, 2020*
