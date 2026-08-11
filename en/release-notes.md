<!-- pre-align:aligned sig=65087328ad5c -->

<a id="content-delivery-image-manager-release-notes"></a>
## Content Delivery > Image Manager > Release Notes { #content-delivery-image-manager-release-notes }

<a id="march-24-2026"></a>
### March 24, 2026 { #march-24-2026 }
<a id="march-24-2026-feature-updates"></a>
#### Feature Updates
* [API] Added API v3.0 with token authentication
<a id="march-24-2026-bug-fixes"></a>
#### Bug Fixes
* [API] Fixed thumbnail creation failure when file name contains &

<a id="november-1-2023"></a>
### November 1, 2023 { #november-1-2023 }
<a id="november-1-2023-feature-updates"></a>
#### Feature Updates
* [API] Added List Folder Default Properties API
* [Console] Removed folder size and number files from the folder properties
<a id="november-1-2023-bug-fixes"></a>
#### Bug Fixes
* [API] Fixed operation error for webp files
* [Console] Fixed an error where files are not uploaded even though they are an allowed extensions

<a id="september-14-2023"></a>
### September 14, 2023 { #september-14-2023 }
<a id="september-14-2023-feature-updates"></a>
#### Feature Updates
* [API] Added supported file format (.webp)
* [API] Changed uploaded image size limit (12 MB > 50 MB)
* [API] Added the origial URL path to responses

<a id="september-27-2022"></a>
### September 27, 2022 { #september-27-2022 }
<a id="september-27-2022-service-name-change"></a>
#### Service Name Change
* Changed the service name to Image Manager

<a id="february-22-2018"></a>
### February 22, 2018 { #february-22-2018 }
<a id="february-22-2018-feature-updates"></a>
#### Feature Updates
* [Console] Changed the method of accessing 'Thumbnail Option Management' from a button within the 'Folder and Image File Management' to a top menu  
	* Folder and image file management is accessible from 'File View'
	* Thumbnail option management is accessible from 'Operation Setting'
* [Console] [Folder and Image File Management](./console-guide/#_1)
	* Added the feature of moving folder paths on the existing page, as well as the folder tree feature 
	* Added the feature of moving to a previous folder on the folder list

<a id="february-22-2018-bug-fixes"></a>
#### Bug Fixes 
* [API] Fixed a bug where, when sending a request with operation-exec API, the request is handled as a success response regardless of the task if the file (or operation) is invalid
	* Processed as a failed response when task items (queues) are unavailable 
	* Processed as a partial success response when task items (queues) count is not consistent with the request count 

<a id="december-21-2017"></a>
### December 21, 2017 { #december-21-2017 }
<a id="december-21-2017-feature-updates"></a>
#### Feature Updates
* [API] Added the display of whether the files have been overwritten to the processing result callback 
	* [Uploading Multiple Images](./api-guide/#_16)
	* [Executing Image Operations](./api-guide/#_37)
* [Console] Changed UI design of the page 

<a id="november-30-2017"></a>
### November 30, 2017 { #november-30-2017 }
<a id="november-30-2017-more-features"></a>
#### More Features 
* [API] Added the processing result callback feature
	* Added the feature of sending processing result to callbackUrl when callbackUrl is sent as a parameter for an API call
		* [Uploading Multiple Images](./api-guide/#_16)
		* [Executing Image Operations](./api-guide/#_37)

<a id="november-30-2017-bug-fixes"></a>
#### Bug Fixes 
 * [Console] Fixed bugs in which an invalid subfolder path was created while uploading a folder including compression files 

<a id="november-23-2017"></a>
### November 23, 2017 { #november-23-2017 }
<a id="november-23-2017-feature-updates"></a>
#### Feature Updates 
* [Added Features of Image Processing](./api-guide/#_25)
	* Added grid-split as part of splitting images
	* Added the watermark feature
* [Console] [Added Image Processing Option](./console-guide/#_10)
	* The option was available only for resizing but now is configurable as a common option  
		* Quality, image format, callback URL for result, whether to maintain meta data, whether to rotate based on orientation data  
	* Changed the default value for the option of maintaining GIF animation: Changed from Not Maintain to Maintain  
* [Console] [Grouping by image processing features](./console-guide/#_10)
	* Group 1 for Basic Processing: Resize, Gray, or Rectangle Crop
	* Group 2 for Split Processing: Slice Crop (width, height, grid)
	* Group 3 for Composite Processing : Circle Crop
	* Images are to be processed in the group sequence 
* [Console] [Changed Process of Product Closure](./console-guide/#_8)
	* Unable to close when there is a file left when stopping the use of the service
	* Added the feature to delete the whole files, and service use can be stopped after all files are deleted  

<a id="may-25-2017"></a>
### May 25, 2017 { #may-25-2017 }
<a id="may-25-2017-bug-fixes"></a>
#### Bug Fixes
* Fixed an error of parsing image meta information 

<a id="april-20-2017"></a>
### April 20, 2017 { #april-20-2017 }
<a id="april-20-2017-feature-updates"></a>
#### Feature Updates 
* [Added Thumbnail Resizing Method](./console-guide/#_10) 
    * Changed size to meet the width and height of option 
    * Changed standard size of the width of option
    * Changed standard size of the height of option 
* [Added the method of cropping](./console-guide/#_10)
    * Added Slice Crop 
* [Console] [Changed the option of maintaining Gif animation as global configuration](./console-guide/#_10)

<a id="april-20-2017-bug-fixes"></a>
#### Bug Fixes 
* Modified not to create a folder which includes a tilde

<a id="march-23-2017"></a>
### March 23, 2017 { #march-23-2017 }
<a id="march-23-2017-bug-fixes"></a>
#### Bug Fixes
* [Console] Fixed an issue in which Korean files uploaded on macOS were unable to be searched 
