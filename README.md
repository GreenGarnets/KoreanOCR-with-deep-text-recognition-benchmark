# Korean OCR with clova ai's deep-text-recognition-benchmark

#### korean prediction results

| demo images | [TPS-ResNet-BiLSTM-Attn korean](https://drive.google.com/file/d/1AOucYNbIvzclpurXVAFiBi7imrNMFjVJ/view?usp=sharing) | 
| ---         |        --- |
| <img src="./demo_image/0.jpg" width="400" height="130">      |    서울대역    |  
| <img src="./demo_image/0_.jpg" width="400" height="130">      |    상설    |  
| <img src="./demo_image/2.jpg" width="400" height="130">      |    영어전문학원    |   
| <img src="./demo_image/3.jpg" width="400" height="130">      |    아카데미    | 
| <img src="./demo_image/5.jpg" width="400" height="130">      |    대형출력인쇄    | 
| <img src="./demo_image/demo_1.png" width="300">    |   available   |  

<img src="./figures/koreanTest.PNG">

We have added Korean to the project and modified it for reading. trainings studied 500000 sets of [Korean](http://ptak.felk.cvut.cz/public_datasets/SyntText/Korean.zip) and English datasets made using synth text, and the examples of those datasets are as follows.

| Trainning images | GT text | 
| ---         |        --- |
| <img src="./Assets/15.jpg" width="260" height="140">      |    항자원    |  
| <img src="./Assets/32.jpg" width="260" height="140">      |    신청을    |  
| <img src="./Assets/291702.jpg" width="260" height="140">      |    Polizei!    |  
| <img src="./Assets/291724.jpg" width="260" height="140">      |    때문에    |  
| <img src="./Assets/291727.jpg" width="260" height="140">      |    소비가    |  

After securing the Korean data set, input is required to the Korean string.<br>
We modified train.py and saved Korean consonants in the file [KoreanCodec.txt](https://github.com/GreenGarnets/KoreanOCR-with-deep-text-recognition-benchmark/blob/master/koreanCodec.txt) so that we could call it up.<br>

model downlaod : [TPS-ResNet-BiLSTM-Attn-korean.pth](https://drive.google.com/file/d/1AOucYNbIvzclpurXVAFiBi7imrNMFjVJ/view?usp=sharing)
Please contact me if there is a problem with the model.

If the OCR image is corrected for tilting and further learning, 99.922% of the accuracy of the Korean OCR was shown, but the model cannot be disclosed due to the research project contract. 

|  <center>Predict</center> |  <center>GT</center> |  <center>Result</center> |
|:--------:|:--------:|:--------:|
|<center>배산공원 </center> | <center>배산공원 </center> |True |
|<center>87 </center> | <center>87 </center> |True |
|<center>300m </center>| <center>300m </center> |True |
|<center>분당소방서 </center>| <center>분당소방서 </center> |True |
|<center>시의회 </center>| <center>시의회 </center> |True |

[100000/100000] **Train Loss: 0.00663** elapsed_time: 2609.21140<br>
[100000/100000] **valid loss: 0.00391** **accuracy: 99.922**, norm_ED: 0.83

