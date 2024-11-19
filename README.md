# CDPG Privacy Research
## _A collection of the privacy-related research work undertaken under the purview of the Center of Data for Public Good_

## Motivation

## Funding

## Research Directions
| Project | Link to Github Repository |
| ------ | ------ |
| Secure Multi-Party Computation Extensions | [datakaveri/iudx-MOTION2NX][smpc] |
| Trusted Execution Environment Integrations | |
| Anonymisation Pipeline | [datakaveri/differential-privacy][anonpipe] |
| Carbyne Stack Extensions | [abhi4578/klyshko][cs-klyshko] |
| Blockchain-based Payments | [datakaveri/crypto-payment-gateway-poc][blockchain] |

## Tech

We use a number of open source libraries to work properly:

- [pandas] - 
- [numpy] - 
- [h3] -
.
.
.

## Peer-Reviewed Papers

Below are the works that have been peer-reviewed.
### Conference Papers

* P. Gupta, V. A. Rameshwar, A. Tandon and N. Chakraborty, "Mean Estimation with User-Level Privacy for Spatio-Temporal IoT Datasets," 2024 International Conference on Signal Processing and Communications (SPCOM), Bangalore, India, 2024, pp. 1-5, doi: 10.1109/SPCOM60851.2024.10631607. <br>
```Abstract: This paper considers the problem of the private release of sample means of speed values from traffic datasets. Our key contribution is the development of user-level differentially private algorithms that incorporate carefully chosen parameter values to ensure low estimation errors on real-world datasets, while ensuring privacy. We test our algorithms on ITMS (Intelligent Traffic Management System) data from an Indian city, where the speeds of different buses are drawn in a potentially non-i.i.d. manner from an unknown distribution.```

* R. Burra, A. Tandon and S. Mittal, "Empowering SMPC: Bridging the Gap Between Scalability, Memory Efficiency and Privacy in Neural Network Inference," 2024 16th International Conference on COMmunication Systems & NETworkS (COMSNETS), Bengaluru, India, 2024, pp. 1-6, doi: 10.1109/COMSNETS59351.2024.10427509. <br>
```Abstract: This paper aims to develop an efficient open-source Secure Multi-Party Computation (SMPC) repository, that addresses the issue of practical and scalable implementation of SMPC protocol on machines with moderate computational resources while aiming to reduce the execution time. We implement the ABY2.0 protocol for SMPC, providing developers with effective tools for building applications on the ABY 2.0 protocol. This article addresses the limitations of the C++ based MOTION2NX framework for secure neural network inference, including memory constraints and operation compatibility issues.```

* N. Chakraborty, A. Sharma, J. Dutta. H. D. Kumar, "Privacy-Preserving Data Quality Assessment for Time-Series IoT Sensors," 2024 IEEE International Conference on Internet of Things and Intelligence Systems (IoTaIS) - Applications and Services Track, Bandung, Indonesia, Accepted - Pending Publication. <br>
```Abstract: This paper proposes a novel framework for automated, objective, and privacy-preserving data quality assessment of time-series data from IoT sensors deployed in smart cities. We leverage custom, autonomously computable metrics that parameterise the temporal performance and adherence to a declarative schema document to achieve objectivity. Additionally, we utilise a trusted execution environment to create a "data-blind" model that ensures individual privacy, eliminates assessee bias, and enhances adaptability across data types. This paper describes this data quality assessment methodology for IoT sensors, emphasising its relevance within the smart-city context while addressing the growing need for privacy in the face of extensive data collection practices.```

* V. Walunj, V. Rajaraman, J. Dutta, A. Sharma, “Integrating Crypto-Based Payment Systems for Data Marketplaces: Enhancing Efficiency, Security, and User Autonomy”, 20th International Conference on Information Systems Security (ICISS), LNMIIT, Jaipur, India, 2024. Accepted - Pending Publication. <br>
```Abstract: Data exchanges as Digital Public Infrastructures drive data-driven economies by enhancing efficiency, enabling revenue streams, and facilitating data monetization. This work explores integrating crypto-based payments into platforms like IUDX and ADeX, offering benefits such as enhanced security, lower fees, and decentralized control. Key focus areas include crypto gateways, smart contracts, and wallet integration. The study highlights challenges like regulation and scalability while proposing a secure, efficient ecosystem to advance the data economy.```

### Workshop Posters

* V. A. Rameshwar, A. Tandon, and A. Sharma, "User-Level Differentially Private Mean Estimation for Real-World Datasets," in the ISIT 2024 Workshop on Information-Theoretic Methods for Trustworthy Machine Learning (IT-TML). <br>```Short precis: In this work, we provide rigorous theoretical justifications for the performance trends of well-known clipping-based algorithms on real-world ITMS and i.i.d. synthetic datasets. An important contribution of this work is the formalization and explicit computation of the "worst-case estimation error" incurred by a canonical user-level differentially private algorithm for mean estimation, which clips the number of contributions of users in an attempt to increase the accuracy of reconstruction.```

## License

&copy; 2024 Center for Data For Public Good
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [SMPC]: https://github.com/datakaveri/iudx-MOTION2NX
   [cs-klyshko]: https://github.com/abhi4578/klyshko
   [AnonPipe]: https://github.com/datakaveri/differential-privacy>
   [blockchain]: https://github.com/datakaveri/crypto-payment-gateway-poc
