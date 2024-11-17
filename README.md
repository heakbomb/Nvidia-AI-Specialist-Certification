# Nvidia AI Specialist Certification

## Title

Real-time road traffic sign detection and analysis system using cameras and artificial intelligence

## Opening background information

</aside>

---

Recently, the importance of driver assistance systems has been increasing as much as the advancement of autonomous driving technology. The traffic sign detection and analysis system helps to operate safely and effectively while driving by recognizing and analyzing the surrounding environment in real-time.

## General description of the current project

---

This project uses cameras to detect and analyze each traffic sign in real-time through AI, and then relays this information to the driver while they are driving.

## **Proposed idea for enhancements to the project**

---

It helps to automatically recognize traffic signs that could be missed in complex road situations, alerting the driver and thus reducing accidents or cases of deviating onto incorrect routes.

## **Current limitations**

---

There are issues with the system not accurately detecting signs when they are obscured by other objects or environmental factors, and there is a need for improvements in real-time processing requirements and performance.

- Traffic signs recognized by artificial intelligence

![%EC%BA%A1%EC%B2%98](https://github.com/user-attachments/assets/115201bc-46f9-433f-acff-1744f3537c02)

## Video Acquisition Method

---

I recorded the video from inside a moving car.

## - DarkLabel

**The video is cropped to fit 640x640.**

https://www.vapshion.com/vapshion4/download.php

![640_%EC%9E%90%EB%A5%B4%EA%B8%B0](https://github.com/user-attachments/assets/2b52d418-ca3a-4497-8243-51e3e9a2c77e)

https://github.com/heakbomb/Nvidia-AI-Specialist-Certification/blob/main/DarkLabel2.4.zip

**Unzip the zip file and open the ‘darklabel.yml’ file to add classes for the content to be extracted.**

## - darklabel.yml

![%EB%82%B4%EC%9A%A9_%EC%88%98%EC%A0%95_1](https://github.com/user-attachments/assets/6c52bf2c-b512-434f-90d2-9ba505bf0725)

```
💡format9:    # pascal voc & imagenet (predefined format]
     fixed_filetype: 0                 # if specified as true, save setting isn't changeable in GUI
     data_fmt: [classid, ncx, ncy, nw, nh]
     gt_file_ext: "txt"                # if not specified, default setting is used
     gt_merged: 0                    # if not specified, default setting is used
     delimiter: " "                    # if not spedified, default delimiter(',') is used
     classes_set: "sign_classes"      # if not specified, default setting is used
     name: "sign"              # if not specified, "[fmt%d] $data_fmt" is used as default format name
```


![image](https://github.com/user-attachments/assets/98903e0d-6c2d-4b39-bc39-fa1cf8e89105)

**Open Video** : Load the desired video or image.

**Open Image Folder** : Load a folder containing multiple images.

**0.pascal voc select bar** : Specify the formatting style. Here, select the class name you will be labeling.

## Training video

[https://drive.google.com/drive/folders/1uzY9UreLnw8u5mtnr0VaUOyNlvp5RQex?usp=drive_link](https://drive.google.com/drive/folders/1uzY9UreLnw8u5mtnr0VaUOyNlvp5RQex?usp=drive_link)

**Click 'Open Video' to select the video to extract.**

![dark](https://github.com/user-attachments/assets/55396612-fbda-46f4-9a08-562d72931e13)

**Click 'as Images..' to convert it to images.**

![image_%EC%9E%90%EB%A5%B4%EA%B8%B0](https://github.com/user-attachments/assets/bd0c84b4-9fd1-482b-adcc-04f305b7897f)

**Load the converted images into DarkLabel.**

![1](https://github.com/user-attachments/assets/da3488ec-a634-4a60-a60d-92bfa1b4b003)

**Check the Box + Label and label 'sign'.**

![2](https://github.com/user-attachments/assets/e8d072c8-a504-45b3-9ec3-baacf239c978)

**Click 'GT Save As..' to save the labeled images.**

![3](https://github.com/user-attachments/assets/2790f696-2e67-4b4f-bf86-48c0d2768c1c)

## Training

**Enable recognition of file paths.**

![1](https://github.com/user-attachments/assets/1651542f-2ecd-4375-9d23-bc4559390f01)

**Install the necessary files for YOLOv5.**

![2](https://github.com/user-attachments/assets/252ca093-189c-4172-97e3-b8ceea66eca7)

**Create Train and Val folders, and save the image files created with DarkLabel and the labeled files.**

![3](https://github.com/user-attachments/assets/1c4c7e09-7a27-4c7e-a40c-402771e97829)

**Create validation data and check the dataset.**

![4](https://github.com/user-attachments/assets/cc42be89-e305-4047-8346-46e024b81d28)

**Begin training.**

![5](https://github.com/user-attachments/assets/d064e299-06b4-4755-b5a0-408f1e6b076a)

![6](https://github.com/user-attachments/assets/0db675c0-b86b-46a9-911b-ef841cc8d049)

![7](https://github.com/user-attachments/assets/4b7e5606-3adf-448b-8f47-1c65935f27f9)

**After the training is complete, check the training values through TensorBoard and input the video for validation and run it.**

![8](https://github.com/user-attachments/assets/11e76a85-01a5-4282-8dd9-a14a8e625336)

![9](https://github.com/user-attachments/assets/3fee01f7-56f5-4912-92c7-b3260c67b309)

---

## Training results

![results](https://github.com/user-attachments/assets/a22121b3-391f-4420-aa9a-0dcf744c9fb7)

## Google Drive YOLOv5 files & validation video

[https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing](https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing)

https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing
