# Auto_Checkout_Counter_with_Merchandise_Classification
This auto checkout counter aimed to utilize state-of-art computer vision algorithm in embedded systems to implement automation on selling merchandise. This concept is similar to unmanned store performed by Alibaba and Amazon, but have some further optimization on this. We attempted to operate all the transaction on the phone. More specifically, customer is expected to take a photo of the products they want and published to our interface (or application). In that platform, server classifies the stuff and marks it on the list, which would require the assistance of cloud computing. Customer only needs to press checkout button as long as they finish shopping. This could eliminate human resource on daily stores. 

We researched on this for a whole semester, there were models we worked on, respectively ResNet (nearly all type of layers), you only look once v2 (YOLOv2), and YOLOv4. ResNet structure was from open source. YOLOv2 and YOLOv4 were referred to [darkflow](https://github.com/thtrieu/darkflow) and [darknet](https://github.com/pjreddie/darknet). I also put their introduction and files here for quick view. Since this project operated on embedded systems, the computing loading of model was an important contribution for successfully executing. We therefore focused on the lightweight or tiny version of ResNet, YOLOv2, and YOLOv4. Detailed introduction exhibited in the following sections.

## Dataset


## Models


## Training


## Testing


## Conclusion


## Contact Info
Author: Chun-Sheng Wu, MS student in Computer Engineering @ Texas A&M University  
Email: jinsonwu@tamu.edu  
LinkedIn: https://www.linkedin.com/in/chunshengwu/

*This project was in collaboration with Jung-Te Lin under the supervision of Dr. Jiun-In Guo at Intelligent Vision Lab, National Chiao Tung University, 2020*
