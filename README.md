# YOLOv7_EntryTest
Bước 1: Mount Google Colab với Drive
```
import os
os.chdir('/content/drive/MyDrive/YOLOv7')
```
Bước 2: Tải (clone) mô hình YOLOv7 bằng link Github
```
!git clone https://github.com/WongKinYiu/yolov7.git
```
Bước 3: Chuyển thư mục làm việc hiện tại đến thư mục yolov7 và cài đặt các thư viện cần thiết để chạy mô hình
```
%cd yolov7
!pip install -r requirements.txt
```
Bước 4: Chạy code Train mô hình bên dưới. Các tham số quan trọng của mô hình:
  --epochs 'số vòng huấn luyện'
  --data 'data path'
  --img 'kích thước ảnh huấn luyện'
  --cfg 'file yolo config'
  --weight 'weight pretrain model'
  --hyp 'config các giá trị hyperparameters'
```
!python train_custom.py --workers 4 --epochs 10 --batch-size 8 --data data/custom.yaml --img 640 640 --cfg cfg/training/yolov7.yaml --weights 'yolov7.pt' --name yolov7-custom --hyp data/hyp.scratch.custom.yaml
```
