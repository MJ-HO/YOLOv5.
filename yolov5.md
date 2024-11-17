# YOLO v5 <hr>
## Title # 주제
YOLOv5를 이용한 박스 인식과 분류<br><br>
Box recognition and classification using YOLOv5<br><br>

#
### Opening background information # 배경 정보 :
상품을 주문하여 택배가 배송되기를 기다렸는데 도착한 후 손상된 상자와 상품을 받게 될 경우 고객은 큰 불편함을 겪게 된다. 다시 새 상품을 받기까지 시간이 오래걸리며 고객은 불만이 높아지게 된다.
택배 산업은 전세계적으로 계속해서 발전하고 규모를 확장시켜 나가고 있고 이에 따라 빠른 물류 처리 속도와 높은 정확성이 요구된다. 
그러나 택배 물량이 증가하면서 택배를 받았을 때 상자가 찌그러지거나 손상된 경우, 내부 제품이 파손되어 있는 경우가 증가 하였고 상자의 손상은 고객의 만족도를 낮추며 기업의 비용 증가로 이어진다. 
물류, 배달 과정 중 어디에서 파손되었는지도 정확히 추적하기 어려워 책임 소재를 밝히는데 한계가 있다.
따라서 회사, 배송기사, 고객의 불편을 줄이고 물류 시스템을 더 효율적이고 신뢰할 수 있도록 AI를 접목시킨 새로운 기술이 필요하다.
<br><br>

Customers will experience great inconvenience if they order the product and wait for it to be delivered, but receive a damaged box and product after arrival. It takes a long time to receive a new product again, and customers will be dissatisfied.
The parcel delivery industry continues to develop and expand its scale worldwide, which requires fast logistics processing speed and high accuracy.
However, if the box is crushed or damaged when the parcel is received as the parcel volume increases, the internal product is damaged, and the damage to the box lowers customer satisfaction and leads to an increase in corporate costs.
There is a limit to identifying who is responsible because it is difficult to accurately track where it was damaged during logistics and delivery processes.
Therefore, new technologies incorporating AI are needed to reduce inconvenience to companies, delivery drivers, and customers and to make logistics systems more efficient and reliable. <br><br>

#
### General description of the current project # 전반적인 설명 :
손상된 상자를 유통 과정에서 육안으로 점검하기에는 비효율적이다. YOLOv5를 활용해 상자의 상태를 실시간으로 감지하여 손상된 상자와 정상 상자를 분류하여 정상 상자만 배송 경로로 이동 시키게 한다.
다수의 물체를 실시간으로 탐지해야 하기 때문에 오류 없이 상자를 분류 하고 물류 처리 속도를 증가시킬 수 있도록 한다.
정상 상자만 통과 시키는 것은 고객의 불편을 줄이고 기업 입장에서도 효율적 관리가 가능하게 한다. 손상된 상자로 분리된 상자들은 모아서 재활용하여 환경 보호에 기여할 수 있다.
배송 과정에서 발생할 수 있는 분쟁을 공정하게 해결하기 위해 배달 차량에도 시스템을 부착해 실시간으로 파손을 감지하도록 한다.
 <br><br>

It is inefficient to visually check damaged boxes during the distribution process. By using YOLOv5 to detect the status of the box in real time, the damaged and normal boxes are classified, and only the normal boxes are moved to the delivery route.
Since a large number of objects must be detected in real time, it allows them to sort boxes without errors and increase the logistics processing speed.
Passing only normal boxes reduces customer inconvenience and enables efficient management from the company's point of view. Boxes separated by damaged boxes can be collected and recycled to contribute to environmental protection.
In order to resolve disputes that may arise during the delivery process fairly, the system is also attached to the delivery vehicle to detect damage in real time. <br><br>

#
### Proposed idea for enhancements to the project # 강점 :
AI의 적용으로 반복적인 작업을 YOLOv5 모델을 사용해 작업량을 줄여주는 효과를 낼 수 있다.
물류 산업에서 흐름 중단 없이 일을 처리할 수 있고 정확한 객체 인식으로 오류를 줄여 물류 처리 속도를 향상 시키고 다양한 상황에 효과적인 대응이 가능하다.
시스템으로 수 많은 사람을 대체할 수 있기 때문에 비용 절감 측면에서 뛰어난 효과를 낸다.
손상된 상자들은 따로 분류 시킬 수 있기 때문에 쉽게 상자를 회수하여 재활용 할 수 있다. 재활용 산업과 연계하여 환경 보호와 경제적 효과를 가져올 수 있다.
고객의 불편함을 줄이고 배송기사와의 분쟁을 해결하여 결과적으로 신뢰도를 높인다. <br><br>

With the application of AI, repetitive tasks can be reduced using the YOLOv5 model.
In the logistics industry, work can be handled without interruption of flow, and errors can be reduced with accurate object recognition to improve logistics processing speed and effectively respond to various situations.
Because the system can replace a large number of people, it is highly effective in terms of cost reduction.
Damaged boxes can be sorted separately, so they can be easily collected and recycled. In connection with the recycling industry, it can bring about environmental protection and economic effects.
It reduces customer inconvenience and resolves disputes with delivery drivers, resulting in increased reliability. <br><br>

#
### Value and signifiance of the project # 중요성 :
물류 및 유통에서 핵심인 속도와 정확성을 개선하여 무인 처리 시스템을 구축하거나 적은 인력으로도 더 좋은 효과를 만들어낼 수 있으며 품질에 대한 신뢰도를 높일 수 있다. 이는 고객 불만을 줄이는 효과를 만든다.
파손된 상자 또한 효율적으로 회수되며 재활용 과정을 거쳐 자원낭비를 줄이고 비용 절감으로 이어진다.
배달 과정에서 발생하는 파손을 감지해 분쟁 발생 시 책임 소재를 분명히 알 수 있다.
<br><br>

By improving speed and accuracy, which are key in logistics and distribution, it is possible to build unmanned processing systems or create better effects with less manpower, and increase reliability in quality. This creates the effect of reducing customer dissatisfaction.
Damaged boxes are also recovered efficiently and are recycled to reduce resource waste and reduce costs.
By detecting the damage that occurs during the delivery process, it is possible to clearly identify the responsible person in the event of a dispute. <br><br>

#
### Current limitations # 직면하고 있는 한계 : 
미세한 손상이 있는 경우 정상 박스와 구분하여 정확하게 인식하기 어렵다. 복잡한 환경에서 객체들이 밀집되어 있는 경우에도 정확한 인식이 어렵고 외부 환경에 의해 탐지가 어려운 경우 성능에 영향을 줄 수 있다. <br><br>

In the case of fine damage, it is difficult to accurately recognize it separately from the normal box. Even when objects are concentrated in a complex environment, accurate recognition is difficult and detection is difficult by the external environment can affect performance. <br><br>

#
### Literature review # 문헌 고찰 : 
1.실제 yolo 모델이 적용된 사례중 물류 처리에 관한 연구 결과들을 조사하고 그 기술들을 탐구할 필요가 있다.<br>
2.다양한 객체를 탐지하고 분류하는 기술에 대해 정확한 이해가 필요하다. <br><br>

1.Among the actual cases in which the yolo model is applied, it is necessary to investigate the research results on logistics processing and explore the technologies.<br>
2.An accurate understanding of the technology for detecting and classifying various objects is needed. <br><br>


## Image Acquisition Method # 영상 취득 방법 :
youtube, pexels.com 에서 영상을 다운받아 취득하였다. <br><br>

I downloaded the video from YouTube, pexels.com and acquired it.<br><br>
https://www.youtube.com/shorts/iPw-8pY_pGM<br>
https://www.youtube.com/shorts/-EPA20KTQfM<br>
https://www.pexels.com/ko-kr/video/4569535/<br>
https://www.pexels.com/ko-kr/video/4553205/<br><br><br><br>

## Training Data Extraction and Training Process # 학습 데이터 추출 및 학습 과정
&bull; 640 x 640 해상도로 만들어진 영상을 프레임 단위 이미지로 만들고 라벨링 하기 위해 DarkLabel을 사용한다.<br><br>
DarkLabel is used to create and label images made with 640 x 640 resolution as frame-by-frame images.<br>

![그림 1](https://github.com/user-attachments/assets/2007fdaa-37ed-4a89-8186-2c6ead79fc16)<br><br><br><br>

### Training data extraction # 학습 데이터 추출
&bull; darklabel.yml 파일을 열어 내용을 추가한다.<br><br>
Open the darklabel.yml file to add content.<br>
```python
box_classes: ["box"]
```
<br>

![그림 2](https://github.com/user-attachments/assets/f17c9439-845d-4a1a-8007-760d566518bf)<br><br><br><br>

&bull; 새로운 format을 만든다.<br><br>
Create a new format.<br>
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

&bull; open Video로 640 x 640 영상을 열고 labeled frames only의 체크표시를 끄고 as Images로 Images폴더 안에 이미지를 만든다.<br><br>
Open the 640 x 640 video with open Video, uncheck labeled frames only, and create an image in the images folder with as Images.<br><br>

![그림 5](https://github.com/user-attachments/assets/e748b90f-0a47-4bef-ae49-fb73bc28e255)<br><br><br><br>

&bull; 0.pascal voc 부분을 자신이 만든 라벨링 클래스 이름으로 변경하고 옵션을 box + Label로 변경한다.<br><br>
Change the 0.pascal voc part to the labelling class name you created and change the option to box + label. <br><br>
![그림 4](https://github.com/user-attachments/assets/24837c27-ec26-41b1-a660-6636716529f2)<br><br><br><br>

&bull; open Image Folder로 이미지가 있는 폴더를 선택하여 이미지를 열어 라벨링 해준다. GT Save As로 labels 폴더에 저장하고 GT Load로 불러온다. 라벨 데이터는 텍스트 파일로 저장되고 클래스 번호, 좌표, 너비, 높이로 구성되어 있다.<br><br>
Open Image Folder to open and label the image by selecting the folder with the image. Save As to GT Save As in the labels folder and import to GT Load. Label data is stored as a text file and consists of class number, coordinates, width, and height. <br><br>
![그림 6](https://github.com/user-attachments/assets/c025d91d-f3f3-4ef6-bae1-54b423b4579b)<br><br><br><br>

### Training process # 학습 과정
&bull; 깃허브에서 파일을 clone 하여 yolov5 폴더에 패키지를 설치한다. <br><br>
Install the package in the yolov5 folder by cloning the file on GitHub. <br>
```python
!git clone https://github.com/ultralytics/yolov5 <br>
%cd yolov5 <br>
%pip install -qr requirements.txt <br>
```
<br><br><br><br>
&bull; train, val 폴더에 DarkLabel에서 만든 이미지와 라벨을 넣는다.<br><br>
Put the image and label made by DarkLabel in the train, val folder.<br><br><br><br>

&bull; data.yaml 파일을 classes에 맞게 수정하고 yolov5n.pt 파일과 함께 yolov5 폴더에 넣는다.<br><br>
Modify the data.yaml file to suit the classes and put it in the yolov5 folder with the yolov5n.pt file. <br><br>
![그림 9](https://github.com/user-attachments/assets/e1573800-a471-479f-89f3-b7e5452a5da6)<br>
![그림 8](https://github.com/user-attachments/assets/1af8b748-981d-48e1-b112-8d30950d4866)<br><br><br><br>

&bull; 이미지를 처리하기 위해 Pillow 라이브러리를 설치한다. <br><br>
Install the Pillow library to process the image. <br>
```python
!pip install Pillow==10.3
```

![13](https://github.com/user-attachments/assets/e23ed6bd-34ea-41bf-a538-72e5a302b10a)<br><br><br><br>

&bull; 스크립트를 파이썬으로 학습시키기 위해 train.py를 실행시킨다. 이미지의 크기는 512 x 512, 한번에 처리되는 이미지는 16개, 학습은 300번 반복한다.
해당 경로에 있는 훈련 데이터 및 검증 데이터 경로 등 정보를 포함한 data.yaml과 yolov5n.pt 파일을 사용해 훈련을 한다. cache로 학습 속도를 향상 시킨다.<br><br>

Run train.py to learn the script in Python. The size of the image is 512 x 512, 16 images are processed at a time, and the learning is repeated 300 times.
Train using data.yaml and yolov5n.pt files, including information such as training data and verification data paths in the path. Improve learning speed with cache.<br>
```python
!python train.py  --img 512 --batch 16 --epochs 300 --data /content/drive/MyDrive/yolov5/data.yaml --weights yolov5n.pt --cache
```

![11](https://github.com/user-attachments/assets/ff75c0fb-e007-4580-ae48-e3c68d17437a)<br><br><br><br>

&bull; 학습 과정을 시각화 하기 위해 TensorBoard를 사용한다. runs는 훈련 로그 파일을 저장하는 폴더로 학습이 완료되면 폴더 안에 학습된 파일이 생긴다.<br><br>
TensorBoard is used to visualize the learning process. Runs is a folder that stores training log files, and when learning is completed, a learned file is created in the folder. <br>
```python
%load_ext tensorboard
%tensorboard --logdir runs
```
<br><br><br><br>
&bull; 저장된 훈련 모델을 불러오기 위해 해당 경로에 있는 best.pt 불러온다. train 폴더의 images에 저장된 이미지를 불러와 모델에 입력한다. --conf로 신뢰도를 설정해 준다. 결과는 runs/detect/exp폴더에 저장된다.<br><br>
To retrieve the saved training model, import best.pt in the corresponding path. Import the image stored in the images in the training folder and enter it into the model. Set the reliability with --conf. The results are stored in the runs/detect/exp folder.<br>
```python
!python detect.py --weights /content/drive/MyDrive/yolov5/runs/train/exp/weights/best.pt --img 512 --conf 0.1 --source /content/drive/MyDrive/yolov5/Train/images
```
![12](https://github.com/user-attachments/assets/cf4c92ed-764f-4737-a906-bd7957597b1f)<br><br><br><br>

&bull; 결과가 저장된 폴더에서 앞에서 이미지 10개를 가져와 확인한다.<br><br>
Take 10 images from the front from the folder where the results are saved and check them.<br>
```python
import glob
from IPython.display import Image, display
for imageName in glob.glob('/content/drive/MyDrive/yolov5/runs/detect/exp/*.jpg')[:10]:
    display(Image(filename=imageName))
    print("\n")
```
<br><br><br><br>

&bull; 비디오를 불러와 저장된 훈련 모델로 학습하여 exp폴더에 저장한다.<br><br>
The video is imported and trained with the saved training model and stored in the exp folder.<br>
```python
!python detect.py --weights /content/drive/MyDrive/yolov5/runs/train/exp/weights/best.pt --img 512 --conf 0.1 --source /content/drive/MyDrive/video.mp4
```
<br><br><br><br>

## Training result # 학습 결과
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

## trained video # 학습된 영상 <br>
손상된 상자는 box로 표시된다.<br><br>
The damaged box is marked as box.<br><br>
https://youtube.com/shorts/2ftsguCluPk
