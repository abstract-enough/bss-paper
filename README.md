literature review
ica and other source separation methods (my method has no prior)
matrix factorization (see thesis)

because multipath noise may vary slowly over time, this noise will not be handled by large number of time samples and presents the hardest problem for our method
(this can also be overcome by increasing the receiver array size)

experiment design

vary distance of transmitters relaive to size of receiver array

vary SNR
(since the ambient noise at the receiver is constant relative to different incoming signals, that means when we report SNR of 20dB, if this is measured for the mosg distance source, the closer signals will have better SNF, meaning in practice we can expect better result than our simplified model of constant SNR)

normalize receiver positions
(make them small so solution has transmitter locations between 0 and 1)

normalize received power
(already done, since target transmit power is 1)

(both normalizations are for optimization tool to search from 0 to 1)
