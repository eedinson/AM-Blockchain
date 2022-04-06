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
    <li><a href="#Information on the associated paper">Information on the associated paper</a></li>
    <li><a href="#Goals to be achieved with the AM Blockchain">Goals to be achieved with the AM Blockchain</a></li>
    <li><a href="#Architecture of the AM Blockchain solution">Architecture of the AM Blockchain solution</a></li>
    <li><a href="#Preliminary definitions">Preliminary definitions</a></li>
    <li>
      <a href="#Process documentation">Process documentation</a>
      <ul>
        <li><a href="#Create part record">Prerequisites</a></li>
        <li><a href="#Enter quality-related information">Enter quality-related information</a></li>
      </ul>
    </li>
    <li><a href="#Evaluation">Evaluation</a></li>
  </ol>
</details>



<!-- INFORMATION -->
## Information on the associated paper

Title:    Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record
Authors:  Erik Westphal, Hermann Seitz, Benjamin Leiding, Max Muster
Journal:  ksdjbfd
DOI:      gfdghgh

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GOALS -->
## Goals to be achieved with the AM Blockchain

Durch die neue AM Bauteilakte soll eine Qualitätssteigerung bei der additiven Fertigung erzielt werden. Die Umsetzung konkreter Ziele ermöglicht dabei eine Bewertung der Qualitätssteigung im Vergleich zu konventionellen Qualitätsmanagement- und Qualitätssicherungslösungen. Die mit der AM Blockchain zu erreichenden Ziele sind dabei:
* Eine Digitalisierung und dezentrale Dokumentation konventioneller Qualitätsdokumentationsprozesse des FDM Prozesses wie bspw. papierbasierte Vorbereitungsprotokolle, Materialzertifikate, Bedienernachweise etc.
* Eine umsetzbare, funktionale und wirtschaftliche Alternative zu aktuell gängigen Lösungen.
* Eine kompakte Dokumentation von ML-basierten Fertigungsdatenanalysen während des Druckprozesses.
* Eine ganzheitliche, detailliert nachvollziehbare und fälschungssichere Dokumentation der gesamten Wertschöpfungskette sowie des Informationsflusses.
* Eine Lösung zur ortsunabhängigen und zeitigen Aktualisierung von Fertigungs- und Qualitätsinformationen für alle beteiligten Parteien.
* Eine Möglichkeit zur einfachen und schnellen Bauteilzertifizierung.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ARCHITECTURE -->
## Architecture of the AM Blockchain solution

Title:    Development of a blockchain-based quality assurance concept for a digital additive manufacturing part record
Authors:  Erik Westphal, Hermann Seitz, Benjamin Leiding, Max Muster
Journal:  ksdjbfd
DOI:      gfdghgh

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- PRELIMINARY DEFINITIONS -->
## Preliminary definitions

Within the AM Blockchain concept, the following aspects are defined:

**Participants**
`Manufacturer` `IPFS` `Smart contract` `Shipper` `Sinterer` `Customer`

**Assets**
`partID`

**Transactions**<br />

`Created` `RequestShippingSinterer`
`AcceptShippingSinterer` `CompleteShippingSinterer`
`ReceivedShippingSinterer` `Sintered` `RequestReshippingManufacturer`
`AcceptReshippingManufacturer` `CompleteReshippingManufacturer`
`ReceivedReshippingManufacturer` `Checked` `RequestDeliveryCustomer`
`AcceptDeliveryCustomer` `CompleteDeliveryCustomer`
`ReceivedDeliveryCustomer` `Accepted` `Declined`

**Events**<br />
Manufacturing sequence<br />
`OrderCreated` `OrderRequestShippingSinterer`<br />
Shipment to Sinterer sequence<br />
`OrderAcceptShippingSinterer` `OrderCompleteShippingSinterer` `OrderReceivedShippingSinterer`<br />
Sintering sequence<br />
`OrderSintered` `OrderRequestReshippingManufacturer`<br />
Shipment back to Manufacturer sequence<br />
`OrderAcceptReshippingManufacturer` `OrderCompleteReshippingManufacturer` `OrderReceivedReshippingManufacturer`<br />
Quality control sequence<br />
`OrderChecked` `OrderRequestDeliveryCustomer`<br />
Delivery to Customer sequence<br />
`OrderAcceptDeliveryCustomer` `OrderCompleteDeliveryCustomer` `OrderReceivedDeliveryCustomer`<br />
Customer decision sequence<br />
`OrderAccepted` `OrderDeclined`
