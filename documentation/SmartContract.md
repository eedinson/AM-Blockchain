<!-- Documentation -->
## Smart contract execution documentation

All functions programmed in the smart contract were subsequently tested to ensure that they can only be executed by the intended party and that they record data and events correctly. 

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Deploy-contract">Deploy contract</a></li>
    <li><a href="#1-Manufacturing-sequence">1. Manufacturing sequence</a></li>
    <li><a href="#2-Shipment-to-Sinterer-sequence">2. Shipment to Sinterer sequence</a></li>
    <li><a href="#II1_AcceptShippingSintererOrder">II1_AcceptShippingSintererOrder</a></li>
    <li><a href="#II2_CompleteShippingSintererOrder">II2_CompleteShippingSintererOrder</a></li>
  </ol>
</details>



## Deploy contract

Creation of the smart contract. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/DeployContract/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/DeployContract/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/DeployContract/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/DeployContract/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 1. Manufacturing sequence



### I1_CreateOrder

Creation of a new order or a new part record documentation on the blockchain. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details, transaction logs and Contract query are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CreateOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CreateOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CreateOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CreateOrder/Transaction_logs.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CreateOrder/Contract_query.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### I2_RequestShippingSintererOrder

Shipping request to transport the printed parts to the sintering service provider. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestShippingSintererOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestShippingSintererOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestShippingSintererOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestShippingSintererOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 2. Shipment to Sinterer sequence



### II1_AcceptShippingSintererOrder

The shipping service provider accepts the shipping request and takes over the parts. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptShippingSintererOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptShippingSintererOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptShippingSintererOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptShippingSintererOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### II2_CompleteShippingSintererOrder

The shipping service provider complete the shipping order and deliver the parts to the sinterer. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteShippingSintererOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteShippingSintererOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteShippingSintererOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteShippingSintererOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>
