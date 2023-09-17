# Art Unveiled: Enhancing Access to Arts for the Visually Impaired
Our goal is to train a object detection model using various paintings and at the end, we will have audio descriptions from the paintings's tags.

It is essential to run this project using google colab.
You need to create a new folder in your google drive named **_all_data_final_** in which you need to put all the necessary subfolders from the project, in order to execute the .ipynb file.
 
In order to execute this model using your own images, you need to create a directory **_/content/drive/MyDrive/all_data_final/images_** and **_/content/drive/MyDrive/all_data_final/labels_** which will be in a **_YOLO_** format.

<dl type = "circle">In the <b><i>detect/tune</b></i> folder, there are:
 <li>the <b><i>weights</b></i> of the best and the last model that was tuned. </li>
 <li>The <b><i>best_hyperparameters.yaml</b></i> file contains all the tuned hyperparameters</li> 
 <li>the rest files are some <b><i>plots</b></i> which indicate how the tuning process took place.</li></dl>
<dl type = "circle">In the <b><i>final_models</b></i> folder, there are:
 <li>3 final models which were trained using the hyperparameters above and in the end, <b><i>final_mod_yolov8m_afSiLU_optSGD_epochs50/weights/best.pt</b></i> model was  selected for prediction.</li></dl>
<dl type = "circle">In the <b><i>predict folder</b></i>, there are:
 <li><b><i>XXXXX.jpg</b></i> files corresponds to the images that we predicted.</li>
 <li><b><i>XXXXX.txt</b></i> files corresponds to the actual labels.</li>
 <li><b><i>XXXXX_predicted_results.txt</b></i> files corresponds to the predicted labels.</li>
 <li><b><i>XXXXX_description.txt</b></i> files corresponds to the question that we made to google Bard in order to get an answer description.</li>
 <li><b><i>XXXXX_desired_response.txt</b></i> files corresponds to the answer of google Bard.</li>
 <li><b><i>XXXXX_example.mp3</b></i> files corresponds to the audio description file for an image.</li></dl>
<dl type = "circle">In the <b><i>train</b></i> folder, there is our training dataset with:
 <li>All the <b><i>images</b></i> used to train and tune our models </li>
 <li>All the corresponding <b><i>labels</b></i> of the training images </li></dl>
<dl type = "circle">In the <b><i>trained_models</b></i> folder, there are:
 <li><b><i>36</b></i> models which were trained in order to find the best model before tuning.</li></dl>
<dl type = "circle">In the <b><i>val</b></i> folder, there is our validation dataset with:
 <li>All the <b><i>images</b></i> used to evaluate our models </li>
 <li>All the corresponding <b><i>labels</b></i> of the evaluated images </li></dl>
<dl type = "circle">The remaining files are explained below:
 <li><b><i>best_model_final.pt</b></i> is a torch.save of our model, containing both weights and other parameters </li>
 <li><b><i>best_model_info.csv</b></i> is a .csv file containing 4 metrics for the 3 final models which are located in <b><i>final_models</b></i> directory.<br>
 With the mean of those 4 metrics(mean precision, mean recall, mean Average Precision (mAP) at an IoU threshold of 0.5 and mean Average Precision (mAP) over IoU thresholds of 0.5 - 0.95 in steps of 0.05), we decided which is the final model for predictions.</li></dl>
