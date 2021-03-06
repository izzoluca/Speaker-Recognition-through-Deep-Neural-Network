<h1> Speaker Recognition through Deep-Neural-Network </h1>

<p>In recent years, speaker identification has been gaining popularity, with important applications in computer security, automation and authentication systems.<br>
Speaker Recognition can be divided into two types of applications: <b>Speaker Verification</b> and <b>Speaker Identification</b>. <br>

<ul>
<li>In Speaker Verification, the person 'introduces' himself by means of an identifier of some kind (user name, smart card, etc.) and the application verifies whether the voice of the person speaking matches that of his voiceprint stored in the system. If the voice of the speaker and the fingerprint are similar, i.e. if the similarity value exceeds a certain threshold, the verification is successful and the person is authenticated.</li>
<li>In a Speaker Identification application, on the other hand, the person speaking 'does not present himself', and the degree of similarity of his voice must be measured against a set of available voiceprints. If all the possible users of the system have already been catalogued ("closed-set"), it is assumed that the voice of the person must, in any case, correspond to one of those available. Otherwise, if there is a possibility that a user has not been previously catalogued ("openset"), the result of the verification may be that the voice does not match any of those known.</li><br> 
</ul>
With the increasing demand for security, two fundamental concepts come to the fore: that of identity and that of non-repudiation. In other words, if the identification technique is sufficiently secure, then in addition to guaranteeing the identity of the person speaking, it will imply that the latter cannot deny having done so.</p><br>

<p>With my thesis project I wanted to explore the recognition of voiceprints because nowadays the technology used to implement these biometric systems is available to everyone. Specifically, I used a neural architecture for the processing of raw audio samples, ECAPA-TDNN, based on the Time Delay Neural Network (TDNN) model. The architecture used significantly outperforms previous models on the VoxCeleb1 and VoxCeleb2 datasets.<p>

<h3>Phase 1</h3>
<p>Each speaker recognition system is characterised by two phases: a data collection phase (enrollment) and a verification phase (verification). During the data collection phase, the voice of the speaker is recorded and from it a certain number of characteristics are extracted through a neural model trained to form a vocal fingerprint. In the verification phase a voice sample is compared with the previously created voiceprint to verify its identity. If the two fingerprints match, it is the same speaker and the verification is successful.</p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc0.jpg" alt="SpeakerVerification" >

<p>The Enrollment phase is the first phase of a biometric process and consists of the acquisition of the biometric characteristics of the individual. On the sample obtained, the quality of the signal is generally checked and then follows a procedure known as "feature extraction". From the audio tracks in "wav" format, a CSV file is produced that will be useful for the training phase. These files tell the model where to find the audio data and how to identify it. The process of creating the files is made possible by the package implemented in the PyTorch library "torchaudio", which is commonly used for I/O operations and audio transformations, using functions that analyse the audio signal and extract the necessary information to fill the file. 
Once this process is complete, a data augmentation process is performed, which literally means 'data augmentation'. It is a set of techniques that expand the available dataset without actually collecting new elements, used to solve the common problem of overfitting.</p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc1.jpg" alt="SpeakerVerification" >

<h3>Phase 2</h3>
<p>The previously elaborated data set is divided, in a pseudo-random way, in two subsets: one destined to the training phase of the neural model (training set) and the other to the validation phase (test set), and they include respectively 90% and 10% of the data of the whole dataset. The training set is used to train the classifier to recognise the subjects, while the test set is used to verify the correctness of the classification.</p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc2.jpg" alt="Training" >

<h3>Phase 3</h3>
<p>For the recognition of the speaker, as previously mentioned, the library <a href="https://speechbrain.github.io/"> "SpeechBrain" </a> was used, which allowed the use of the neural model trained previously to extract the characteristics of the audio tracks and compare them giving in output a score and a prediction. The score is calculated using the cosine distance function (i.e. a heuristic technique for measuring the similarity between the two vectors, carried out by calculating the cosine between them, The similarity value thus defined is between -1 and +1, +1 if the two vectors are perfectly equal, -1 otherwise), while the prediction is a Boolean value, which will be "TRUE" when the system recognises the two voiceprints as coming from the same speaker, while it will be "FALSE" in the opposite case. </p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc3.jpg" alt="Verification" >

<h3>Phase 4 </h3>
<p>Testing phase: For information on the experiments, see this <a href="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/SpeakerRecognitionDNN%20-%20LucaIzzo.pptx"> document </a>. </p>

<h3>Results</h3>
<p>The accuracy achieved by the ECAPA-TDNN model after training with the VoxCeleb1 and VoxCeleb2 datasets was 98-99% for both datasets. This figure increased by about 2% compared to older systems based on different models but trained on the same dataset. While the Equal Error Rate (EER) stored by the system is 0.69%. In fact: a biometric system is better the lower the value of its EER.<br>
<b> Even 2.6% lower than the models considered to be state-of-the-art (x-Vector and ResNet).</b></p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc4.jpg" alt="Verification" >


<h1> Update in Progress </h1>
<p>Setup,configurations and tests will be uploaded soon.</p>
