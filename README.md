<h1>ChunkedFileDownloader - Oracle APEX Region Plugin</h1>

Plug-in designed to enhance data export experiences from Interactive Grids or Reports by enabling multi-file downloads with configurable chunk sizes and dynamic filenames.

<h2>Installation</h2>
Import plugin file "region_type_plugin_chunkedfiledownloader.sql" from Source directory into your application.

<h2>How to Use</h2>
  1) Create a new Region on your APEX page and select the plugin "Chunked File Downloader [Plug-in]" as the region type.
  2) In the Custom Attributes section of the plugin settings, configure the following:
    2.1) Chunk Size: Optional. Map to a page item (e.g., number field). Allows the user/developer to control the file chunk size during download.
    2.2) File Name: Optional. Map to a page item (e.g., text field). Used to specify the custom name of the downloaded file.
    2.3) Include Timestamp: Optional. Map to a checkbox page item with values Y / N. When set to Y, a timestamp will be added to the file name.
    2.4) Button Label: Optional. Provide a label for the download button that will appear in the report toolbar.
    2.5) Target Report Static ID: Mandatory. Specify the static ID of the target Interactive Grid (IG) or Interactive Report (IR). The plugin will use this to insert the download button into the report’s toolbar.          Make sure the toolbar is enabled.
    2.6) Max Rows: Mandatory. Define the maximum number of rows allowed for download. This is used for logic control within the plugin.
    2.7) Bind Items: Mandatory. List the bind items used in your report’s SQL query (comma-separated), so the plugin can properly fetch and use those values during export.
<h2>Important Notes</h2>
1) The target IG/IR must use a static SQL query as the data source. The plugin does not support function-returning SQL or direct table references.
2) Page items for Chunk Size, File Name, and Include Timestamp are optional.
    2.1) Create and map these only if you want to allow user-level control over these values.
    2.2) If not mapped, the plugin will use default or static values defined in the plugin settings.
3) The plugin automatically inserts the download button into the toolbar of the target IG/IR region, based on the provided static ID.
4) Ensure that the toolbar is enabled in the target report. If the toolbar is not visible or properly configured, the download button will not appear.

<h2>Images For Reference</h2>


    
<h2>Demo</h2>


