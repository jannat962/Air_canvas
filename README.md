# Air_canvas

エア・キャンバスは、OpenCVのコンピュータ・ビジョン技術を使用して実現されたプロジェクトです。このプロジェクトでは、指先の色のついたカラーマーカーの動きをカメラで検出し、その上に描画することができます。プロジェクトの構築には、色の検出と追跡が使用されます。カラーマーカーが検出され、生成されたマスクに対して形態素演算が行われます。最後に、検出された輪郭の中心座標を連続するフレームのために配列に格納し、それらをフレーム上に描画します。このプロジェクトは、指を振るだけで自在な描画を行うことができるという特徴を持っています。
(Air Canvas is a project realised using OpenCV computer vision technology. The project uses a camera to detect the movement of coloured colour markers on the fingertips and draw on them. Colour detection and tracking is used to build the project. The colour markers are detected and morphological operations are performed on the generated masks. Finally, the centre coordinates of the detected contours are stored in an array for successive frames and they are drawn on the frames. The project is characterised by the ability to draw at will, simply by waving a finger.


Computer vision project implemented with OpenCV

Ever wanted to draw your imagination by just waiving your finger in air. In this post we will learn to build an Air Canvas which can draw anything on it by just capturing the motion of a coloured marker with camera. Here a coloured object at tip of finger is used as the marker.

We will be using the computer vision techniques of OpenCV to build this project. The preffered language is python due to its exhaustive libraries and easy to use syntax but understanding the basics it can be implemented in any OpenCV supported language.

Here Colour Detection and tracking is used in order to achieve the objective. The colour marker in detected and a mask is produced. It includes the further steps of morphological operations on the mask produced which are Erosion and Dilation. Erosion reduces the impurities present in the mask and dilation further restores the eroded main mask.

# Algorithm
1.Start reading the frames and convert the captured frames to HSV colour space.(Easy for colour detection)

2.Prepare the canvas frame and put the respective ink buttons on it. Adjust the trackbar values for finding the mask of coloured marker.

3.Preprocess the mask with morphological operations.(Erotion and dilation)

4.Detect the contours, find the center coordinates of largest contour and keep storing them in the array for successive frames .(Arrays for drawing points on canvas)

Finally draw the points stored in array on the frames and canvas .
Requirements: python3 , numpy , opencv installed on your system.
