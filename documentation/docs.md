<div align="center">
  <h3 align="center">AM Blockchain</h3>

  <p align="center">
    Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record
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
        <li><a href="#Create-part-record">Prerequisites</a></li>
        <li><a href="#Enter-quality-related-information">Enter quality-related information</a></li>
      </ul>
    </li>
    <li><a href="#Evaluation">Evaluation</a></li>
  </ol>
</details>



<!-- INFORMATION -->
## Information on the associated paper

Title: &ensp;&emsp;&emsp;   Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record<br />
Authors: &emsp;             Erik Westphal, Hermann Seitz, Benjamin Leiding, Max Muster<br />
Journal: &nbsp;&emsp;       ksdjbfd<br />
DOI: &ensp;&emsp;&emsp;     gfdghgh<br />

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
The following images illustrates the interaction between the individual participants in the manufacturing process within the smart contract once again in great detail in the form of a sequence diagram.

<p align="center">
 <img src="https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_SequenceDiagram.jpg" width="800">
</p>

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- PRELIMINARY DEFINITIONS -->
## Preliminary definitions

Within the AM Blockchain concept, the following aspects are defined:

**Participants**
`Manufacturer` `IPFS` `Smart contract` `Shipper` `Sinterer` `Customer`

**Assets**
`partID`

**Transactions**<br />
<br />

`Created` `RequestShippingSinterer`
`AcceptShippingSinterer` `CompleteShippingSinterer`
`ReceivedShippingSinterer` `Sintered` `RequestReshippingManufacturer`
`AcceptReshippingManufacturer` `CompleteReshippingManufacturer`
`ReceivedReshippingManufacturer` `Checked` `RequestDeliveryCustomer`
`AcceptDeliveryCustomer` `CompleteDeliveryCustomer`
`ReceivedDeliveryCustomer` `Accepted` `Declined`

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



<!-- MARKDOWN LINKS & IMAGES -->
[architecture]: https://github.com/eedinson/AM-Blockchain/blob/main/images/AMBlockchain_Architecture.jpg
