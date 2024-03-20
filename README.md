<h2> Image Classification using SwinV2 Vision Transformer </h2>
<b> Data Source: Zindi </b></br>
<b> URL: https://zindi.africa/competitions/cgiar-crop-damage-classification-challenge </b></br></br>

This code was developed to classify crops into five categories - Good growth (G), Drought (DR), Nutrient Deficient (ND), Weed (WD), and Other. Specifically, a "tiny" Swin transformer V2, which was pretrained on ImageNet-1k data set at 256 x 256 resolution, was fine-tuned using Zindi's data set.
<br>

The training dataset is unbalanced as shown below - 
| **Class**      | **Number of images**|
| :---       |    :----|
|G        | 11623 |
|WD       | 9238  |
|DR       | 4516  |
|Other    | 419   |
|ND       | 272   |

and a ML practioner might want to augment images in the last two classes (namely, Other and ND) prior to model training. Further, the practitioner may want to evaluate the impact of regularization on the model's performance on test data set. 

A preliminary analysis of this data showed that even classes with 4000+ samples had high classification error. Consequently, multiple data transformation methods (geometric and photometric transformations) were considered for all the classes. The notebooks contain code for various image transformations and customized classes for evaluating the effect of learning rate, regularization (via dropout), and number of epochs on the model's performance.
