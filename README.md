# Art Unveiled: Enhancing Access to Arts for the Visually Impaired
Our goal is to train a object detection model using various paintings and at the end, we will have audio descriptions from the paintings's tags.

It is essential to run this project using google colab.
You need to create a new folder in your google drive named **_all_data_final_** in which you need to put all the necessary subfolders from the project, in order to execute the .ipynb file.
 
In order to execute this model using your own images, you need to create a directory **_/content/drive/MyDrive/all_data_final/images_** and **_/content/drive/MyDrive/all_data_final/labels_** which will be in a **_YOLO_** format.

<dl type = "circle">In the detect/tune folder, there are:
 <li>the weights of the best and the last model that was tuned. </li>
 <li>The best_hyperparameters.yaml file contains all the tuned hyperparameters</li> 
 <li>the rest files are some plots which indicate how the tuning process took place.</li></dl>
<dl type = "circle">In the final_models folder, there are:
 3 final models which were trained using the hyperparameters above and in the end,<br> <b><i>final_mod_yolov8m_afSiLU_optSGD_epochs50/weights/best.pt</b></i> model was selected for prediction.</dl>
<dl type = "circle">In the predict folder, there are:
 <li>**_XXXXX.jpg_** files corresponds to the images that we predicted.</li>
 <li>XXXXX.txt files corresponds to the actual labels.</li>
 <li>XXXXX_predicted_results.txt files corresponds to the predicted labels.</li>
 <li>XXXXX_description.txt files corresponds to the question that we made to google Bard in order to get an answer description.</li>
 <li>XXXXX_desired_response.txt files corresponds to the answer of google Bard.</li>
 <li>XXXXX_example.mp3 files corresponds to the audio description file for an image.</li>
</dl>
