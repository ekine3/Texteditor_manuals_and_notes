# Notes of use: Visidata
> ekine 2026

## Basic navigation
You can move in visidata ussing the arrow keys as in most spreadsheet editors. The movement also can be done using the *h* left, *j* down, *k* up and *l* down.  

You can go to left corner of the table with *gh*, to the right side of the table with *l*, *gj* to the lowest part of the file and *gk* to the upper side of the file.  

To move the current row upwards one line *K*, *J* to move the row downwards.  
To move the whole column to the left *H* and *L* to move ir to the right.  



## Add new rows and tables
To add a new blank row after the cursor *a*.  
To add a new column at the right of the cursor *za*, this will trigger a confirmation prompt asking for the name of the header; to edit the column's header use *^*.  

To delete the row in the cursor use the *d* key.  
To delete the column in the cursor use the hypen *-*.  

To copy the current row use *y* and use the key *p* to paste it in the next row after the cursor and the *P* key to paste in the row before the cursor.  
To copy the column use *:copy column* by default the system paste the copied column after the current one with a default header.  

## Edit contents
To edit cell contents use the *e* key, to clear cell content *del* or *zd*, to copy cell contents use *zy* and *zp* to paste the content.  

## Edit files
To save the file user *Crtl+s*.  
To exit the editor *Crtl+q*.  

## Other functions
* To save the command log of the current sheet use *Ctrl+d* to save it to an independent file.  
* Use *o* to open new files or sheets, use *Shift+s* to navigate sheets and *d* to close inside the navigator menu.  

## Working with CSV files
**Comma Sepparated Values** files or CSV files, registered as *text/csv* MIME type, are documents that follow these basic rules of format:  
1. Each record (row) is located on a separated line, delimited by a line break (CRLF)  
> aaa,bbb,ccc CRLF  
> xxx,yyy,zzz CRLF  

2. The last record may or may not have and ending line break  
3. There might be an optional (but usual) header line appearing at the first line of the file. This header will contain names corresponding to the fields in the file and **should contain the same number of fields** as the records in the rest of file. The presence or absence should be indivated via the optional *header* parameter of this MIME type.  
4. Within the header and each record, here may be one or more fields separated by commas \,. Each line should contain the same number of fields throughout the file. Spaces are considered part of a field. The last record must not be followed by a comma.  
> (last record) aaa,bbb,ccc  
5. Each field may be enclosed in double quotes *\"*. If fields are not enclosed with double quotes, then double quotes may not appear inside the fields.  
6. Fields containing line breaks (CRLF), double quotes \", and commas \, should be enclosed in double quotes.  
> "aaa","Doe, John" (not tested)  
7. If double quotes are used to enclose fields, then a double quote appearing inside a field must be escaped by preceeding it whith another double quote.  
> "aaa","b""bb","ccc"  

### What is a MIME type?
**Media types** formerly known as **Multipurpose Internet Mail Extensions** (MIME) indicate the nature and format of a document.  
MIME types are standarized in *Internet Engineering Task Force*'s (IETF) RFC 6838 (*Request for comments*).  
The Internet Assigned Numbers Authority (IANA) is responsible for all official MIME types, this is important because browsers use MIME types and not file extensions to determine how to process a URL. It's important that web servers send the correct MIME type in the response *Content-Type* header to avoid browser's misinterpret of contents and file mishanlde.  

## References
* Internet Engineering Task Force (2020). *What is an RFC*.  
	* <https://www.rfc-editor.org/series/rfc/>  

* MDN (2026). *Media types (MIME types)*.  
	* <https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/MIME_types>  

* Singer-Vine, Jeremy (2021). *An introduction to VisiData*.  
  * <https://jsvine.github.io/intro-to-visidata/index.html>  

* Pswanson, Paul (2026). *Visidata*.  
  * <https://www.visidata.org/>  

* Abhisheck, Ray (2026). *CSV escape characters*.  
	* <https://www.importcsv.com/blog/csv-escape-characters>  

* Shafranovich, Y (2005). *RFC 4180: Common format and MIME type for Comma Sepparated Values (CSV) files*.  
	* <https://www.rfc-editor.org/info/rfc4180/>  
