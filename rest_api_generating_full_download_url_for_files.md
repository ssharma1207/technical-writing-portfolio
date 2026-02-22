---
title: REST API - Generating Full Download URL for Files
nav_text: Generating Full Download URL for Files
heading: REST API - Generating Full Download URL for Files
description: REST API - Generating Full Download URL for Files
variables:
  ItemKey: features/rest_api/t_restapi_generate_full_download_url.htm
---


You can configure the Upload Drive or ${{ upload_store }} to generate a full download URL for the file. When you run the Upload Drive or ${{ upload_store }} APIs to view the properties of a file, by default, the API response will list a relative download URL for the file.

## Procedure

1. On the Server computer, add the GenerateFullDownloadURL additional setting as shown in the following table.

    For instructions about adding the additional setting from the Server User Interface, see $[Adding an Additional Setting](doc:docs/server_management/troubleshooting/additional_settings/adding_additional_setting_from_server_ui).

    /// html | table.table.table-bordered
    //// html | tr
    ///// html | th
        markdown: block

    Property
    /////
    ///// html | th
        markdown: block

    Value
    /////
    ////
    //// html | tr
    ///// html | td
        markdown: block

    Name
    /////
    ///// html | td
        markdown: block

    $[GenerateFullDownloadURL](https://documentation.example.com/additionalsetting/details?name=GenerateFullDownloadURL)
    /////
    ////
    //// html | tr
    ///// html | td
        markdown: block

    Category
    /////
    ///// html | td
        markdown: block

    ServerDB.GlobalParam
    /////
    ////
    //// html | tr
    ///// html | td
        markdown: block

    Type
    /////
    ///// html | td
        markdown: block

    Integer
    /////
    ////
    //// html | tr
    ///// html | td
        markdown: block

    Value
    /////
    ///// html | td
        markdown: block

    1 \- to generate a full download URL

    0 \- to view a relative download URL
    /////
    ////
    ///

2. On the ${{ webserver }}, restart Internet information Services \(IIS\).
