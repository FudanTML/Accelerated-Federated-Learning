# Accelerated-Federated-Learning
## Problem Statement
Federated learning (FL) is a machine learning setting where many clients (e.g. mobile devices or whole organizations) collaboratively train a model under the orchestration of a central server (e.g. service provider), while keeping the training data decentralized [1]. In a FL model, clients (e.g., Android phones) use their local data to train a local ML model, then send the parameter updates of local models (e.g., Android phone updates) rather than raw data to the central server (e.g., Android cloud). The server produces a shared global ML model by aggregating the local updates [2]. Despite the ability to jointly train the model without directly
sharing the data, which mitigats the data isolation and protects the data privacy, FL still faces several major challenges.

## Project Goals
 * __Unfavorable Convergence :__ The communication cost between clients and the server in federated learning is expensive, so traditional optimization methods, such as SGD, are often unsuitable. Therefore, FedAvg allows clients to perform multiple epochs of SGD on their local data, and then feedback the optimization results to the server. Despite FedAvg has seen great success, there are still some issues in its convengence : 1) _non-iid data_ : data between clients is not independent and identically distributed (non-iid), which leads to client models moving away from the globally optimal model.    2)_a lack of adaptivity_: Standard SGD optimization methods used in most FL models may be unsuitable for federated settings. Therefore, in this project, we hope that you can make some improvements in the convergence and adaptation of FL to help FL converge better and faster. 

`code:`You may follow the following as an example  
  * [Communication-Efficient Adaptive Federated Learning](https://github.com/yujiaw98/FedCAMS)
  
 `note:`Although the code contains both non-IID and IID cases, we encourage you to explore in the non-IID case, which is not only more challenging, but you can discover more interesting phenomena.
 
## Reference
[1] Kairouz P, McMahan H B, Avent B, et al. Advances and open problems in federated learning[J]. Foundations and Trends® in Machine Learning, 2021, 14(1–2): 1-210.  
[2] Jin J, Ren J, Zhou Y, et al. Accelerated Federated Learning with Decoupled Adaptive Optimization[C]//International Conference on Machine Learning. PMLR, 2022: 10298-10322.   
