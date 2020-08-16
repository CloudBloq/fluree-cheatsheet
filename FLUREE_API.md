# API Endpoints

There are two types of Fluree we can use:

* Fluree Anywhere
* Fluree On Demand


The base address of all endpoints will be `http://localhost:8080` by default if we are using Fluree Anywhere. Fluree On Demand users will have to set up an Account and then login into Fluree and get a token. This token can then be used to call the Fluree API. 

<br>

## Main Endpoints

| Action | Endpoint | Example | Description |
| ------ | -------- | ------- | ----------- |
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


<br><br>

## Test Endpoints

| Action | Endpoint | Example | Description |
| ------ | -------- | ------- | ----------- |
| Generate Flakes | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/gen-flakes` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-gen-flakes) | Returns the list of flakes that would be added to a ledger if a given transaction is issued | 
| Query With | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/query-with` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-query-with) | Returns the results of a query using the existing database flakes, including flakes that are provided with the query. |
| Test Transact With | `/fdb/[NETWORK-NAME]/[DBNAME-OR-DBID]/test-transact-with` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-test-transact-with) | Given a valid set of flakes that could be added to the database at a given point in time and a transaction, returns the flakes that would be added to a ledger if a given transaction is issued. |


<br><br>

## Password Authentication Endpoints

| Action | Endpoint | Example | Description |
| ------ | -------- | ------- | ----------- |
| Generate Token | `/fdb/[NETWORK-NAME]/[DBID]/pw/generate` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-generate) | Returns a valid token for a given user or role. Sets a valid password for that user or role. | 
| Renew Token | `/fdb/[NETWORK-NAME]/[DBID]/pw/renew` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-renew) | Given a token in the header and a new expiration time, returns a new token for a given user or role. |
| Login | `/fdb/[NETWORK-NAME]/[DBID]/pw/login` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-login) | Given a password and user or auth id, returns a valid token. |


<br><br>

## Other Endpoints

| Action | Method | Endpoint | Example | Description |
| ------ | ------ | -------- | ------- | ----------- |
| Block Stats | POST | `/fdb/[NETWORK-NAME]/[DBID]/block-range-with-txn` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-block-range-with-txn) | Returns block data, signatures, instant, hash, flakes and transactions | 
| Health | GET | `/fdb/health` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-health) | Can be used to test application status | 
| Ledger Stats | POST | `/fdb/[NETWORK-NAME]/[DBID]/ledger-stats` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-ledger-stats) | General ledger stats, including status, # flakes, current block, and size (kb). | 
| Generate Public / Private keys | GET | `/fdb/new-keys` | [Example](https://docs.flur.ee/api/downloaded-endpoints/downloaded-examples#-new-keys) | Get a pair of Public / Private Keys | 

