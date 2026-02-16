rename code word as word from modulatiom constellation

gradient descent should give better convergence (more info about the loss landscape)
use tensor flow to autodiff

Blind Source Separation of Inverse Square Law Signals with no Prior

abstract
This work develops a blind source separation algorithm for unmixing signals received from sources at different locations arriving at a sensor array. The approach is based on the geometry of the propagtion of signals that decay with inverse square of the distance from each transmitter. A difference in our approach is that we don't make any prior assumptions about the signal statistics. This will allow the method to be used for a very general class of signals. The geometric approaches takes a previously underdetermined problem and finds an overdetermined approach which obtains accurate signal separation and transmitter location estimation, which can be seen as a new take on the classic matrix factorization problem in communications. This approach works for waves where the speed of propagation is large relative to the sensor array dimension. This means for smaller arrays, this approach will apply to multisource audio separation, and will also for electromagnetic signal separation with possibly larger arrays. We also see potential applications in medical sensing, for example ultrasound. For more distant EM signals, we perform an analysis of the operating limits of the method for different receiver arrays configurations. For example, given a SNR of 80dB, we can use an array to separate sources with no prior knowledge and obtain an root mean squared error of 0.00551 for a signal with power (mean squared amplitude) of 1 unit. 

this is also known as the cocktail party problem

no positive requirment, mixing amplitudes is more accurate than mixing powers

add literature review about methods using microphone locations

larger number of receivers, as this is like more samples in a neural network problem

SNR at receiver makes sense, since more distant transmitters would use a larger power we don't measure SNR at transmitter

modulation based approaches
Blind Signal Separation Techniques on Different 
types of MIMO Systems – An Overview


if wave is slow, the signals can arrive at different times, the receivers just need to be close relative to the wave speed so they can measure the different losses at the same time
(so it can also work for audio)

if number of sources is unknown, iterate from N=1,2,3 until there is a minimum in loss

literature review
ica and other source separation methods (my method has no prior)
matrix factorization (see thesis)

because multipath noise may vary slowly over time, this noise will not be handled by large number of time samples and presents the hardest problem for our method
(this can also be overcome by increasing the receiver array size, since multipath makes loss at each receiver off, but the larger the distances between receivers, the smaller the multipath loss is relative to the difference in loss), also I think higher frequencies have less multipath error

experiment design

vary distance of transmitters relaive to size of receiver array

vary SNR
(since the ambient noise at the receiver is constant relative to different incoming signals, that means when we report SNR of 20dB, if this is measured for the mosg distance source, the closer signals will have better SNF, meaning in practice we can expect better result than our simplified model of constant SNR)

normalize receiver positions
(make them small so solution has transmitter locations between 0 and 1)

normalize received power
(already done, since target transmit power is 1)

(both normalizations are for optimization tool to search from 0 to 1)
