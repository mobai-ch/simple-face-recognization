# simple-face-recognization
It'a a simple course about how to do face recognization using openCV.(updating)

At first, you have to have a idea about how to use python tools such as pip3 or setup.py, I won't let you know the code directly, but you can learn how to do it step by step.

Next, you have to download the ORL dataset accroding to the task recommadation.
Because of some reason we can't discribe, we choose to use Baidu-yun, and the link show at next line.

URL: [https://pan.baidu.com/s/178K357kYHhaJnYGyGI76Rg](https://pan.baidu.com/s/178K357kYHhaJnYGyGI76Rg)

password: o6e0

Thanks for the Contribution of deana_.

And now, you will find something Strange, why the format of Image is PGM, If you try to understand, you can click the url follow ([http://netpbm.sourceforge.net/doc/pgm.html](http://netpbm.sourceforge.net/doc/pgm.html)), though I don't recommand you to do it for you will waste at least one hour in your life.

All right, please download some module for this work. Open your terminal and input it.

> pip3 install -i https://pypi.douban.com/simple opencv-python <br>
> pip3 install -i https://pypi.douban.com/simple opencv-contrib-python <br> 
> pip3 install -i https://pypi.douban.com/simple matplotlib

After that, you can simply read image by the code follow

> img = cv2.imread("path of the image") <br>
> cv2.imshow("mat", img) <br>
> cv2.waitKey(0)

you will see a face from ORL Dataset

## Key Point
Now, I will show you the key point of this project.As we all know, face recognization is essentially a few-shot problem. We have only few sample to recognize a new object unknow.The general method based on metric learning is encoding the face into vector, and judge the face by KNN, K-means or its' Gussian Distribution.

In order to achieve this, we have to find some module which have already finished this function.

Opencv have prepared three face recognizer, but I recommand you use something else such as dlib or train a model by Siamese Network.

> EigenFaces: cv2.face.createEigenFaceRecognizer() <br>
> FisherFaces: cv2.face.createFisherFaceRecognizer() <br>
> LBPH: cv2.face.createLBPHFaceRecognizer()

And you can train your recognizer as follow:

> face_recognizer.train(faces, np.array(labels)) <br>
>  <br>
> faces: List of face rect <br>
> labels: List of face label, you should encode one in same number. <br>

Finally, you can simply test the result of it.

>  face_recognizer.predict(face) <br>
>  face: face image rect <br>

## Finally
I found some task about Data analysis, try to use matplotlib and pandas make figures. It's not hard but very troublesome. Good Luck!

