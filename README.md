# OrcaDB 🌊🐋

Welcome to **OrcaDB**, the lightweight, JSON file-based database module for Node.js. 🌟 Whether you're developing a small prototype or a full-fledged application, OrcaDB offers a simple and efficient way to manage your data. Dive in and explore the depths of what OrcaDB can do for you! 🐬

## Installation 🚀

Getting started with OrcaDB is a breeze. Install it via npm with a single command:

```sh
npm install orcadb
Usage 📚
Here's a comprehensive guide to using OrcaDB. Follow along to learn how to harness the full power of this module.

Importing the Module
First, require the orcadb module in your project:

const orcadb = require('orcadb');
Adding Key-Value Pairs ➕
To add a key-value pair to the database, use the add method. This method takes two arguments: the key and the value you want to store. For example:

orcadb.add('exampleKey', 'exampleValue');
console.log(orcadb.get('exampleKey')); // Outputs: exampleValue
Retrieving Values 🔍
To retrieve the value of a specific key, use the get method. This method takes one argument: the key you want to retrieve. For example:

const value = orcadb.get('exampleKey');
console.log(value); // Outputs: exampleValue
Removing Key-Value Pairs ➖
To remove a key-value pair from the database, use the remove method. This method takes one argument: the key you want to remove. For example:

orcadb.remove('exampleKey');
console.log(orcadb.get('exampleKey')); // Outputs: undefined
Adding Multiple Key-Value Pairs
You can add multiple key-value pairs using the add method multiple times. For example:

orcadb.add('key1', 'value1');
orcadb.add('key2', 'value2');
console.log(orcadb.getAll()); // Outputs: { key1: 'value1', key2: 'value2' }
Searching Key-Value Pairs 🔎
To search for key-value pairs based on a predicate, use the search method. This method takes a predicate function that receives the value and key as arguments and returns a boolean. For example:

const results = orcadb.search((value, key) => key.startsWith('key'));
console.log(results); // Outputs: [{ key: 'key1', value: 'value1' }, { key: 'key2', value: 'value2' }]
Removing by Predicate 🗑️
To remove key-value pairs based on a predicate, use the removeBy method. This method takes a predicate function that receives the value and key as arguments and returns a boolean. For example:

orcadb.removeBy((value, key) => key.startsWith('key'));
console.log(orcadb.getAll()); // Outputs: {}
Updating Values ✏️
To update the value of a specific key, use the update method. This method takes two arguments: the key and the new value. For example:

orcadb.add('exampleKey', 'exampleValue');
orcadb.update('exampleKey', 'newValue');
console.log(orcadb.get('exampleKey')); // Outputs: newValue
Clearing the Database 🧹
To clear all key-value pairs from the database, use the clear method. For example:

orcadb.clear();
console.log(orcadb.getAll()); // Outputs: {}
Counting Key-Value Pairs 📊
To count the number of key-value pairs in the database, use the count method. For example:

console.log(orcadb.count()); // Outputs: 0
Checking if a Key Exists ✔️
To check if a specific key exists in the database, use the exists method. This method takes one argument: the key you want to check. For example:

console.log(orcadb.exists('exampleKey')); // Outputs: false
Getting the First Key-Value Pair
To get the first key-value pair in the database, use the getFirst method. For example:

orcadb.add('key1', 'value1');
orcadb.add('key2', 'value2');
console.log(orcadb.getFirst()); // Outputs: { key: 'key1', value: 'value1' }
Getting the Last Key-Value Pair
To get the last key-value pair in the database, use the getLast method. For example:

console.log(orcadb.getLast()); // Outputs: { key: 'key2', value: 'value2' }
Getting All Keys 🗝️
To get all keys in the database, use the getKeys method. For example:

console.log(orcadb.getKeys()); // Outputs: [ 'key1', 'key2' ]
Getting All Values 📋
To get all values in the database, use the getValues method. For example:

console.log(orcadb.getValues()); // Outputs: [ 'value1', 'value2' ]
Support 💬
For support, join our Discord server: https://discord.gg/pqSaauK8kr or contact FeraxRD.

License 📜
This project is licensed under the MIT License.
