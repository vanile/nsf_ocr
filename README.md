# Dependencies
* Firefox
* BeautifulSoup
* selenium (with [geckodriver.exe](https://github.com/mozilla/geckodriver/releases) in PATH)
* OpenCV (using 4.5.1) with GUI
* youtube-dl
* ffmpeg
* pytesseract — must be with 14MB [eng.traineddata](https://github.com/tesseract-ocr/tessdata_best/blob/master/eng.traineddata) (replace the 4MB one)

# TODO List
* Account for missing checklist
  * Add log to keep track of previous detections and calculate time since
* Use line detection instead of contours to detect the box is on screen
* Verify initial crop and min/max area values based on real data
* Add more comprehensive crop for entire checklist (can use ```cv2.vconcat()```)
* Filter to check for duplicate crops (use ```compareHist()``` with thresh2?)
  * Avoids running through entire thing every time
* Split checklist using ```cv2.reduce``` to read every line separately
  * Can get sequence number
* Figure out some way to share the info openly