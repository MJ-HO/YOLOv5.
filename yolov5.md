# YOLO v5 <hr>
## Title

Box recognition and classification using YOLOv5<br><br>

#
### Opening background information

Customers will experience great inconvenience if they order the product and wait for it to be delivered, but receive a damaged box and product after arrival. It takes a long time to receive a new product again, and customers will be dissatisfied.
The parcel delivery industry continues to develop and expand its scale worldwide, which requires fast logistics processing speed and high accuracy.
However, if the box is crushed or damaged when the parcel is received as the parcel volume increases, the internal product is damaged, and the damage to the box lowers customer satisfaction and leads to an increase in corporate costs.
There is a limit to identifying who is responsible because it is difficult to accurately track where it was damaged during logistics and delivery processes.
Therefore, new technologies incorporating AI are needed to reduce inconvenience to companies, delivery drivers, and customers and to make logistics systems more efficient and reliable. <br><br>

#
### General description of the current project

It is inefficient to visually check damaged boxes during the distribution process. By using YOLOv5 to detect the status of the box in real time, the damaged and normal boxes are classified, and only the normal boxes are moved to the delivery route.
Since a large number of objects must be detected in real time, it allows them to sort boxes without errors and increase the logistics processing speed.
Passing only normal boxes reduces customer inconvenience and enables efficient management from the company's point of view. Boxes separated by damaged boxes can be collected and recycled to contribute to environmental protection.
In order to resolve disputes that may arise during the delivery process fairly, the system is also attached to the delivery vehicle to detect damage in real time. <br><br>

#
### Proposed idea for enhancements to the project 

With the application of AI, repetitive tasks can be reduced using the YOLOv5 model.
In the logistics industry, work can be handled without interruption of flow, and errors can be reduced with accurate object recognition to improve logistics processing speed and effectively respond to various situations.
Because the system can replace a large number of people, it is highly effective in terms of cost reduction.
Damaged boxes can be sorted separately, so they can be easily collected and recycled. In connection with the recycling industry, it can bring about environmental protection and economic effects.
It reduces customer inconvenience and resolves disputes with delivery drivers, resulting in increased reliability. <br><br>

#
### Value and signifiance of the project 

By improving speed and accuracy, which are key in logistics and distribution, it is possible to build unmanned processing systems or create better effects with less manpower, and increase reliability in quality. This creates the effect of reducing customer dissatisfaction.
Damaged boxes are also recovered efficiently and are recycled to reduce resource waste and reduce costs.
By detecting the damage that occurs during the delivery process, it is possible to clearly identify the responsible person in the event of a dispute. <br><br>

#
### Current limitations

In the case of fine damage, it is difficult to accurately recognize it separately from the normal box. Even when objects are concentrated in a complex environment, accurate recognition is difficult and detection is difficult by the external environment can affect performance. <br><br>

#
### Literature review

1.Among the actual cases in which the yolo model is applied, it is necessary to investigate the research results on logistics processing and explore the technologies.<br>
2.An accurate understanding of the technology for detecting and classifying various objects is needed. <br><br>


## Image Acquisition Method 

I downloaded the video from YouTube, pexels.com and acquired it.<br><br>
https://www.youtube.com/shorts/iPw-8pY_pGM<br>
https://www.youtube.com/shorts/-EPA20KTQfM<br>
https://www.pexels.com/ko-kr/video/4569535/<br>
https://www.pexels.com/ko-kr/video/4553205/<br><br><br><br>

## Training Data Extraction and Training Process 

&bull; DarkLabel is used to create and label images made with 640 x 640 resolution as frame-by-frame images.<br>

![그림 1](https://github.com/user-attachments/assets/2007fdaa-37ed-4a89-8186-2c6ead79fc16)<br><br><br><br>

### Training data extraction

&bull; Open the darklabel.yml file to add content.<br>
```python
box_classes: ["box"]
```
<br>

![그림 2](https://github.com/user-attachments/assets/f17c9439-845d-4a1a-8007-760d566518bf)<br><br><br><br>

&bull; Create a new format.<br>
```python
format9:    # darknet yolo (predefined format] <br>
 fixed_filetype: 1                 # if specified as true, save setting isn't changeable in GUI <br>
 data_fmt: [classid, ncx, ncy, nw, nh] <br>
 gt_file_ext: "txt"                 # if not specified, default setting is used <br>
 gt_merged: 0                    # if not specified, default setting is used <br>
 delimiter: " "                     # if not spedified, default delimiter(',') is used <br>
 classes_set: "box_classes"     # if not specified, default setting is used <br>
 name: "box"           # if not specified, "[fmt%d] $data_fmt" is used as default format name <br>
```
![그림 3](https://github.com/user-attachments/assets/0229da20-7557-4d40-8669-761095bb787b)<br><br><br><br>

&bull; Open the 640 x 640 video with open Video, uncheck labeled frames only, and create an image in the images folder with as Images.<br><br>

![그림 5](https://github.com/user-attachments/assets/e748b90f-0a47-4bef-ae49-fb73bc28e255)<br><br><br><br>

&bull; Change the 0.pascal voc part to the labelling class name you created and change the option to box + label. <br><br>
![그림 4](https://github.com/user-attachments/assets/24837c27-ec26-41b1-a660-6636716529f2)<br><br><br><br>

&bull; Open Image Folder to open and label the image by selecting the folder with the image. Save As to GT Save As in the labels folder and import to GT Load. Label data is stored as a text file and consists of class number, coordinates, width, and height. <br><br>
![그림 6](https://github.com/user-attachments/assets/c025d91d-f3f3-4ef6-bae1-54b423b4579b)<br><br><br><br>

### Training process 
&bull; Install the package in the yolov5 folder by cloning the file on GitHub. <br>
```python
!git clone https://github.com/ultralytics/yolov5 <br>
%cd yolov5 <br>
%pip install -qr requirements.txt <br>
```
<br><br><br><br>
&bull; Put the image and label made by DarkLabel in the train, val folder.<br><br><br><br>

&bull; Modify the data.yaml file to suit the classes and put it in the yolov5 folder with the yolov5n.pt file. <br><br>
![그림 9](https://github.com/user-attachments/assets/e1573800-a471-479f-89f3-b7e5452a5da6)<br>
![그림 8](https://github.com/user-attachments/assets/1af8b748-981d-48e1-b112-8d30950d4866)<br><br><br><br>

&bull; Install the Pillow library to process the image. <br>
```python
!pip install Pillow==10.3
```

![13](https://github.com/user-attachments/assets/e23ed6bd-34ea-41bf-a538-72e5a302b10a)<br><br><br><br>

&bull; Run train.py to learn the script in Python. The size of the image is 512 x 512, 16 images are processed at a time, and the learning is repeated 300 times.
Train using data.yaml and yolov5n.pt files, including information such as training data and verification data paths in the path. Improve learning speed with cache.<br>
```python
!python train.py  --img 512 --batch 16 --epochs 300 --data /content/drive/MyDrive/yolov5/data.yaml --weights yolov5n.pt --cache
```

![11](https://github.com/user-attachments/assets/ff75c0fb-e007-4580-ae48-e3c68d17437a)<br><br><br><br>

&bull; TensorBoard is used to visualize the learning process. Runs is a folder that stores training log files, and when learning is completed, a learned file is created in the folder. <br>
```python
%load_ext tensorboard
%tensorboard --logdir runs
```
<br><br><br><br>
&bull; To retrieve the saved training model, import best.pt in the corresponding path. Import the image stored in the images in the training folder and enter it into the model. Set the reliability with --conf. The results are stored in the runs/detect/exp folder.<br>
```python
!python detect.py --weights /content/drive/MyDrive/yolov5/runs/train/exp/weights/best.pt --img 512 --conf 0.1 --source /content/drive/MyDrive/yolov5/Train/images
```
![12](https://github.com/user-attachments/assets/cf4c92ed-764f-4737-a906-bd7957597b1f)<br><br><br><br>

&bull; Take 10 images from the front from the folder where the results are saved and check them.<br>
```python
import glob
from IPython.display import Image, display
for imageName in glob.glob('/content/drive/MyDrive/yolov5/runs/detect/exp/*.jpg')[:10]:
    display(Image(filename=imageName))
    print("\n")
```
<br><br><br><br>

&bull; The video is imported and trained with the saved training model and stored in the exp folder.<br>
```python
!python detect.py --weights /content/drive/MyDrive/yolov5/runs/train/exp/weights/best.pt --img 512 --conf 0.1 --source /content/drive/MyDrive/video.mp4
```
<br><br><br><br>

## Training result 
F1_curve &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; PR_curve <br>
<img src="https://github.com/user-attachments/assets/ff99e195-928e-4cb5-bc49-bdf31f492cba" alt="11" width="300px">
<img src="https://github.com/user-attachments/assets/c33b08a4-feb9-41b2-8224-eced006533fb" alt="11" width="300px" style="margin-right: 20px;"><br><br><br>

P_curve &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; R_curve <br>
<img src="https://github.com/user-attachments/assets/7bf4aca6-5cfc-4501-b92b-fc145bb4bf30" alt="11" width="300px">
<img src="https://github.com/user-attachments/assets/6a0946b4-6de6-46e8-8dd3-b2cb3ff4270a" alt="11" width="300px" style="margin-right: 20px;"><br><br><br>

confusion_matrix <br>
<img src="https://github.com/user-attachments/assets/538e1dde-f56d-4c2f-b05e-538ce5ef6c18" alt="11" width="300px">

results <br>
<img src="https://github.com/user-attachments/assets/e3df3549-a5b7-4270-b029-00a8f889af22"><br>

<img src="https://github.com/user-attachments/assets/fbc15a7b-023a-4b14-9ac0-15e316d44fba" alt="11" width="300px" style="margin-right: 20px;">
<img src="https://github.com/user-attachments/assets/660fc6d1-cd84-40df-ac3e-5de1405e3dd8" alt="11" width="300px"> <br><br>
<img src="https://github.com/user-attachments/assets/e9101aa5-a315-4d67-8731-58d32cb259de" alt="11" width="300px" style="margin-right: 20px;">
<img src="https://github.com/user-attachments/assets/091b24e8-bc11-4393-ada1-4c48b74fa74c" alt="11" width="300px"> <br><br><br>

## trained video 
The damaged box is marked as box.<br><br>
https://youtube.com/shorts/2ftsguCluPk<br>
https://github.com/user-attachments/assets/9f7ac7a3-e626-4ccd-a8b4-849e8a823336<br>
https://github.com/user-attachments/assets/33a195b7-17bf-4a48-ba91-05be05ff3dd6



