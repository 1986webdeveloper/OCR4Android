# OCR4Android

In this demo we have tried implementing the GoogleOCR to read the text from the image selected from the gallery or captured from the camera.

For this demo, we require two permission : Camera permission and Write external storage permission

Things to keep in mind while implementing googleOCR : 

Dependecies to add  : 
implementation 'com.google.android.gms:play-services-vision:15.0.2'

Manifest changes : 
<meta-data
            android:name="com.google.android.gms.vision.DEPENDENCIES"
            android:value="ocr" />
Note : it is compulsory to add meta-data in manifest for GoogleOCR to work.

Work flow :

First we check if user has granted the permission to write the external storage, if user has not granted then we will show the dialog to the user else wait for the user to click on one of the button either to select image from gallery or capture using camera.

If user clicks on the select image from gallery, we will open the gallery using intent for user to select image. 

If user clicks on the capture image option, we will first check, whether the camera permission is granted or not. If not, then first ask for camera permission, then open camera intent else directly open the camera intent.

Once the user provides us with the image to read from, we will convert the image to bitmap and then will scan image line-by-line for texts and will display it in textview.


Output:

![alt text](http://dev.acquaintsoft.com/ezgif.com-video-to-gif.gif)
