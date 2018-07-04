# GOB

Generic Disclosure of Basic Data

## Background

Basic data is the raw material for a large number of municipal processes.
Without these data, the processes can not be executed.

Basic data are recorded in basic registers (prescribed by law) and core registrations (prescribed by the Municipal Executive).

Some of these data are taken from their own municipal facilities (source system) and partly from national facilities.
The problem is that all these sources do not use one and the same data / message standard.
In-house customers make use of different systems in which the basic data are shown or processed.

The seven basic registers are:
1. persons (BRP)
2. addresses and buildings (BAG)
3. value of immovable property (BR WOZ)
4. small-scale topography (BRT)
5. large-scale topography (BGT)
6. Commercial register (HR)
7. Land Registry (BRK).

The eight core registrations are:
1. the municipal restriction registration (Wkpb)
2. the current height file in the Netherlands
3. areas
4. NAP
5. aerial photographs
6. measuring bolts
7. monuments
8. panorama images.

Three systems are in use for retrieving data from the source or the national facility, the management, the translation and the distribution of the basic data:
- DIVA for real estate data
- Makelaar suite for personal details
- Handelsregister and Neuron Communicator for BAG and WOZ data

Not all systems can handle the different deliveries.
A 'translation' is therefore necessary.
Within GOB, the basic data from the various source registrations are stored, processed and distributed in a format as defined in
[Stelselpedia](https://www.amsterdam.nl/stelselpedia/|Stelselpedia) and
[RSGB](https://www.gemmaonline.nl/index.php/Informatiemodel_Basis-_en_Kerngegevens_(RSGB))..

## Target

The aim of the project is to guarantee the delivery of high-quality basic data for municipal processes against minimal management efforts and costs.

With derived objectives:
- Customized deliveries

Many customers need data sets that are composed of multiple basic data.
There is therefore a need for functionality that enables customers to be served with customized deliveries.

- Integral quality management of the system

The project must manage the consistency, integrity and quality of the entire basic data system of Amsterdam,
including requirements for information management in the context of the archive law.

## Global structure

The GOB project is a modular system.

Each component within GOB has a well-defined function and can also be used separately from GOB.
Examples of components are the import of Neuron data, storage of Systematic data, deduction of mutations based on an import.

Communication between the components runs over a Message Broker.

Storage of data takes place in a database.

All components are fed from a data format based on Stelselpedia and RSGB.

Dependencies of specific message brokers or databases are encapsulated.
The choice for a specific message broker or database can be adjusted if necessary.

## Users

The users of GOB are civil servants, citizens and companies.

Officials within the municipality of Amsterdam use the data for support or as input for their work.

Citizens and companies have access to (the publicly available part of) the data via an API or web applications.
