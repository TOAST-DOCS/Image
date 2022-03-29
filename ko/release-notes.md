## Content Delivery > Image > Release Notes

### February 25, 2020
#### Feature Changes 
* Added the feature of moving to the previous folder on the list 


### February 22, 2018
#### Feature Changes
* [Console] Changed the method of access to 'Thumbnail Option Management' page from a button on the screen to the upper menu  
	* Access to Folder and Image File Management is available from the 'File View' menu
	* Access to Thumbnail Option Management is available from the 'Operation Setting' menu 
* [Console] [Folder and Image File Management](./console-guide/#_1)
	* Added the feature of moving folder path from the previous page and the folder tree feature 
	* Added the feature of moving to the previous folder on the folder list 

#### Bug Fixes
* [API] Fixed a bug for the operation-exec API request, in which invalid file (or operation) is processed as successful, regardless of the operation
	* Process as failed response when there is no queues
	* Process as partially successful response when the queue count is not same as request count 

### December 21, 2017
#### Feature Updates
* [API] Added the display of whether processing result has been overwritten to callback 
	* [Uploading Multiple Images](./api-guide/#_16)
	* [Executing Image Operations](./api-guide/#_37)
* [Console] Changed UI design on the screen 

### November 30, 2017
#### More Features
* [API] Added the callback feature for processing result 
	* On an API call, the result of callbackUrl sent to parameter is delivered to callbackUrl
		* [Uploading Multiple Images](./api-guide/#_16)
		* [Executing Image Operations](./api-guide/#_37)

#### Bug Fixes
 * [Console] Fixed bugs in which uploading folders including compression files results in invalid lower-folder paths 

### November 23, 2017
#### Feature Updates
* [Added Image Processing](./api-guide/#_25)
	* Added grid segmentation as part of image segmentation
	* Added the watermarking feature 
* [Console] [Added Image Processing Options](./console-guide/#_10)
	* Modified to allow options that were previously configurable only for resizing to be commonly applied 
		* Decide to rotate by quality, image format, result callback URL, whether to maintain metadata, or by orientation   
	* Changed the default for maintaining GIF animation: Changed from Not Maintain to Maintain 
* [Console] [Grouped by Image Processing](./console-guide/#_10)
	* Default Processing for Group 1: Resize, Gray, Rectangle Crop
	* Segmented Processing for Group 2: Slice Crop (Width, length, or grid)
	* Compound Processing for Group 3: Circle Crop
	* Images are processed in the group order
* [Console] [Changed Product Closing Process](./console-guide/#_8)
	* Unavailable to close a product, if there is any files left 
	* Now available to delete all files, and a product can be closed after all is deleted 

### May 25, 2017
#### Bug Fixes
* Fixed the error of parsing image meta information 

### April 20, 2017 
#### Feature Updates
* [Added Thumbnail Sizing Methods](./console-guide/#_10)
    * Sizing for the length and width of option 
    * Sizing for the width of option
    * Sizing for the length of option 
* [Added Cropping Method](./console-guide/#_10)
    * Added slice crops 
* [Console] [Changed the option of maintaining Gif animation to be globally applied](./console-guide/#_10)

#### Bug Fixes
* Modified not to create a folder including a tilde (~)

### March 23, 2017 
#### Bug Fixes
* [Console] Fixed an issue in which uploaded Korean files cannot be searched on macOS 
