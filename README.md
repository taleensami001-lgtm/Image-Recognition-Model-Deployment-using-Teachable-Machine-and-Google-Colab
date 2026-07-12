# **Building an Image Recognition Model                      بناء نموذج للتعرف على الصور**
 



## **- إعداد الفئات ورفع البيانات التدريبية (Setting up Classes and Uploading Training Data)**

تبدأ الخطوة الأولى بفتح منصة Google Teachable Machine واختيار مشروع صور (Image Project). يتم بعد ذلك تحديد وتسمية الفئات (Classes) المراد تدريب النموذج عليها. في هذا المشروع، تم إنشاء ثلاث فئات لأنواع مختلفة من الزهور: الزنبق (Lily)، تباع الشمس (Sunflower)، والتوليب (Tulip). بعد تسمية الفئات، يتم رفع مجموعة من الصور التمثيلية لكل زهرة من جهاز الكمبيوتر لتدريب النموذج عليها.

The first step begins by opening the Google Teachable Machine platform and selecting an Image Project. Next, the categories (Classes) that the model will be trained on are defined and named. In this project, three classes were created for different types of flowers: Lily, Sunflower, and Tulip. After naming the classes, a set of representative images for each flower is uploaded from the local computer to serve as training data.

1- 
![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/2a95de519c5e70aadd9f9abfb7e209d70b7e0a4b/Screenshot%202026-07-12%20152535.png)

2-
![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/adb9e17548048c66296dcc666cf6d6a9bd599731/Screenshot%202026-07-12%20152700.png)


## **- تدريب النموذج (Training the Model)**

بعد الانتهاء من إدراج الصور في كل فئة، يتم النقر على زر Train Model (تدريب النموذج) الموجود في المنتصف. تقوم المنصة خلال هذه المرحلة بمعالجة البيانات المرفوعة وبناء شبكة عصبية قادرة على التمييز بين أنواع الزهور الثلاثة بناءً على الخصائص البصرية لكل فئة.

Once the images are populated into each class, the next step is to click the Train Model button located in the center panel. During this phase, the platform processes the uploaded data and builds a neural network capable of distinguishing between the three flower types based on the visual features of each class.


![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/adb9e17548048c66296dcc666cf6d6a9bd599731/Screenshot%202026-07-12%20152754.png)


## **- اختبار وتقييم النموذج (Testing and Evaluating the Model)**

بمجرد اكتمال التدريب، ننتقل إلى قسم المعاينة (Preview) لاختبار دقة النموذج. يتم رفع صور اختبارية جديدة (لم يتم استخدامها في التدريب) للزهور الثلاثة. كما يظهر في النتائج، أظهر النموذج كفاءة عالية حيث تعرف على صورة زهرة "تباع الشمس" بنسبة دقة 100%، وتعرف على "التوليب" بنسبة 100%، وتعرف على "الزنبق" بنسبة 99%.

Once training is complete, we move to the Preview section to test the model's accuracy. New test images (which were not part of the training set) of the three flowers are uploaded. As shown in the results, the model demonstrated high efficiency, recognizing a "Sunflower" image with 100% confidence, a "Tulip" with 100% confidence, and a "Lily" with 99% confidence.


![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/9357060dcc027cbbe2f71513ba8ed43c1d513983/Screenshot%202026-07-12%20153033.png)


![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/9357060dcc027cbbe2f71513ba8ed43c1d513983/Screenshot%202026-07-12%20153050.png)


![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/2c1c7084a4d2212a053536d1918ff09ebf40a43e/Screenshot%202026-07-12%20153554.png)


![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/2c1c7084a4d2212a053536d1918ff09ebf40a43e/Screenshot%202026-07-12%20153626.png)


## **- تصدير النموذج (Exporting the Model)**

لاستخدام هذا النموذج في بيئة برمجية خارجية، يتم النقر على زر Export Model (تصدير النموذج). من النافذة المنبثقة، يتم اختيار تبويب Tensorflow ثم تحديد نوع التحويل ليكون Keras. بعد ذلك، يتم النقر على Download my model لتحميل ملفات النموذج (keras_model.h5 و labels.txt) إلى جهاز الكمبيوتر. كما توفر المنصة كود Python جاهزاً لاستخدامه في تشغيل النموذج.

To utilize this model in an external programming environment, the Export Model button is clicked. From the pop-up window, the Tensorflow tab is selected, and the conversion type is set to Keras. After that, clicking Download my model saves the model files (keras_model.h5 and labels.txt) to the local computer. The platform also provides a ready-to-use Python code snippet for running the model.

![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/507c828d1d198fa7a707b417d946440032c5727a/Screenshot%202026-07-12%20153800.png)

## **- تطبيق النموذج في بيئة Google Colab (Deploying the Model in Google Colab)**

الخطوة الأخيرة تتمثل في الانتقال إلى بيئة Google Colab. يتم إنشاء مستند تفاعلي جديد (Notebook) ونسخ كود Python الذي تم الحصول عليه في الخطوة السابقة ولصقه في خلية الأكواد. من خلال لوحة الملفات الجانبية في Colab، يتم رفع ملف النموذج (keras_model.h5) وملف التسميات (labels.txt) وصورة اختبارية (مثل images (2).jpeg). يتم تعديل مسار الصورة في الكود ليتطابق مع اسم الصورة المرفوعة، ثم يتم تشغيل الخلية لتنفيذ الكود والحصول على التنبؤ النهائي للنموذج برمجياً.


The final step involves transitioning to the Google Colab environment. A new Notebook is created, and the Python code snippet obtained in the previous step is pasted into a code cell. Using the file explorer panel on the left side of Colab, the downloaded model file (keras_model.h5), the labels file (labels.txt), and a test image (e.g., images (2).jpeg) are uploaded. The image path within the code is then modified to match the uploaded test image's name. Finally, the cell is executed to run the script and generate the model's final prediction programmatically.

![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/507c828d1d198fa7a707b417d946440032c5727a/Screenshot%202026-07-12%20154359.png)

![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/507c828d1d198fa7a707b417d946440032c5727a/Screenshot%202026-07-12%20164535.png)

![img alt](https://github.com/taleensami001-lgtm/Image-Recognition-Model-Deployment-using-Teachable-Machine-and-Google-Colab/blob/507c828d1d198fa7a707b417d946440032c5727a/Screenshot%202026-07-12%20164535.png)