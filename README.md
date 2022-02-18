<h1> Speaker Recognition through Deep-Neural-Network </h1>

<p>In recent years, speaker identification has been gaining popularity, with important applications in computer security, automation and authentication systems.<br>
Speaker Recognition can be divided into two types of applications: <b>Speaker Verification</b> and <b>Speaker Identification</b>. <br>

<ul>
<li>In Speaker Verification, the person 'introduces' himself by means of an identifier of some kind (user name, smart card, etc.) and the application verifies whether the voice of the person speaking matches that of his voiceprint stored in the system. If the voice of the speaker and the fingerprint are similar, i.e. if the similarity value exceeds a certain threshold, the verification is successful and the person is authenticated.</li>
<li>In a Speaker Identification application, on the other hand, the person speaking 'does not present himself', and the degree of similarity of his voice must be measured against a set of available voiceprints. If all the possible users of the system have already been catalogued ("closed-set"), it is assumed that the voice of the person must, in any case, correspond to one of those available. Otherwise, if there is a possibility that a user has not been previously catalogued ("openset"), the result of the verification may be that the voice does not match any of those known.</li><br> 
</ul>
With the increasing demand for security, two fundamental concepts come to the fore: that of identity and that of non-repudiation. In other words, if the identification technique is sufficiently secure, then in addition to guaranteeing the identity of the person speaking, it will imply that the latter cannot deny having done so.</p><br>

<p>With my thesis project I wanted to explore the recognition of voiceprints because nowadays the technology used to implement these biometric systems is available to everyone. Specifically, I used a neural architecture for the processing of raw audio samples, ECAPA-TDNN, based on the Time Delay Neural Network (TDNN) model. The architecture used significantly outperforms previous models on the VoxCeleb1 and VoxCeleb2 datasets.<p>

<strong>Phase 1</strong>
<p>Each speaker recognition system is characterised by two phases: a data collection phase (enrollment) and a verification phase (verification). During the data collection phase, the voice of the speaker is recorded and from it a certain number of characteristics are extracted through a neural model trained to form a vocal fingerprint. In the verification phase a voice sample is compared with the previously created voiceprint to verify its identity. If the two fingerprints match, it is the same speaker and the verification is successful.</p>

<img src="https://github.com/izzoluca/Speaker-Recognition-through-Deep-Neural-Network/blob/main/Screenshots/sc0.jpg" alt="SpeakerVerification" >
