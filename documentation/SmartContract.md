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
    <li><a href="#3-Sintering-sequence">3. Sintering sequence</a></li>
    <li><a href="#4-Shipment-back-to-Manufacturer-sequence">4. Shipment back to Manufacturer sequence</a></li>
    <li><a href="#5-Quality-control-sequence">5. Quality control sequence</a></li>
    <li><a href="#6-Delivery-to-Customer-sequence">6. Delivery to Customer sequence</a></li>
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



### II3_ReceivedShippingSintererOrder

The sintering service provider receives the parts from the shipper and confirms the handover. The function is executed by the sinterer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedShippingSintererOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedShippingSintererOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedShippingSintererOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedShippingSintererOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 3. Sintering sequence



### III1_SinterOrder

The sinterer debinds and sinter the components. In addition, he documents the activities, saves the documents in the IPFS and stores an updated CID string in the smart contract. The function is executed by the sinterer. The transaction execution, smart contract history, transaction details, transaction logs and Contract query are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/SinterOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/SinterOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/SinterOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/SinterOrder/Transaction_logs.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/SinterOrder/Contract_query.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### III2_RequestReshippingManufacturerOrder

Shipping request to transport the printed parts back to the manufacturer for final quality assurance. The function is executed by the sinterer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestReshippingManufacturerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestReshippingManufacturerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestReshippingManufacturerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestReshippingManufacturerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 4. Shipment back to Manufacturer sequence



### IV1_AcceptReshippingManufacturerOrder

The shipping service provider accepts the new shipping request and takes over the parts. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptReshippingManufacturerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptReshippingManufacturerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptReshippingManufacturerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptReshippingManufacturerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### IV2_CompleteReshippingManufacturerOrder

The shipping service provider complete the reshipping order and deliver the parts to the manufacturer. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteReshippingManufacturerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteReshippingManufacturerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteReshippingManufacturerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CompleteReshippingManufacturerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### IV3_ReceivedReshippingManufacturerOrder

The manufacturer receives the parts from the shipper and confirms the handover. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedReshippingManufacturerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedReshippingManufacturerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedReshippingManufacturerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/ReceivedReshippingManufacturerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 5. Quality control sequence



### V1_CheckOrder

The manufacturer performs the final quality control of the parts. In addition, he documents the activities, saves the new documents in the IPFS and stores an updated CID string in the smart contract. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details, transaction logs and Contract query are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CheckOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CheckOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CheckOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CheckOrder/Transaction_logs.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/CheckOrder/Contract_query.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### V2_RequestDeliveryCustomerOrder

Shipping request to transport the final parts to the customer. The function is executed by the manufacturer. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestDeliveryCustomerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestDeliveryCustomerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestDeliveryCustomerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/RequestDeliveryCustomerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



## 6. Delivery to Customer sequence



### VI1_AcceptDeliveryCustomerOrder

The shipping service provider accepts the shipping request to the customer and takes over the parts. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### VI1_AcceptDeliveryCustomerOrder

The shipping service provider accepts the shipping request to the customer and takes over the parts. The function is executed by the shipper. The transaction execution, smart contract history, transaction details and transaction logs are shown below.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_execution.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/SmartContract_history.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_details.jpg" width="700">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AcceptDeliveryCustomerOrder/Transaction_logs.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>
