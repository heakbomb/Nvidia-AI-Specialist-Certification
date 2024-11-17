# Nvidia AI Specialist Certification

## Title

Real-time road traffic sign detection and analysis system using cameras and artificial intelligence

## Opening background information

</aside>

---

Recently, the importance of driver assistance systems has been increasing as much as the advancement of autonomous driving technology. The traffic sign detection and analysis system helps to operate safely and effectively while driving by recognizing and analyzing the surrounding environment in real-time.

## General description of the current project

---

**This project uses cameras to detect and analyze each traffic sign in real-time through AI, and then relays this information to the driver while they are driving.**

## **Proposed idea for enhancements to the project**

---

**It helps to automatically recognize traffic signs that could be missed in complex road situations, alerting the driver and thus reducing accidents or cases of deviating onto incorrect routes.**

## **Current limitations**

---

There are issues with the system not accurately detecting signs when they are obscured by other objects or environmental factors, and there is a need for improvements in real-time processing requirements and performance.

- Traffic signs recognized by artificial intelligence

![%EC%BA%A1%EC%B2%98](https://github.com/user-attachments/assets/9eeb8c08-d485-4b42-a154-de0609ca6955)

## Video Acquisition Method

---

I recorded the video from inside a moving car.

## - DarkLabel

**The video is cropped to fit 640x640.**

https://www.vapshion.com/vapshion4/download.php

![640_%EC%9E%90%EB%A5%B4%EA%B8%B0](https://github.com/user-attachments/assets/68bc7ff0-30da-44a8-af9b-3ce8f4251597)

[DarkLabel.zip](https://drive.google.com/file/d/1FZcUJKofjROzEBYMR7yUWmWs4OAhcEfp/view?usp=drive_link)

**Unzip the zip file and open the ‘darklabel.yml’ file to add classes for the content to be extracted.**

## - darklabel.yml

![%EB%82%B4%EC%9A%A9_%EC%88%98%EC%A0%95_1](https://github.com/user-attachments/assets/f8ec7b8a-6888-428c-a681-1c4f996d2108)


<aside>

💡format9:    # pascal voc & imagenet (predefined format]
     fixed_filetype: 0                 # if specified as true, save setting isn't changeable in GUI
     data_fmt: [classid, ncx, ncy, nw, nh]
     gt_file_ext: "txt"                # if not specified, default setting is used
     gt_merged: 0                    # if not specified, default setting is used
     delimiter: " "                    # if not spedified, default delimiter(',') is used
     classes_set: "sign_classes"      # if not specified, default setting is used
     name: "sign"              # if not specified, "[fmt%d] $data_fmt" is used as default format name

</aside>

![image](https://github.com/user-attachments/assets/8a6d8084-d835-4cb5-845b-6d018d59f323)


**Open Video: Load the desired video or image.**

**Open Image Folder: Load a folder containing multiple images.**

**0.pascal voc select bar: Specify the formatting style. Here, select the class name you will be labeling.**

## Training video

[https://drive.google.com/drive/folders/1uzY9UreLnw8u5mtnr0VaUOyNlvp5RQex?usp=drive_link](https://drive.google.com/drive/folders/1uzY9UreLnw8u5mtnr0VaUOyNlvp5RQex?usp=drive_link)

**Click 'Open Video' to select the video to extract.**

![dark](https://github.com/user-attachments/assets/5af6cce2-7166-492c-a906-2c8fbea8aa27)

**Click 'as Images..' to convert it to images.**

![image_%EC%9E%90%EB%A5%B4%EA%B8%B0](https://github.com/user-attachments/assets/fb0d9db3-7e42-4cf5-a30b-759438b732cb)

**Load the converted images into DarkLabel.**

![1](https://github.com/user-attachments/assets/02ea7583-66c9-4662-a46e-627a22a11e60)

**Check the Box + Label and label 'sign'.**

![2](https://github.com/user-attachments/assets/8e7e52fc-4a27-4fa1-b79f-5ec5942eea77)

**Click 'GT Save As..' to save the labeled images.**

![3](https://github.com/user-attachments/assets/9c18ad96-8627-4397-9658-7e6e52091a33)

## Training

**Enable recognition of file paths.**

![1](https://github.com/user-attachments/assets/38502540-1b35-4255-8cb2-1887e8a7e73b)

**Install the necessary files for YOLOv5.**

![2](https://github.com/user-attachments/assets/a7156a0c-81bc-46fb-b913-08058c529b69)

**Create Train and Val folders, and save the image files created with DarkLabel and the labeled files.**

![3](https://github.com/user-attachments/assets/fc7589e5-1259-4e0a-b8b6-c665693d0500)

**Create validation data and check the dataset.**

![4](https://github.com/user-attachments/assets/046d3d29-a73f-43ff-8bff-8988e59d0fc2)

**Begin training.**

![5](https://github.com/user-attachments/assets/cd63be9f-7183-4539-9b0d-bdf4678337ea)

![6](https://github.com/user-attachments/assets/c67f30b2-14a5-4144-a662-87772d43e814)

![7](https://github.com/user-attachments/assets/1ca53b74-27b4-45f1-b55d-99e38651b094)

**After the training is complete, check the training values through TensorBoard and input the video for validation and run it.**

![8](https://github.com/user-attachments/assets/897091a5-6bb0-4340-a6ec-4cc15f432a03)

![9](https://github.com/user-attachments/assets/ab62ec86-4a42-401d-b31d-da04d00ee692)

## Training results

![results](https://github.com/user-attachments/assets/b7ea41b3-94c0-48d8-9b00-d9c3bae23869)

## Google Drive YOLOv5 files & validation video

[https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing](https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing)

https://drive.google.com/drive/folders/182YmCgO1SYBkHNi2efWMQp0M6wlRHCx_?usp=sharing
