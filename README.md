# Art Unveiled: Enhancing Access to Arts for the Visually Impaired
The goal of the current project is to train an object detection model using various art images in order to acquire a final optimised model that will be then used to provide labels for art images which will then be imported to NLP and audio to text tools so that a final audio recording with the description can be produced.

This is a collaborative project for Machine Learning and Context Analytics lesson in Business Analytics at A.U.E.B. Part Time 2022-2024.

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
 We decided which would be the final model for predictions based on the mean of those 4 metrics(<i>mean precision, mean recall, mean Average Precision (mAP) at an IoU threshold of 0.5 and mean Average Precision (mAP) over IoU thresholds of 0.5 - 0.95 in steps of 0.05</i>)</li>
 <li><b><i>best_model_info.xlsx</b></i> is a .xlsx file with the same data as <b><i>best_model_info.csv</b></i> file.</li>
 <li><b><i>classes.txt</b></i> is a .txt file containing all the available classes of our model.</li>
 <li><b><i>data_custom.yaml</b></i> is a .yaml file containing some basic arguments for our initial models.</li>
 <li><b><i>data_custom_final.yaml</b></i> is a .yaml file containing some basic arguments for our final models combined with the tuned hyperparameters located in <b><i>detect/tune/best_hyperparameters.yaml.</b></i></li>
 <li><b><i>model_info.csv</b></i> is a .csv file containing 4 metrics for the 36 initial models which are located in <b><i>trained_models</b></i> directory.<br>
 We decided which is the final model for tuning based on the mean of those 4 metrics(<i>mean precision, mean recall, mean Average Precision (mAP) at an IoU threshold of 0.5 and mean Average Precision (mAP) over IoU thresholds of 0.5 - 0.95 in steps of 0.05</i>).</li>
 <li><b><i>model_info.xlsx</b></i> is a .xlsx file with the same data as <b><i>model_info.csv</b></i> file.</li>
 <li><b><i>notes.json</b></i> is a .json file containing all categories ids with the  corresponding names, provided by <b><i>Label Studio</b></i>.</li>
</dl>

## Example Image with Text and Audio Description

### Image
!["Portrait of Felix Auerbach" by Edvard Munch](https://github.com/Vaimaster/Art-Unveiled-Enhancing-Access-to-Arts-for-the-Visually-Impaired/raw/main/predict/00014.jpg)
<br>"Portrait of Felix Auerbach" by Edvard Munch

### Text
<a href="https://github.com/Vaimaster/Art-Unveiled-Enhancing-Access-to-Arts-for-the-Visually-Impaired/blob/main/predict/00014_desired_response.txt" target="_blank" rel="noopener">A man is wearing a jacket, suit, and tie. He has a moustache, beard, and cigarette in his hand. His collar is turned up and he has a bow tie on. His beard is neatly trimmed. He is standing in front of a wall.</a>

### Audio
Click <a href="https://github.com/Vaimaster/Art-Unveiled-Enhancing-Access-to-Arts-for-the-Visually-Impaired/raw/main/predict/00014_example.mp3" target="_blank" rel="noopener">here</a> to download and play the audio file.
