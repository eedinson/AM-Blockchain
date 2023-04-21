<div align="center">
  <h3 align="center">AM Blockchain</h3>

  <p align="center">
    Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record
    <br />
    <a href="#Process-documentation"><strong>Go to visual documentation »</strong></a>
    <br />
    <br />
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Information-on-the-associated-paper">Information on the associated paper</a></li>
    <li><a href="#Goals-to-be-achieved-with-the-AM-Blockchain">Goals to be achieved with the AM Blockchain</a></li>
    <li><a href="#Architecture-of-the-AM-Blockchain-solution">Architecture of the AM Blockchain solution</a></li>
    <li><a href="#Preliminary-definitions">Preliminary definitions</a></li>
    <li>
      <a href="#Process-documentation">Process documentation</a>
      <ul>
        <li><a href="#Web-application">Web application</a></li>
        <li><a href="#Decentralized-storage">Decentralized storage</a></li>
        <li><a href="#Smart-contract">Smart contract</a></li>
        <li><a href="#Data-access-via-Etherscan">Data access via Etherscan</a></li>
      </ul>
    </li>
    <li><a href="#Evaluation">Evaluation</a></li>
  </ol>
</details>



<!-- INFORMATION -->
## Information on the associated paper

Title: &ensp;&emsp;&emsp;   Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record<br />
Authors: &emsp;             Erik Westphal, Benjamin Leiding, Hermann Seitz<br />
Journal: &nbsp;&emsp;       Journal of Industrial Information Integration<br />
DOI: &ensp;&emsp;&emsp;     tbd<br />

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GOALS -->
## Goals to be achieved with the AM Blockchain

The new AM part record is designed to increase the quality of additive manufacturing processes. In doing so, the implementation of concrete goals enables an evaluation of the quality increase compared to conventional quality management and quality assurance solutions. The goals to be achieved with the AM blockchain are thereby:
* A digital and decentralized documentation of the conventional quality documentation processes of the FDM process such as paper-based preparation protocols, material certificates, operator logs etc.
* A viable, functional and economical alternative to current solutions.
* A compact documentation of ML-based manufacturing data analysis during the printing process.
* A holistic, detailed traceable and forgery-proof documentation of the entire value chain as well as the information flow.
* A solution for location-independent and timely updating of manufacturing and quality information for all parties involved.
* A way to enable easier and faster part certification.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ARCHITECTURE -->
## Architecture of the AM Blockchain solution

The architecture and process flow for implementing digital manufacturing documentation based on the AM Blockchain are shown below:

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Architecture.jpg" width="800">
</p>

The presented architecture includes all involved parties, applications and processes of the conceptualized digital AM part record as well as their interactions with each other. All parties involved in the value chain are to access the smart contract, the decentralized storage system, and the blockchain via a web application with a frontend. These components and their associated processes are referred to as dApp and digitally connect the manufacturing side with the customer side. The shipping service provider is also integrated into the value chain via this. The parties involved interact with the dApp in different ways.<br />
<br />
Zur besseren Verständlichkeit werden nachfolgend auch noch ein UML component sowie ein UML communication diagram der vorgestellten Architektur aufgefürt:

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Architecture.jpg" width="800">
</p>

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Architecture.jpg" width="800">
</p>

<br />
The following images illustrates the interaction between the individual participants in the manufacturing process within the smart contract once again in great detail in the form of a sequence diagram.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_SequenceDiagram.jpg" width="800">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- PRELIMINARY DEFINITIONS -->
## Preliminary definitions

Within the AM Blockchain concept, the following aspects are defined:

**Participants and ethereum addresses**
* AMChain smart contract
   ```sh
   0x34A253F8E74460F264A902E305990Df65FA6C5Ce
   ```
* Manufacturer
   ```sh
   0xebdc7eAdBCc95aa5911A571cC589B0A42119D5dD
   ```
* Shipper
   ```sh
   0xA4084Fc2FeCBC4E20BaA2b5FA9Af3f5C72906536
   ```
* Sinterer
   ```sh
   0xadbe1C35f796C709A800DeF7A2e08ec34A2C139E
   ```
* Customer
   ```sh
   0x5c6743508a15829E7bcb0484AFEfB07f88BA6Ce5
   ```

**Assets**<br />
* ID and CID of the parts<br />
  `_partID` `_IPFS_CID`

**Transactions**<br />
* Manufacturer<br />
  `Created` `RequestShippingSinterer`
* Shipper<br />
  `AcceptShippingSinterer` `CompleteShippingSinterer`
* Sinterer<br />
  `ReceivedShippingSinterer` `Sintered` `RequestReshippingManufacturer`
* Shipper<br />
  `AcceptReshippingManufacturer` `CompleteReshippingManufacturer`
* Manufacturer<br />
  `ReceivedReshippingManufacturer` `Checked` `RequestDeliveryCustomer`
* Shipper<br />
  `AcceptDeliveryCustomer` `CompleteDeliveryCustomer`
* Customer<br />
  `ReceivedDeliveryCustomer` `Accepted` or `Declined`

**Events**<br />
* Manufacturing sequence<br />
  `OrderCreated` `OrderRequestShippingSinterer`<br />
* Shipment to Sinterer sequence<br />
  `OrderAcceptShippingSinterer` `OrderCompleteShippingSinterer` `OrderReceivedShippingSinterer`<br />
* Sintering sequence<br />
  `OrderSintered` `OrderRequestReshippingManufacturer`<br />
* Shipment back to Manufacturer sequence<br />
  `OrderAcceptReshippingManufacturer` `OrderCompleteReshippingManufacturer` `OrderReceivedReshippingManufacturer`<br />
* Quality control sequence<br />
  `OrderChecked` `OrderRequestDeliveryCustomer`<br />
* Delivery to Customer sequence<br />
  `OrderAcceptDeliveryCustomer` `OrderCompleteDeliveryCustomer` `OrderReceivedDeliveryCustomer`<br />
* Customer decision sequence<br />
  `OrderAccepted` `OrderDeclined`



<!-- Documentation -->
## Process documentation

In order to be able to evaluate the functionalities of the AM Blockchain solution, real manufacturing processes were run through and the data was recorded via the AM part record. In the course of this, all developed applications (web application, decentralized storage, smart contract, data access via Etherscan) were tested and validated.

<p align="right">(<a href="#top">back to top</a>)</p>



### Web application

First, the part manufacturer logs into the developed web application and creates a part record for a new part.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_WebApp_Login.jpg" width="700">
</p>

All relevant quality information is then stored digitally for this part.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_WebApp_Insights.jpg" width="700">
</p>

Furthermore, quality documents are created during production and the file and document names are also inserted into the web application. Finally, a summary of all information is extracted via the web application in the form of a JSON file.

For example, the print report `DO-04_PrintReport_LFM-0122-100-001.pdf` is considered as a quality document.
A reference to each quality document is stored among other information in the `ID1.json` file to the [Data](https://github.com/eedinson/AM-Blockchain/tree/main/data) for the respective component.

<p align="right">(<a href="#top">back to top</a>)</p>



### Decentralized storage

All created documents as well as the JSON file with the collected information about the part production are uploaded to a folder in the decentralized storage system IPFS. A CID is generated under which the data can be accessed in the IPFS.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_IPFS_Files.jpg" width="700">
</p>

All folders in the IPFS have a uniform folder structure in which the individual quality documents and production data are stored in a structured manner. Each document is in turn linked to its own CID, so that only access to individual files is possible. 

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_IPFS_PartDocuments.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



### Smart contract

After all data is uploaded to the IPFS, CID and other manufacturing information is inserted into the developed and deployed smart contract via the Remix IDE.<br />
<br />
The various accounts of the process participants are simulated via Metamask. For this purpose, each participant account is created in Metamask and the respective Ropsten Ethereum address is written into the smart contract. In the "Injected Web3" environment using the "creatOrder" function programmed with Solidity, the component name, CID and participant accounts are then stored in the smart contract and saved on-chain in the Ropsten ethereum blockchain.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_SmartContract_CreateOrder.jpg" width="700">
</p>

The "createOrder" function is executed by the manufacturer, which creates a new part record by entering the partID and IPFS_CID in the smart contract. The transaction takes place from the ethereum address of the manufacturer to the address of the smart contract. Furthermore, it can be seen in the logs that an event was successfully executed and the creation of the contract and indexing of a new part was completed.<br />

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_SmartContract_FunctionLogs.jpg" width="1200">
</p>

Subsequently, all further functions of the smart contract are executed successfully. This is fully documented in the [Smart contract.md](https://github.com/eedinson/AM-Blockchain/blob/main/documentation/SmartContract.md).

<p align="right">(<a href="#top">back to top</a>)</p>



### Data access via Etherscan

Parallel to the manufacturing documentation, the data stored on-chain can be continuously viewed via the blockchain explorer Ropsten Etherscan. To do this, the address of the smart contract must first be entered into the explorer to gain access to the documentation.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Etherscan_ContractSearch.jpg" width="700">
</p>

In order to be able to fully view the documentation and make queries to the smart contract, it must first be verified and published. This process is described in more detail in [Etherscan.md](https://github.com/eedinson/AM-Blockchain/blob/main/documentation/Etherscan.md).<br />
<br />
The associated information stored on-chain can then be read out via a data query for the corresponding indexed parts. 

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Etherscan_ContractQuery.jpg" width="700">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[architecture]: https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Architecture.jpg
