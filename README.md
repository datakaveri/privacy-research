# CDPG Privacy Research
## _A collection of the privacy-related research work undertaken under the purview of the Center of Data for Public Good_

## Research Directions
| Project | Link to Github Repository |
| ------ | ------ |
| Secure Multi-Party Computation Extensions| [datakaveri/iudx-MOTION2NX][smpc] |
| Confidential Computing | |
| Anonymisation Pipeline | [datakaveri/differential-privacy][anonpipe] |
| Carbyne Stack Extensions |  |
| Blockchain-based Payments | [datakaveri/crypto-payment-gateway-poc][blockchain] |

### Secure Multi-Party Computation Extensions
Secure Multiparty Computation (SMPC) is a cryptographic technique that enables multiple parties to jointly compute a function over their private inputs while keeping those inputs confidential. It ensures that no party learns anything about others' inputs beyond what can be inferred from the output. SMPC is widely used in privacy-preserving applications, such as secure data analysis, voting systems, and federated learning. It relies on cryptographic primitives like secret sharing, homomorphic encryption, and oblivious transfer. 

We applied SMPC to an image inference task involving a machine learning model, ensuring that both the image provider and model provider keep their inputs private. This application was implemented using ABY2.0 on the MOTION2NX framework. To enhance performance, we designed algorithms to reduce execution time and memory consumption. Additionally, we created Docker images with all necessary dependencies and binaries to streamline the deployment of the end-to-end application on cloud machines.

### Confidential Computing
In the changing world of data processing shifting to the cloud, a key question arises: How do we make sure our shared data stays secure and confidential in third-party managed cloud environments? How can different parties having sensitive data collaborate to create value without compromising?
Confidential Computing is the solution to these challenges. 

A Trusted Execution Environment [TEE] - also known as a secure enclave - is a hardware-based, isolated and encrypted section within a computer's processor where sensitive data and processes can be executed. A TEE guarantees data confidentiality, data integrity and code integrity.
We integrate our privacy-enhancing applications and workflows with PII data with TEEs to enforce the paradigm of secure computation. We have incorporated three state-of-the-art TEE workflows:
* AMD SEV-SNP
* Intel SGX
* AWS Nitro 

These integrations require some custom modules to ensure smooth handling of data, operations, and users:
* Enclave Manager - Responsible for scheduling tasks and communicating between the enclave and the client. 
* Access Policy Domain - Handles the attestation procedure to verify the enclave hardware through an external client. 
* Resource Server - Facilitates the process of fetching data from various data providers.

Through our work, we hope to answer the following questions:
How can we make sure our shared data stays secure and confidential in third-party managed cloud environments?
How can different parties having sensitive data collaborate to create value without compromising privacy?

### Carbyne Stack Extensions
Multi-Party Computation (MPC) paradigms provide privacy-preserving computation via two phases: an input-independent offline phase, which uses heavyweight cryptographic tools to generate cryptographic randomness in advance, and a second online phase consisting of lightweight operations that consume this randomness. We integrate TEEs with MPC to securely accelerate the MPC offline phase in collaboration with the Carbyne Stack team at Bosch Research. 

### Blockchain Payment Integrations
Data exchanges are transforming global economies by enabling seamless data sharing, trade, and monetization. Exchanges under the CDPG umbrella such as India Urban Data Exchange (IUDX) and Agricultural Data Exchange (ADeX) create ecosystems where data providers and consumers collaborate, innovate, and unlock the potential of data.
However, traditional payment systems supporting these exchanges face challenges such as high costs, slow processing, and security vulnerabilities. To solve for this, we integrate crypto-based payment systems with our exchange platforms. They offer enhanced security, faster transactions, lower fees, and decentralized fund control. We utilise blockchain-enabled technologies like cryptocurrency payment gateways, smart contracts, and digital wallets to streamline data transactions, ensuring secure and efficient data discovery, purchase, and exchange.
Through this integration, we hope to provide these platforms with a scalable, secure, and user-friendly ecosystem that drives growth, innovation, and equitable access in the data economy.

### De-Identification Pipeline
The De-Identification Pipeline started off as an exploration of the first principles of differential privacy and its applications to large datasets generated by smart cities, particularly those containing Personally Identifiable Information [PII]. This eventually blossomed into a full-fledged data de-identification pipeline that can perform ingestion handling, sanitization, classical data anonymization techniques such as suppression, pseudonymization, generalization, and aggregation as well as techniques that offer a formal guarantee of privacy such as k-anonymization and differential privacy.
We offer this application in conjunction with a Trusted Execution Environment to ensure that anyone using the application are also offered the trinity of benefits provided by a TEE - data integrity, code integrity and data confidentiality.

To make this codebase open-source and allow people to use the modules of the pipeline on their own datasets, we also offer the code as a python package that can be installed using pip - found here[link].

## Peer-Reviewed Papers

Below are the works that have been peer-reviewed.
### Conference Papers

* P. Gupta, V. A. Rameshwar, A. Tandon and N. Chakraborty, "Mean Estimation with User-Level Privacy for Spatio-Temporal IoT Datasets," 2024 International Conference on Signal Processing and Communications (SPCOM), Bangalore, India, 2024, pp. 1-5, doi: 10.1109/SPCOM60851.2024.10631607.
```Abstract: This paper considers the problem of the private release of sample means of speed values from traffic datasets. Our key contribution is the development of user-level differentially private algorithms that incorporate carefully chosen parameter values to ensure low estimation errors on real-world datasets, while ensuring privacy. We test our algorithms on ITMS (Intelligent Traffic Management System) data from an Indian city, where the speeds of different buses are drawn in a potentially non-i.i.d. manner from an unknown distribution.```
[Read The Paper][gupta_et_al]

* R. Burra, A. Tandon and S. Mittal, "Empowering SMPC: Bridging the Gap Between Scalability, Memory Efficiency and Privacy in Neural Network Inference," 2024 16th International Conference on COMmunication Systems & NETworkS (COMSNETS), Bengaluru, India, 2024, pp. 1-6, doi: 10.1109/COMSNETS59351.2024.10427509.
```Abstract: This paper aims to develop an efficient open-source Secure Multi-Party Computation (SMPC) repository, that addresses the issue of practical and scalable implementation of SMPC protocol on machines with moderate computational resources while aiming to reduce the execution time. We implement the ABY2.0 protocol for SMPC, providing developers with effective tools for building applications on the ABY 2.0 protocol. This article addresses the limitations of the C++ based MOTION2NX framework for secure neural network inference, including memory constraints and operation compatibility issues.```
[Read The Paper][burra_et_al]

* N. Chakraborty, A. Sharma, J. Dutta. H. D. Kumar, "Privacy-Preserving Data Quality Assessment for Time-Series IoT Sensors," 2024 IEEE International Conference on Internet of Things and Intelligence Systems (IoTaIS) - Applications and Services Track, Bandung, Indonesia, Accepted - Pending Publication.
```Abstract: This paper proposes a novel framework for automated, objective, and privacy-preserving data quality assessment of time-series data from IoT sensors deployed in smart cities. We leverage custom, autonomously computable metrics that parameterise the temporal performance and adherence to a declarative schema document to achieve objectivity. Additionally, we utilise a trusted execution environment to create a "data-blind" model that ensures individual privacy, eliminates assessee bias, and enhances adaptability across data types. This paper describes this data quality assessment methodology for IoT sensors, emphasising its relevance within the smart-city context while addressing the growing need for privacy in the face of extensive data collection practices.```
[Read The Paper][chakraborty_et_al_iotais]

* V. Walunj, V. Rajaraman, J. Dutta, A. Sharma, “Integrating Crypto-Based Payment Systems for Data Marketplaces: Enhancing Efficiency, Security, and User Autonomy”, 20th International Conference on Information Systems Security (ICISS), Jaipur, India, 2024. Accepted - Pending Publication.
```Abstract: Data exchanges as Digital Public Infrastructures drive data-driven economies by enhancing efficiency, enabling revenue streams, and facilitating data monetization. This work explores integrating crypto-based payments into platforms like IUDX and ADeX, offering benefits such as enhanced security, lower fees, and decentralized control. Key focus areas include crypto gateways, smart contracts, and wallet integration. The study highlights challenges like regulation and scalability while proposing a secure, efficient ecosystem to advance the data economy.```
[Read The Paper][walunj_et_al]

* H. Kallamadi, R. Burra, S. Mittal, S. Sharma, A. Venkatesh, A. Tandon, "Enhancing MOTION2NX for Efficient, Scalable and Secure Image Inference using Convolutional Neural Networks", 4th International Conference on Network Security and Blockchain Technology (ICNSBT), Haldia, India, 2025. Accepted - Pending Publication.
```Abstract: This work contributes towards the development of an efficient and scalable open-source Secure Multi-Party Computation (SMPC) protocol on machines with moderate computational resources. We use the ABY2.0 SMPC protocol implemented on the C++ based MOTION2NX framework for secure convolutional neural network (CNN) inference application with semi-honest security. Our list of contributions are as follows. Firstly, we enhance MOTION2NX by providing a tensorized version of several primitive functions including the Hadamard product, indicator function and argmax function. Secondly, we adapt an existing Helper node algorithm, working in tandem with the ABY2.0 protocol, for efficient convolution computation to reduce execution time and RAM usage. Thirdly, we also present a novel splitting algorithm that divides the computations at each CNN layer into multiple configurable chunks. This novel splitting algorithm, providing significant reduction in RAM usage, is of independent interest and is applicable to general SMPC protocols.```
[Read The Paper][kallamadi_et_al]

* V. A. Rameshwar, A. Tandon, and A. Sharma, "Optimal Tree-Based Mechanisms for Differentially Private Approximate CDFs", 17th International Conference on COMmunication Systems & NETworkS (COMSNETS) - Cyber Security and Privacy Workshop, Bengaluru, India, 2025. Accepted - Pending Publication.
```Abstract: This paper considers the epsilon-differentially private (DP) release of an approximate cumulative distribution function (CDF) of the samples in a dataset. We assume that the true (approximate) CDF is obtained after lumping the data samples into a fixed number K of bins. In this work, we extend the well-known binary tree mechanism to the class of level-uniform tree-based mechanisms and identify epsilon-DP mechanisms that have a small l2-error. We identify optimal or close-to-optimal tree structures when either of the parameters, which are the branching factors or the privacy budgets at each tree level, are given, and when the algorithm designer is free to choose both sets of parameters. Interestingly, when we allow the branching factors to take on real values, under certain mild restrictions, the optimal level-uniform tree-based mechanism is obtained by choosing equal branching factors independent of K, and equal privacy budgets at all levels.```
[Read The Paper][rameshwar_et_al_comsnets]

* N. Chakraborty, A. Tandon, K. Reddy, K. Kirpekar, B. Robert, H. Kumar, A. Venkatesh, A. Sharma, "Building a Privacy Web with SPIDEr - Secure Pipeline for Information De-Identification with End-to-End Encryption", 17th International Conference on COMmunication Systems & NETworkS (COMSNETS) - Demos and Exhibits, Bengaluru, India, 2025. Accepted - Pending Publication.
``` Abstract: Data de-identification makes it possible to glean insights from data while preserving user privacy. The use of Trusted Execution Environments (TEEs) allow for the execution of de-identification applications on the cloud without the need for a user to trust the third-party application provider. In this paper, we present SPIDEr - Secure Pipeline for Information De-Identification with End-to-End Encryption, our implementation of an end-to-end encrypted data de-identification pipeline. SPIDEr supports classical anonymisation techniques such as suppression, pseudonymisation, generalisation, and aggregation, as well as techniques that offer a formal privacy guarantee such as k-anonymisation and differential privacy. To enable scalability and improve performance on constrained TEE hardware, we enable batch processing of data for differential privacy computations. We present our design of the control flows for end-to-end secure execution of de-identification operations within a TEE. As part of the control flow for running SPIDEr within the TEE, we perform attestation - a process that verifies that the software binaries were properly instantiated on a known, trusted platform.```
[Read The Paper][chakraborty_et_al_comsnets]

### Workshop Posters

* V. A. Rameshwar, A. Tandon, and A. Sharma, "User-Level Differentially Private Mean Estimation for Real-World Datasets," 2024 IEEE International Symposium on Information Theory (ISIT) - Workshop on Information-Theoretic Methods for Trustworthy Machine Learning (IT-TML). ```Short precis: In this work, we provide rigorous theoretical justifications for the performance trends of well-known clipping-based algorithms on real-world ITMS and i.i.d. synthetic datasets. An important contribution of this work is the formalization and explicit computation of the "worst-case estimation error" incurred by a canonical user-level differentially private algorithm for mean estimation, which clips the number of contributions of users in an attempt to increase the accuracy of reconstruction.```
[Read The Paper][rameshwar_et_al_isit_ititml]

## License

&copy; 2024 Center for Data For Public Good
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [SMPC]: https://github.com/datakaveri/iudx-MOTION2NX
   [AnonPipe]: <https://github.com/datakaveri/differential-privacy>
   [blockchain]: <https://github.com/datakaveri/crypto-payment-gateway-poc>
   
   
   [burra_et_al]:https://github.com/datakaveri/privacy-research/blob/298c970a61455829a3bf0b5e4ff5f3759aa25e4e/files/COMSNET24_burra_et_al.pdf
   [chakraborty_et_al_iotais]:https://github.com/datakaveri/privacy-research/blob/298c970a61455829a3bf0b5e4ff5f3759aa25e4e/files/IOTAIS24_chakraborty_et_al.pdf
   [walunj_et_al]:https://github.com/datakaveri/privacy-research/blob/298c970a61455829a3bf0b5e4ff5f3759aa25e4e/files/ICISS24_walunj_et_al.pdf
   [gupta_et_al]:https://github.com/datakaveri/privacy-research/blob/298c970a61455829a3bf0b5e4ff5f3759aa25e4e/files/SPCOM24_gupta_et_al.pdf
   [rameshwar_et_al_isit_ititml]:https://github.com/datakaveri/privacy-research/blob/298c970a61455829a3bf0b5e4ff5f3759aa25e4e/files/ISIT24-ITML_rameshwar_et_al.pdf
   [kallamadi_et_al]:https://github.com/datakaveri/privacy-research/blob/4f4fc5601b7f6cd74fc84d691d32e2a13c7d01da/files/ICNSBT25_kallamadi_et_al.pdf
   [rameshwar_et_al_comsnets]:https://github.com/datakaveri/privacy-research/blob/4f4fc5601b7f6cd74fc84d691d32e2a13c7d01da/files/COMSNETS25_CSP_rameshwar_et_al.pdf
   [chakraborty_et_al_comsnets]:https://github.com/datakaveri/privacy-research/blob/4f4fc5601b7f6cd74fc84d691d32e2a13c7d01da/files/COMSNETS25_D%26E_chakraborty_et_al.pdf
   
