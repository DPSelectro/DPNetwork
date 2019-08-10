# DPNetwork

This repositorys stores code for the DPNetwork project. DPNetwork detects malicous network flows using Joy and the UNSW-NB15(https://www.unsw.adfa.edu.au/unsw-canberra-cyber/cybersecurity/ADFA-NB15-Datasets) and USTC-TFC2016(https://ieeexplore.ieee.org/document/7899588) datasets. By anlyzing bidirectional network flow statistics, DPNetwork enables  The DPNetwork incorporates differential privacy through an prepended autoencoder. By then making use of the bounded output stablility property of differential privacy, this project enables robust detection of malicious flows and protects agains carefully designed adversarial example attacks. 

Use joy in order to process pcap and retreive bidirectional flows and then use preprocessing files in order
to retreive files in correct machine learning format
```
bin/joy bidir=1 ppi=1 http=1 tls=1 dns=1 output=cridex.json cridex.pcap
```


Run autoencoder file with a specified SCALE and SCALE-STRING to get an autoencoder to prepend against model that is the used to learn malicious from benign flows.

# UNSW Dataset

## Confustion Matrix for UNSW
<img src="https://github.com/hanshanley/DPNetwork/blob/master/Figures/Confusion-MatrixUNSW2-AutoEncoderGaussianImmed0point7WITHOUT-AUTOENCODER-1.png" width="480">

## TSNE plot of UNSW for malware categories
<img src= "https://github.com/hanshanley/DPNetwork/blob/master/Figures/UNSW-HTTP-all-TSNE3D-1.png" width="480">


## Example Adversarial Example for the UNSW dataset
<img src= "https://github.com/hanshanley/DPNetwork/blob/master/Figures/UNSW-adv-examplegaussian-0point3-1.png" width="480">

