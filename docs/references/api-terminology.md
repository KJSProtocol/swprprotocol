# API Terminology

This document defines common terms used when interacting with SWPR API endpoints or SDK methods.

## Request Object
A structured JSON payload sent to initiate actions such as:
- scanning for dust  
- recovering dust  
- checking conversion status  

## Response Object
A structured reply containing:
- status  
- data  
- error messages (if any)  
- batch metadata  

## Fragment List
A list of detected dust fragments, including:
- token type  
- amount  
- chain  
- classification status  

## Batch Object
A standardized representation of grouped dust ready for conversion.

Contains:
- chain  
- value estimate  
- routing hints  
- fragment IDs  

## Converted Batch
Output after conversion, containing:
- SWPR value  
- logs  
- metadata  
- user allocation details  

## Identifier
A unique ID referencing:
- batches  
- conversions  
- logs  
- users (hashed)  
