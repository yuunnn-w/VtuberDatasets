# 虚拟主播数据集(Vtuber&Vup Dataset)
## 项目介绍(Project Introduction)
  - 这是一个Vtuber和Vup（即虚拟主播）的目标检测（yolov）数据集仓库，包括18名Vtuber/Vups。  
  - 数据集由小阳（我）建立并开源，数据来源是互联网以及各大主播在Bilibili的动态图片。  
  - This is a warehouse of object detection (yolov) datasets for Vtuber and Vup (i.e., virtual streamers), including 18 Vtuber/Vups.  
  - The dataset was built and open source by Xiaoyang小阳 (I), and the data source is the Internet and the dynamic pictures of these Vtuber/Vups on Bilibili.  
## 使用范例(Usage examples)  
  - 您可以将本数据集用于训练任意的目标检测模型，具体的训练方法请参考对应的模型介绍。  
  - 以下是虚拟主播目标检测示例，采用yolov5m模型进行检测。 
  - You can use this dataset to train any object detection model, please refer to the corresponding model introduction for specific training methods.
  - The following is an example of Vtuber/Vups anchor target detection, which is detected using the Yolov5m model.  
### 顾子韵GZY 
![Image text](https://raw.githubusercontent.com/JiaXinSugar-114514/Vtuber-Vup-Dataset/main/gzy.jpg)
## 数据集介绍(Introduction to datasets)
### 数据集格式(Dataset format)  
  - 采用labelimg软件进行标注，标签标注格式为yolov格式，和每一类的图片存放在同一个文件夹下。  
  - 共有1904张Vtuber/Vups的图片，其中有1841张图片作为训练集，63张图片作为测试集。  
  - 数据集中每一个文件夹的名字就是一位虚拟主播的代号，这里采用拼音命名和主播自己的英文名结合的方法给主播命名。  
  - 文件夹下面即可看到对应的图片和标签，在根目录下也可以看到包含所有类别名字的classes.txt文件。  
  - Use labelimg software for annotation, label labeling format is yolov format, and each type of picture is stored in the same folder.  
  - A total of 1904 Vtuber/Vups images, including 1841 images as training sets and 63 images as test sets.  
  - The name of each folder in the dataset is the code name of a virtual host, and the method of combining pinyin naming and the host's own English name is used to name the host.  
  - The corresponding pictures and tags can be seen under the folder, and the .txt file containing all the category names can also be seen in the root directory.  
### 数据集内容(Dataset content)
  - 数据集包含18位Vtuber/Vups，他们的类别名字如下：  
  - The dataset contains 18 Vtuber/Vups with the following class names:  
    - Nana7mi 七海娜娜米(123 images)  
    - DongXueLian 东雪莲(75 images)  
    - BingTangIO 冰糖IO(153 images)  
    - MieLi 咩栗(109 images)  
    - Diana 嘉然(91 images)  
    - Taffy 塔菲(122 images)  
    - DaSi 大思(凜凜蝶凜)(30 images)  
    - MingQianNaiLv 明前奶绿(40 images)  
    - XiaoKe 小可学妹(98 images)  
    - XingTong 星瞳(92 images)  
    - TaoJiOvO 桃几OvO(48 images)  
    - LingYuan_yousa 泠鸢(122 images)  
    - ShenLeQiNai_KaguraNana 神樂七奈(154 images)  
    - MaoLei_Nyaru 猫雷(94 images)  
    - KizunaAI 绊爱(101 images)  
    - Azi 阿梓(107 images)  
    - GZY_w 顾子韵(31 images)  
    - Mayumi 麻尤米(42 images)
  
  - 另外，数据集还包含一些未指定标签的虚拟主播形象：
  - In addition, the dataset contains some Vtuber/Vups images without labels:
    - Other 其他(209 images)
  
  - 以上就是全部用于训练的数据集，共计1841张图片，后续如果作者有时间会持续更新并扩充数据集。值得注意的是，该数据集不是平衡的，各个类别图片数量的差距较为巨大，这是由于不同虚拟主播的知名度有所差异，所以每个虚拟主播图片的丰富程度也不尽相同。  
  - 以下是该数据集在yolov5s模型上训练得到的混淆矩阵和Precision-Recall曲线图：
  - The above is all the dataset used for training, a total of 1841 images, and the author will continue to update and expand the dataset if he has time.It is worth noting that the dataset is not balanced, and the difference in the number of images in each category is relatively large, which is due to the difference in the popularity of different Vtuber/Vups, so the richness of each Vtuber/Vups picture is not the same.  
  - The following is the confusion matrix and Precision-Recall graph obtained by training on the yolov5s model of this dataset:  
<img src="https://raw.githubusercontent.com/JiaXinSugar-114514/Vtuber-Vup-Dataset/main/confusion_matrix.png" width="450px"><img src="https://raw.githubusercontent.com/JiaXinSugar-114514/Vtuber-Vup-Dataset/main/PR_curve.png" width="500px">
  - 可以看出，模型对DongXueLian东雪莲和LingYuan_yousa泠鸢这两个类别的分类效果不是很令人满意，这是由于这两个虚拟主播的形象过于丰富，且在二创作品中的形象过于多变且模糊所造成。如果您想要使用我的数据集来进行分类，请千万注意，如果分类效果不佳，您需要优先考虑这是否是由数据集本身的缺点所引起的，而不是您的原因。
  - It can be seen that the classification effect of the model on the two categories of Dongxuelian and LingYuan_yousa is not very satisfactory, which is caused by the images of these two Vtuber/Vups is too rich, and the images painted by their fans is too changeable and blurry. if you want to use my dataset for classification, please pay attention to it, if the classification effect is not good, you need to prioritize whether this is caused by the shortcomings of the dataset itself, not your reasons.
### 数据来源(Data sources)
  - 该数据集所包含的虚拟主播图片主要来自于他们自己在Bilibili平台所发布的动态中所包含的图片，并利用爬虫技术下载下来，还有一部分来自谷歌搜索引擎，经过我的人工筛选和清洗，剔除掉一些重复的图片和无意义的图片，选取一些有代表性的图片，最终得到完整的数据集。
  - 图片数据不仅包含虚拟主播自己的官方形象，还有一些由粉丝们创作的二创作品也被收录其中，从而能够做到识别二创的目的。
  - The Vtuber/Vups images contained in this dataset are mainly from the pictures contained in their own dynamics published on the Bilibili platform, and downloaded using crawler technology, and some are from the Google search engine, after my manual screening and cleaning, eliminate some duplicate pictures and meaningless pictures, select some representative pictures, and finally get the complete dataset.
  - The image data not only contains the official image of the Vtuber/Vups herself, but also some secondary creations created by fans, so as to achieve the purpose of identifying the second creation.
## 关于我(About me)
  - 我是一位还在就读大学三年级的本科生(2022年)，建立此数据集也单纯的是出于兴趣爱好。  
  - 如果您对我的数据集有任何疑问，或是该数据集涉及了一些版权问题等，请联系我。  
  - 您可以称呼我为小阳，您可以通过如下两种方式联系到我：  
    - 我的邮箱是：jiaxinsugar@gmail.com。  
    - 您也可以在哔哩哔哩平台上私信我，我的哔哩哔哩UID:436636983。  
  - I am a third-year undergraduate student (2022), and I built this dataset purely out of interest.  
  - If you have any questions about my dataset, or if the dataset involves some copyright issues, etc., please contact me.  
  - You can call me Xiaoyang小阳, you can contact me in two ways:  
    - My email address is: jiaxinsugar@gmail.com。  
    - You can also send me a private message on the Bilibili platform, My Bilibili UID: 436636983。  
