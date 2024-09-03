# Surveillance-Detection

This entire project can be divided into four categories of implementation – collecting data using Haarcascade, training the model to generate a yml file for the faces in the database, using the training data in 
the yml file to detect and recognize faces from the live video, and sending an alert one of the faces from the database is spotted. 

* **Collecting Data:**  The database for this project is just the images of the missing victims. In reality, just submitting how many ever photos of the victim to the police would suffice to get this algorithm working, but we have implemented a small snippet of code that collects 150 images per person within the span on 10 seconds from the web camera. 
* **Training Model:** The LBPH algorithm is used to generate histograms corresponding to every image in the database. As mentioned earlier, every folder in the database has a label in the form of a whole number 
which acts as an index for mapping the victims to their images using a dictionary. In this project we have populated images for two people, so the dictionary would look something like this {0: “Ananya”, 1: "Sri"}. 
* **Testing model on live video:** Once the model is trained, the algorithm will be able to detect faces in live. For the sake of simulating CCTV cameras, we are using the web cam of our computer devices to 
capture the live video. 
* **Sending out alerts:** In the real-world, when a person is detected on one of the CCTV cameras, an alert could be send to the police, or a responsible control room. Like amber alerts, there could be/maybe an alert already in system that could be used to alert the officials to rescue the victim immediately. 
Since this is a simulation of the real world, we have enabled an alert system using email. An email with the geolocation of where the person was spotted will be sent to the registered recipient. Along with the email, there is also a beep buzzer sound that is enabled in the system, to attract attention.
