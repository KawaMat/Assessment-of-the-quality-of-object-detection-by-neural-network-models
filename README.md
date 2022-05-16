# Assessment-of-the-quality-of-object-detection-by-neural-network-models
Assessment of the quality of object detection by neural network models, learned with data from a virtual environment.


The object of this thesis is to evaluate the quality of artificial neural network models trained on data coming from reality simulations, such as computer games or modeling programs. The first chapters of the thesis introduce the problem addressed and develop a justification of the value of its solution. One can learn from them that virtual reality can provide a readily available and inexpensive source of data needed to train models tasked with object classification and detection. The following section looks at similar problems solved by research teams around the world and describes their goals, motives, and results. Subsequent chapters lecture the theoretical knowledge necessary for reliable experimentation. First, machine learning, in its broad sense, is discussed, to then focus on neural networks, with special emphasis on convolutional networks. Different network architectures that could potentially be used in the experiment are presented, the ResNet and YOLO (in two versions) networks are mentioned. Since universal measures are required for constructive evaluation, they are described in several variations. The next section deals with the description of the experiment. It contains information about the origin of the learning data. The objects chosen to be the subject of recognition by the model in the image are traffic signs. Then the technologies used in the training process are described, along with its parameters.
The evaluation of the results of the work was carried out by comparing the model learned on images taken from a virtual environment, such as a computer game, with the model learned on real images. A comparison of the detection quality of the same set of test images by both models was then made. The results of this comparison and general conclusions are presented in the last section of the thesis.


The aim is defining to what extent it is possible to use reality simulation with fabricating teaching images corresponding to objects or phenomena from the real world. This method of acquiring images excludes the need to create collections teaching based on photographed objects in the field or in the studio, it is enough to work with computers.




Road signs chosen for the experiment. From the left: Precedence (A-7), Road with priority (D-1), Overtaking ban (B-25):

![image](https://user-images.githubusercontent.com/83005003/168590895-590e3980-77a6-4d74-b317-13fb317ee5b4.png)


Two CNN models were created based on screenshots of the Eurotruck Simulator 2 game and actual images retrieved from Google Maps.


The Eurotruck Simulator 2 game provides the variation of time of day and weather conditions with a high level of detail reproduction:

![image](https://user-images.githubusercontent.com/83005003/168591323-442e1e6e-0344-4d12-9703-1db2e9bc3eea.png)


Test images taken in autumn increase the difficulty of recognizing characters by changing the background context:

![image](https://user-images.githubusercontent.com/83005003/168591492-ae15ccfa-355d-421c-8a06-a656aefe8080.png)

Photograph with model prediction plotted as dark blue envelope and reference frame in green:

![image](https://user-images.githubusercontent.com/83005003/168591642-8165557b-5a7b-41b7-ab3c-9445282b2498.png)

Dependence of model precision and recall on confidence threshold - training data: virtual, sign: No overtaking:

![image](https://user-images.githubusercontent.com/83005003/168591972-c5fc851d-b343-4c36-80c4-dd5f78820c90.png)

Comparison of change in parameters describing prediction quality as a function of threshold level, model learned on virtual data:

![image](https://user-images.githubusercontent.com/83005003/168592099-abd3b43a-0209-4c15-af56-8122b374c91f.png)

Average precision value for each character selected for the experiment:

![image](https://user-images.githubusercontent.com/83005003/168592346-2dbf9879-c3a4-4c5e-9602-38f161853bfd.png)

Average recall value for each character selected for the experiment:

![image](https://user-images.githubusercontent.com/83005003/168592452-d777cbea-53d3-4b3c-a1c9-1050cf3f7a76.png)

Average confidence value for each character selected for the experiment:

![image](https://user-images.githubusercontent.com/83005003/168592651-3c96306d-effe-48a6-a5b2-35e9c7d3b3fe.png)

Average IoU value for each character selected for the experiment:

![image](https://user-images.githubusercontent.com/83005003/168592718-5d50f248-0b9f-49d0-bf38-5cac56d49529.png)


Treatments that could improve the reliability of the experiment include collecting a more numerous database than the one used in the described project. Comparing the models on a larger number of road signs could also affect the final result. If the model would not be used in dynamic inference, it would be worth considering another architecture, such as ResNet, whose average precision in detection tasks is higher, but the model runs slowly. Since traffic signs are easy objects to recognize, due to the characteristics of the task they perform, possible further research in this direction could include recognition of harder-to-see objects or, for example, dangerous street incidents.

