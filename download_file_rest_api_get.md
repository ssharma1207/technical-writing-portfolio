---
title: 'Download a File (REST API: GET)'
nav_text: Download a File
heading: 'Download a File (REST API: GET)'
description: 'Download a File (REST API: GET)'
variables:
  ItemKey: features/rest_api/operations/get_file_download.htm
---


This operation downloads a backed up file on your laptop computer.

/// note | Note
 Downloading a folder is currently not supported using this operation.
///

## Request

### Syntax

```
GET $[webservice]/stream/action/download?appid=$[appId]&path=$[path] HTTP/1.1
Host: $[host name]
Accept: application/xml
Authtoken: $[authentication token]
```

where *\<webservice\>* is the root path used to route the API requests to the ${{ webserver }}. 

For more information, see $[Available Web Services for REST API](https://documentation.example.com/45592.htm).

### Request Parameters

/// html | table.table.table-bordered
//// html | tr
///// html | th
    markdown: block

Name
/////
///// html | th
    markdown: block

Description
/////
///// html | th
    markdown: block

Required
/////
////
//// html | tr
///// html | td
    markdown: block

appid
/////
///// html | td
    markdown: block

The subclient ID of the subclient that was used to backup the file. If the subclient ID is not known, use the $[GET Subclient API](doc:host/tools_utilities/developer_tools/rest_api/rest_api_reference/subclient_operations/rest_api_get_subclient) to retrieve it.
/////
///// html | td
    markdown: block

Yes
/////
////
//// html | tr
///// html | td
    markdown: block

path
/////
///// html | td
    markdown: block

The path to the file on your laptop computer. Specify the path relative from the root.

////// note | Note
 The path must be URL encoded before they are sent in the request.
//////
/////
///// html | td
    markdown: block

Yes
/////
////
///

### Request Headers

/// html | table.table.table-bordered
//// html | tr
///// html | th
    markdown: block

Name
/////
///// html | th
    markdown: block

Description
/////
////
//// html | tr
///// html | td
    markdown: block

Host
/////
///// html | td
    markdown: block

The host name of the ${{ webserver }} or the ${{ console }} used in the API request.
/////
////
//// html | tr
///// html | td
    markdown: block

Accept
/////
///// html | td
    markdown: block

The format of the response. Valid values are: application\/xml or application\/json.
/////
////
//// html | tr
///// html | td
    markdown: block

Authtoken
/////
///// html | td
    markdown: block

The authentication token received after successfully logging on. For details on receiving an authentication token, see $[Authentication](doc:host/tools_utilities/developer_tools/rest_api/rest_api_authentication_post_login).
/////
////
///

## Examples

### Sample Request

```
GET $[webservice]/stream/action/download?appid=$[4]&path=$[C:\Log Files\Gitlab.log] HTTP/1.1
Host: $[client.mydomain.com]
Accept: application/xml
 Authtoken: $[QSDK 38568012f4d1e8ee1841d283a47aa3ba78e124ea58354b5fc60f4dab8a63347d05cf5552484dafda3bfa4c5db84e580b1cb37bcf8e65b39f7f8549a443e6f78a2c7be3f31b3d845e24776c835e498e8e883bb40c46bd15af4f40ca94e823acedcdd4e9659e74b34a07a85c4586cd2ed914b6dce015874783ef768fda78183a4208930954a377f66eb56c8b92cexampl4s437a19317ca6ce7f3233d5a01aca35dbad93468b833f2cf71010809006a937670adce711ca8be46638e8]
```

## Supported Error Codes

/// html | table.table.table-bordered
//// html | tr
///// html | th
    markdown: block

Code
/////
///// html | th
    markdown: block

Status
/////
///// html | th
    markdown: block

Description
/////
////
//// html | tr
///// html | td
    markdown: block

400
/////
///// html | td
    markdown: block

Bad Request
/////
///// html | td
    markdown: block

The request is missing required parameters.
/////
////
//// html | tr
///// html | td
    markdown: block

403
/////
///// html | td
    markdown: block

Forbidden
/////
///// html | td
    markdown: block

Download operation is not allowed. This can happen if you attempt to download a folder.
/////
////
//// html | tr
///// html | td
    markdown: block

404
/////
///// html | td
    markdown: block

Not Found
/////
///// html | td
    markdown: block

The specified file does not exist.
/////
////
///
