<h2> Image Classification using SwinV2 vision transformer </h2>

This code was developed to classify crops into five categories: Good growth (G), Drought (DR), Nutrient Deficient (ND), Weed (WD), and Other and the details are available on Zindi's website (https://zindi.africa/competitions/cgiar-crop-damage-classification-challenge). <br>

The training dataset is unbalanced as shown below - 
| **Class**      | **Number of images**|
| :---       |    :----|
|G        | 11623 |
|WD       | 9238  |
|DR       | 4516  |
|other    | 419   |
|ND       | 272   |

and a ML practioner might want to augment the images in the last two classes - other and ND - prior to model training. Further, the practitioner may want to evaluate the impact of regularization on the model's performance on test data set. To account for these two requirements, the code considers two types of transformations (geometric and photometric) and uses a custom config file to control the extent of regularization.
