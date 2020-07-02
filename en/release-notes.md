## Content Delivery > Image > Release Notes

### February 22, 2018
#### Feature Updates
* [Console] '섬네일 옵션 관리' 화면의 접근 방식을 '폴더 및 이미지 파일 관리' 화면 내부의 버튼에서 상위 메뉴로 변경 Changed the access of 'Thumbnail Option Management' from a button within the 'Folder and Image File Management' to top of the menu  
	* 폴더 및 이미지 파일 관리는 'File View' 메뉴에서 접근 가능 Folder and image file management is accessible from 'File View'
	* 섬네일 옵션 관리는 'Operation Setting' 메뉴에서 접근 가능 Thumbnail option management is accessible from 'Operation Setting'
* [Console] [Folder and Image File Management 폴더 및 이미지 파일 관리](./console-guide/#_1)
	* Added the feature of moving folder paths on the existing page, and added the folder tree feature 기존 화면에서 폴더 경로 이동 기능, 폴더 트리 기능 추가
	* 폴더 목록에 이전 폴더로 이동 기능 추가 Added the feature of moving to a previous folder on the folder list

#### Bug Fixes 
* [API] operation-exec API 요청 시 파일(또는 오퍼레이션)이 잘못된 경우 작업과 무관하게 성공 응답 처리하는 버그 수정 Fixed bugs processing success with no regards to task, even when file (or operation) is incorrect for the operation-exec API request 
	* 작업 내용(queues)이 없는 경우 실패 응답으로 처리 Process as failed response when task (queues) is unavailable 
	* 작업 내용(queues) 개수가 요청 수와 맞지 않은 경우 부분 성공 응답으로 처리 Process as partial success when task (queues) count is not consistent with request count 

### December 21, 2017 
#### Feature Updates
* [API] 처리 결과 Callback에 덮어쓰기 되었는지 여부 표시 추가 Added the display whether processing result has been overwritten to callback 
	* [Uploading Multiple Images 다중 이미지 업로드](./api-guide/#_16)
	* [Executing Image Operations 이미지 오퍼레이션 실행](./api-guide/#_37)
* [Console] Changed UI design of the screen 화면 UI 디자인 변경

### November 30, 2017
#### More Features 
* [API] 처리 결과 Callback 기능 추가 Added callback for processing results 
	* API 호출 시 callbackUrl을 파라미터로 전달하면 처리 결과를 callbackUrl로 전송해주는 기능 추가 Added the feature of sending processing result to callbackUrl when it is sent to parameter for an API call
		* [Uploading Multiple Images](./api-guide/#_16)
		* [Executing Image Operations](./api-guide/#_37)

#### Bug Fixes 
 * [Console] 압축 파일이 포함된 폴더 업로드 시 하위 폴더 경로가 잘못 생성되던 버그 수정 Fixed bugs in which an invalid path of lower folder was created while uploading a folder including compression files 

### November 23, 2017
#### Feature Updates 
* [Added Features of Image Processing 이미지 처리 기능 추가](./api-guide/#_25)
	* 이미지 분할 기능에 격자 분할 추가 Added grid-split as part of splitting images
	* 워터마크 기능 추가 Added the watermark feature
* [Console] [Added image processing option 이미지 처리 옵선 추가](./console-guide/#_10)
	* 기존 Resize에서만 설정 가능했던 옵션을 공통 옵션으로 설정 가능하도록 수정 The option was available only for resizing but now is configurable as a common option  
		* Quality, image format, callback URL for result, whether to maintain meta data, whether to rotate based on orientation data  품질, 이미지 포맷, 결과 콜백 URL, 메타정보 유지 여부, Orientation 정보를 기준으로 회전 여부
	* Changed default value for the option of maintaining GIF animation 애니메이션 유지 옵션의 default 값 변경 : Changed from Not Maintain to Maintain 유지하지 않음에서 유지 함으로 변경 
* [Console] [To be grouped by image processing features 이미지 처리 기능에 따라 Grouping](./console-guide/#_10)
	* Group 1 for Basic Processing기본 처리 : Resize, Gray, or Rectangle Crop
	* Group 2 for Split Processing 분할 처리 : Slice Crop (width, heigh, grid 가로, 세로, 격자)
	* Group 3 for Composite Processing 합성 처리 : Circle Crop
	* Images are to be processed in the group sequence 이미지 처리는 Group 순서대로 처리 됨
* [Console] [Changed Process of Product Closure 상품 종료 프로세스 변경](./console-guide/#_8)
	* Unable to close when there is a file left after service is closed 상품 이용 종료 시 남아있는 파일이 있는 경우 이용 종료 불가능
	* 전체 파일 삭제 기능이 추가되었고, 전체 삭제 후 상품 이용 종료 가능 With the feature of deleting the whole file added, service can be closed after all is deleted  

### May 25, 2017
#### Bug Fixes
* Image Meta 정보 파싱 에러 수정 Fixed an error of parsing image meta information 

### April 20, 2017 
#### Feature Updates 
* [Added Thumbnail Resizing Method 썸네일 크기조절 방식 추가](./console-guide/#_10) 
    * Option의 가로 세로에 맞게 Size 변경 Changed size to meet the width and height of option 
    * Option의 가로 기준 Size 변경 Changed standard size of the width of option
    * Option의 세로 기준 Size 변경 Changed standard size of the height of option 
* [Added the method of cropping 크롭 방식 추가](./console-guide/#_10)
    * Added Slice Crop 추가
* [Console] [Changed the option of maintaining Gif animation as global configuration 애니메이션 유지 옵션 글로벌 설정으로 변경](./console-guide/#_10)

#### Bug Fixes 
* 물결(~) 문자가 포함된 폴더가 생성되지 않도록 수정 Modified not to create a folder which includes a tilde

### March 23, 2017
#### Bug Fixes
* [Console] macOS에서 업로드한 한글 파일 검색 불가 이슈 수정 Fixed an issue in which Korean files uloaded on macOS were unable to be searched 
