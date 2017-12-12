# FaceDetectionAndRecognition
参考自博客：http://www.cnblogs.com/neo-T/p/6511273.html
本项目实现了从USB摄像头或者电脑摄像头中获取实时视频流（getVideo.py），从视频流中检测人脸（faceDetect.py）并保存人脸图片（getMyfaces.py）。对人脸图片进行训练（face_train_use_keras.py），在实时视频流上预测是否为本人（face_predict_use_keras.py）。  

运行步骤：  

1.新建保存人脸图片的文件夹，在项目根目录里打开命令行，输入 python getMyfaces.py 0 200 user1 ，其中0为摄像头的编号，200为采集的图片数，user1为文件名，然后即可自动开启摄像头采集人脸图像。  

2.筛选出一定张数的人脸图片，在项目根目录里打开命令行，输入 python load_face_dataset.py user1，其中user1 为人脸图片的文件夹目录.  

3.运行face_train_use_keras.py  

4.运行face_predict_use_keras.py  

注：也可以不用在命令行中输入.py文件加设备号（0）的方式运行，可以注释掉main里的if判断，在cv2中的需要调用摄像头设备号的函数里直接写0。
