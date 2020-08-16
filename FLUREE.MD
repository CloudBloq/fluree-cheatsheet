# Fluree

Fluree is a web3 data platform. It leverages Blockchain technology to make storage of data secure, available and decentralized. This cheatsheet features some API endpoints to help you get started with FLuree. 


<br>

## Keywords

| Keyword | Description |
| ------- | ----------- |
| Accessible | Fluree makes data Accessible to a wider range of users by enforcing security at the data layer. |
| Decentralization | Fluree can run on a network of servers that participate in Transaction validation. It uses algorithms like RAFT or pBFT to facilitate consensus. |
| F.A.I.R. | F.A.I.R. stands for Findable, Accessible, Interoperable and Reusable. |
| Findable | Fluree makes data Findable by storing and indexing metadata for each transaction. |
| Immutable | The data stored in Fluree can be updated but cannot be deleted. The record of the previous data exists in the previous blocks |
| Interoperable | Fluree enforces Interoperability by enforcing security at data layer and thus data can be used by a wider range of users. |
| Integrity | Fluree uses Tamper-proof blockchain (SHA3-256) for extreme data integrity. |
| Query | Query is a read operation on a ledger. It does not lead to creation of Flakes |
| Reusable | In order for data to be re-used, data must come with descriptive metadata on its usage rights. |
| Schema | Schema in Fluree consists of Collections and Predicates |
| Transaction | Any operation on a Ledger that leads to generation of Flakes like create, update and delete |


<br>

## Concepts

| Keyword | Description |
| ------- | ----------- |
| Auth | Auth is used to determine identity in Fluree that helps in restricting data access |
| Block | Contains a group of atomic updates made to a Ledger at a given point in time. Each block is linked to the previous block |
| Collection | Collections are analogous to a table in a relational database |
| Flakes | A specific fact about a subject at a specific point in time |
| Fuel | Fuel is a measure of the amount of computation a particular Query or Transaction takes. It depends on a number of factors. |
| Ledger | A record of changes made to Collections till a specific Block. |
| Object | Value of an Subject - Predicate combination |
| Predicates | Predicates are analogous to columns in a relational database |
| RDF Triple | Subject - Predicate - Object together is called a RDF Triple |
| Role | Role in Fluree can have multiple Rules to implement security |
| Rule | Rule in Fluree is used to restrict access to Collections inside a Ledger. Each rule can have multiple associated Smart Functions |
| Smart Functions | Smart Functions in Fluree help to set permissions on data |
| Snapshot | A backup of a Ledger upto a specific Block |
| Subject | Subject is an item in a collection. It is analogous to a row in a relational database |
| User | User is one of the default collection available in every Ledger. User can have multiple Roles and Auth |
