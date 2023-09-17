# Art Unveiled: Enhancing Access to Arts for the Visually Impaired
Our goal is to train a object detection model using various paintings and at the end, we will have audio descriptions from the paintings's tags.

It is essential to run this project using google colab.
You need to create a new folder in your google drive named **_all_data_final_** in which you need to put all the necessary subfolders from the project, in order to execute the .ipynb file.
 
In order to execute this model using your own images, you need to create a directory **_/content/drive/MyDrive/all_data_final/images_** and **_/content/drive/MyDrive/all_data_final/labels_** which will be in a **_YOLO_** format.

<dl>In the detect/tune folder, there are:
 <dd>the weights of the best and the last model that was tuned. </dd>
 <dd>The best_hyperparameters.yaml file contains all the tuned hyperparameters</dd> 
 <dd>the rest files are some plots which indicate how the tuning process took place.</dd></dl>
<dl>In the final_models folder, there are 3 final models which were trained using the hyperparameters above and in the end, **_final_mod_yolov8m_afSiLU_optSGD_epochs50/weights/best.pt_** model was selected for prediction.</dl>
