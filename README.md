# destek4
Stop Sign Detection with YOLOv5

# YOLOv5'i klonla ve kütüphaneleri yükle
git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt
pip install torch torchvision numpy opencv-python matplotlib pyyaml

# modeli eğit (dosya yoluna dikkat et)
python train.py --img 640 --batch 16 --epochs 50 --data "/Users/mars/Downloads/rover4/data.yaml" --weights yolov5s.pt --name stop_sign

# modeli test et 
python detect.py --weights runs/train/stop_sign/weights/best.pt --source /Users/mars/yolov5/images/stop1.jpg --imgsz 640 --conf-thres 0.25
