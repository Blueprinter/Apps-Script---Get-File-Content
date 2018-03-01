# Apps-Script---Get-File-Content
This code will get all content out of an Apps Script file.

This README file is not needed or used in the actual code.

There is only one file for the code, Code_GS.  Copy the code and paste it into your Apps Script code editor.

Run the function "myMainFunction" - In the drop down list of functions, choose "myMainFunction" - Click the "Run" button

This code does not require additional OAuth set up or getting any credentials or secret key.
This code gets and uses an existing OAuthToken that is managed internally by Apps Script Drive Service.

Using the code to get the file content out of an Apps Script file, you can get both the SOURCE file data and the TARGET file data, and then compare the two JSON objects.  Apps Script files store their content in a JSON object.  Each "file" is a property in the outer object.  There are three types of files:

server_js
html
appsscript

The "appsscript" type file is the manifest file.

The structure of the files object is as follows:

    {
      "files": [
      {
        "id": "739a57da-f77c-4e1a-96df-7d86ef227d62",
        "name": "Code",
        "type": "server_js",
        "source": "function doGet() {\n  return HtmlService.createHtmlOutputFromFile('index');\n}"
        },
    {
      "id": "2c7e8b5a-dbc5-4cd2-80e9-77b6291b3167",
      "name": "index",
      "type": "html",
      "source": "<html>\n  <body>\n    This is an update.  at 3:06\n  <\/body>\n<\/html>"
    },
    {
      "id": "c6205d38-7d02-4cea-9196-e4c0b3f636e8",
      "name": "Code_Two",
      "type": "server_js",
      "source": "function myFunction() {\n  \/\/This is a test\n  \/\/Test at 306\n}\n"
    },
    {
      "id": "5d92ac8c-1a0f-4b15-a1bf-faa27f97cb3f",
      "name": "appsscript",
      "type": "json",
      "source": "{\n  \"timeZone\": \"America\/New_York\",\n  \"dependencies\": {\n  },\n  \"exceptionLogging\": \"STACKDRIVER\"\n}"
    }
  ]
}
