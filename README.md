<h1> Speaker Recognition through Deep-Neural-Network </h1>

<p>In recent years, speaker identification has been gaining popularity, with important applications in computer security, automation and authentication systems.<br>
Speaker Recognition can be divided into two types of applications: Speaker Verification and Speaker Identification. <br>

<ul>
<li>In Speaker Verification, the person 'introduces' himself by means of an identifier of some kind (user name, smart card, etc.) and the application verifies whether the voice of the person speaking matches that of his voiceprint stored in the system. If the voice of the speaker and the fingerprint are similar, i.e. if the similarity value exceeds a certain threshold, the verification is successful and the person is authenticated.</li>
  
<li>In a Speaker Identification application, on the other hand, the person speaking 'does not present himself', and the degree of similarity of his voice must be measured against a set of available voiceprints. If all the possible users of the system have already been catalogued ("closed-set"), it is assumed that the voice of the person must, in any case, correspond to one of those available. Otherwise, if there is a possibility that a user has not been previously catalogued ("openset"), the result of the verification may be that the voice does not match any of those known.</li><br> 
</ul>
  
With the increasing demand for security, two fundamental concepts come to the fore: that of identity and that of non-repudiation. In other words, if the identification technique is sufficiently secure, then in addition to guaranteeing the identity of the person speaking, it will imply that the latter cannot deny having done so. With my thesis project I wanted to explore and deepen the recognition of voiceprints because now the technology used to implement these biometric systems is available to everyone. Specifically, I used a neural architecture for the processing of raw audio samples, ECAPA-TDNN, based on the Time Delay Neural Network (TDNN) model. The architecture used significantly outperforms previous models on the VoxCeleb1 and VoxCeleb2 datasets.</p>
