# Fluree

Fluree is a web3 data platform. It leverages Blockchain technology to make storage of data secure, available and decentralized. This cheatsheet features some API endpoints to help you get started with FLuree. 

<br>

## API Endpoints

The base address of all endpoints will be `http://localhost:8080` by default. All the endpoints mentioned are post requests unless mentioned otherwise. The endpoints use the bas


### Main Endpoints

| Action | Endpoint | Description |
| ----------- | ----------- | --------- |
| Create Ledger | `/fdb/new-db` | Creates a new ledger |
| List Ledgers | `/fdb/dbs` | Returns list of all ledgers in transactor group |
| Export Ledger | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/export` | Exports an existing ledger into either .xml or .ttl file |
| Delete Ledger | `/fdb/delete-db` | Deletes the ledger but not the ledger files |
| Create Snapshot | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/snapshot` | Creates a snapshot file from an existing ledger |
| List Snapshot | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/list-snapshots` | Lists all local snapshots for an existing ledger |
| Add Server | `/fdb/add-server` | Dynamically add a server to the network |
| Remove Server | `/fdb/remove-server` | Dynamically remove a server from the network |
| Query | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/query` | Send query in FlureeQL syntax |
| Multi-Query | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/multi-query` | Send multiple queries in FlureeQL syntax |
| Block | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/block` | Send block queries in FlureeQL syntax |
| History | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/history` | Send history queries in FlureeQL syntax |
| Transact | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/transact` | Send transactions in FlureeQL syntax |
| GraphQL | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/graphql` | Send queries in GraphQL syntax |
| SPARQL | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/sparql` | Send queries in SPARQL syntax |
| Command | `/fdb/[NETWORK-NAME]/[DBID]/command` | Send signed queries and transactions in FlureeQL syntax |
| Reindex Ledger | `/fdb/[NETWORK-NAME]/[DBID]/reindex` | Reindex the specofoed ledger |
| Hide Flakes | `/fdb/[NETWORK-NAME]/[DBID]/hide` | Hide Flakes in the specified pattern |
