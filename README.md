<h1>ChunkedFileDownloader - Oracle APEX Region Plugin</h1>

Plug-in designed to enhance data export experiences from Interactive Grids or Reports by enabling multi-file downloads with configurable chunk sizes and dynamic filenames.

![](https://github.com/SeemaChowdari/ChunkedFileDownloader/blob/main/chunkedfiledownloader.gif)

<h2>Installation</h2>
Import plugin file "region_type_plugin_chunkedfiledownloader.sql" from Source directory into your application.

<h2>How to Use</h2>
<ul>
  <li>Create a new Region on your APEX page and select the plugin <strong>"Chunked File Downloader [Plug-in]"</strong> as the region type.</li>
  <li>In the <strong>Custom Attributes</strong> section of the plugin settings, configure the following:
    <ul>
      <li><strong>Chunk Size</strong> (Optional): Map to a page item (e.g., number field). Allows the user/developer to control the file chunk size during download.</li>
      <li><strong>File Name</strong> (Optional): Map to a page item (e.g., text field). Used to specify the custom name of the downloaded file.</li>
      <li><strong>Include Timestamp</strong> (Optional): Map to a checkbox page item with values Y / N. When set to Y, a timestamp will be added to the file name.</li>
      <li><strong>Button Label</strong> (Optional): Provide a label for the download button that will appear in the report toolbar.</li>
      <li><strong>Target Report Static ID</strong> (Mandatory): Specify the static ID of the target Interactive Grid (IG) or Interactive Report (IR). The plugin will use this to insert the download button into the report’s toolbar. Make sure the toolbar is enabled.</li>
      <li><strong>Max Rows</strong> (Mandatory): Define the maximum number of rows allowed for download. This is used for logic control within the plugin.</li>
      <li><strong>Bind Items</strong> (Conditional): Required only if your SQL query contains bind variables. Provide a comma-separated list of those bind items so the plugin can resolve them correctly during export.</li>
    </ul>
  </li>
</ul>

<h2>Important Notes</h2>
<ul>
  <li>The target IG/IR must use a <strong>static SQL query</strong> as the data source.
    <ul>
      <li>The plugin does not support function-returning SQL or direct table references.</li>
    </ul>
  </li>
  <li><strong>Chunk Size</strong>, <strong>File Name</strong>, and <strong>Include Timestamp</strong> page items are optional.
    <ul>
      <li>Create and map these only if you want to allow user-level control over these values.</li>
      <li>If not mapped, the plugin will use default or static values defined in the plugin settings.</li>
    </ul>
  </li>
  <li>The plugin <strong>automatically inserts</strong> the download button into the toolbar of the target IG/IR region, based on the provided static ID.</li>
  <li>Ensure that the <strong>toolbar is enabled</strong> in the target report. If the toolbar is not visible or properly configured, the download button will not appear.</li>
</ul>
   
<h2>Demo</h2>
https://apex.oracle.com/pls/apex/r/work_sam/chunkedfiledownloader/report


