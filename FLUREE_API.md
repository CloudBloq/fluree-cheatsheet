# Fluree

Fluree is a web3 data platform. It leverages Blockchain technology to make storage of data secure, available and decentralized. This cheatsheet features some API endpoints to help you get started with FLuree. 


<br>

## Keywords

| Keyword | Description |
| ------- | ----------- |
| Auth | Auth is used to determine identity in Fluree that helps in restricting data access |
| Block | Contains a group of atomic updates made to a Ledger at a given point in time. Each block is linked to the previous block |
| Collection | Collections are analogous to a table in a relational database |
| Flakes | A specific fact about a subject at a specific point in time |
| Ledger | All instances of a specific db across all the blocks is called a Ledger. |
| Object | Value of an Subject - Predicate combination |
| Predicates | Predicates are analogous to columns in a relational database |
| Query | Query is a read operation on a ledger. It does not lead to creation of Flakes |
| RDF Triple | Subject - Predicate - Object together is called a RDF Triple |
| Role | Role in Fluree can have multiple Rules to implement security |
| Rule | Rule in Fluree is used to restrict access to Collections inside a Ledger. Each rule can have multiple associated Smart Functions |
| Schema | Schema in Fluree consists of Collections and Predicates |
| Smart Functions | Smart Functions in Fluree help to set permissions on data |
| Snapshot | A backup of a Ledger upto a specific Block |
| Subject | Subject is an item in a collection. It is analogous to a row in a relational database |
| Transaction | Any operation on a Ledger that leads to generation of Flakes like create, update and delete |
| User | User is one of the default collection available in every Ledger. User can have multiple Roles and Auth |


<br>

## API Endpoints

There are two types of Fluree we can use:

* Fluree Anywhere
* Fluree On Demand


The base address of all endpoints will be `http://localhost:8080` by default if we are using Fluree Anywhere. Fluree On Demand users will have to set up an Account and then login into Fluree and get a token. This token can then be used to call the Fluree API. 


### Main Endpoints

| Action | Endpoint | Example | Description |
| ------ | -------- | ------ | ---- | -------- | ----------- |
| Create Ledger | `/fdb/new-db` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-new-db) | Creates a new ledger | 
| List Ledgers | `/fdb/dbs` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-dbs) | Returns list of all ledgers in transactor group |
| Export Ledger | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/export` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-export) | Exports an existing ledger into either .xml or .ttl file |
| Delete Ledger | `/fdb/delete-db` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-delete-db) | Deletes the ledger but not the ledger files |
| Create Snapshot | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/snapshot` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-snapshot) | Creates a snapshot file from an existing ledger |
| List Snapshot | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/list-snapshots` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-list-snapshots) | Lists all local snapshots for an existing ledger |
| Add Server | `/fdb/add-server` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-add-server) | Dynamically add a server to the network |
| Remove Server | `/fdb/remove-server` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-remove-server) | Dynamically remove a server from the network |
| Query | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/query` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-query) | Send query in FlureeQL syntax |
| Multi-Query | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/multi-query` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-multi-query) | Send multiple queries in FlureeQL syntax |
| Block | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/block` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-block) | Send block queries in FlureeQL syntax |
| History | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/history` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-history) | Send history queries in FlureeQL syntax |
| Transact | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/transact` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-transact) | Send transactions in FlureeQL syntax |
| GraphQL | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/graphql` | [Query Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-graphql-query) <br> [Transaction Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-graphql-transaction) | Send queries in GraphQL syntax |
| SPARQL | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/sparql` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-sparql) | Send queries in SPARQL syntax |
| Command | `/fdb/[NETWORK-NAME]/[DBID]/command` | [Example](https://docs.flur.ee/guides/identity/signatures#signed-transactions) | Send signed queries and transactions in FlureeQL syntax |
| Reindex Ledger | `/fdb/[NETWORK-NAME]/[DBID]/reindex` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-reindex) | Reindex the specified ledger |
| Hide Flakes | `/fdb/[NETWORK-NAME]/[DBID]/hide` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-hide) | Hide Flakes that match the given pattern |
