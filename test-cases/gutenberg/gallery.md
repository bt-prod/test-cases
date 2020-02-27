
# Gallery Block - Test Cases

#### **Precondition**

A site with premium or business plan

--------------------------------------------------------------------------------

##### TC001

### Close/Re-open post with an ongoing image upload

-   Add a gallery block and insert images from device
-   While there’s an ongoing upload, close the post with publishing changes
-   Verify that you see the upload progress in post summary
![Progress](../resources/upload-progress-posts-list.png)
-   Reopen the post while upload is ongoing
-   Verify you still see the upload progress in the gallery block

--------------------------------------------------------------------------------

##### TC002

### Close post with an ongoing image upload

-   Add a gallery block and insert images from device
-   While there’s an ongoing upload, close the post with publishing changes
-   Verify that you see the upload progress in post summary
![Progress](../resources/upload-progress-posts-list.png)
-   Wait until upload finishes
-   Re-open the post
-   Verify that Gallery block shows the uploaded images


--------------------------------------------------------------------------------

##### TC003

### Add caption to gallery

-   Add a Gallery block
-   Set a caption to your gallery

![Gallery Caption](../resources/gallery-caption-3.png)
-   Add some styles to your caption:
    - Bold
    - Italic
    - Underline
    - Expect all to work correctly

![Gallery Caption Styles](../resources/gallery-caption-4.png)

-   Save the post
-   Open it and expect to see the captions with their styles


--------------------------------------------------------------------------------

##### TC004

### Add caption to gallery images

-   Add a Gallery block
-   Add some images to your gallery
-   Set some captions to your images by tapping on each image

![Gallery Image Caption](../resources/gallery-caption-1.png)
-   Add some styles to your captions:
    - Bold
    - Italic
    - Break line
    - Expect all to work correctly

![Gallery Image Caption Styles](../resources/gallery-caption-2.png)

-   Save the post
-   Open it and expect to see the captions with their styles

--------------------------------------------------------------------------------

##### TC005

### Choose from device (stay in editor) - Successful upload

Gallery block should allow uploading multiple images from the device.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from device" option
* Select multiple images from the device and confirm the selection

**Expected behavior:**

* Gallery should show all images being uploaded as dimmed
* Progress bars should be displayed indicating the upload progress
* After each image upload has completed:
  * Image should not be dim
  * Image url scheme should be `https://` (not `file:///`) in HTML mode

--------------------------------------------------------------------------------

##### TC006

### Choose from device (stay in editor) - Failed upload

Gallery block should allow retrying failed uploads

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from device" option
* Select multiple images from the device and confirm the selection
* While images are uploading, turn on airplane mode

**Expected behavior:**

* Images should indicate failed upload state
* Tapping a failed image should provide an option to retry the upload(s)

--------------------------------------------------------------------------------

##### TC007

### Choose from device (leave the editor) - Successful upload

Gallery block should allow uploading multiple images after the editor is closed.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from device" option
* Select multiple images from the device and confirm the selection
* While image are uploading, leave the editor
* Verify that you see the upload progress in post summary:
  * <img src="../resources/upload-progress-posts-list.png" width="360" valign="middle">
* Wait for uploads to complete while in the post list
* Re-open the post with the gallery block

**Expected behavior:**

* Gallery should show all completed uploads
* The images' url schemes should be `https://` (not `file:///`) in HTML mode

--------------------------------------------------------------------------------

##### TC008

### Choose from device (close and re-open the editor with ongoing uploads)

Gallery block should continue normally if the editor is closed and re-opened with ongoing uploads.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from device" option
* Select multiple images from the device and confirm the selection
* While image are uploading, leave the editor
* Verify that you see the upload progress in post summary:
  * <img src="../resources/upload-progress-posts-list.png" width="360" valign="middle">
* Re-open the post with the gallery block before uploads complete

**Expected behavior:**

* Gallery should show all images being uploaded as dimmed
* Progress bars should be displayed indicating the upload progress
* After each image upload has completed:
  * Image should not be dim
  * Image url scheme should be `https://` (not `file:///`) in HTML mode

--------------------------------------------------------------------------------

##### TC009

### Take a photo

Gallery block should allow uploading images from the camera.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Take a photo" option
* Take a photo and confirm the selection

**Expected behavior:**

* Gallery should show the image being uploaded as dimmed
* A progress bar should be displayed indicating the upload progress
* After the image upload has completed:
  * Image should not be dim
  * Image url scheme should be `https://` (not `file:///`) in HTML mode

--------------------------------------------------------------------------------

##### TC010

### Choose from the free photo library

Gallery block should allow uploading images from the free photo library.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from the free photo library" option
* Select multiple images from the device and confirm the selection

**Expected behavior:**

* Gallery should show all images being uploaded as dimmed
* Progress bars should be displayed indicating the upload progress
* After each image upload has completed:
  * Image should not be dim
  * Image url scheme should be `https://` (not `file:///`) in HTML mode

--------------------------------------------------------------------------------

##### TC011

### Choose from device (stay in editor) - Cancel upload

Gallery block should allow canceling image uploads.

**Steps:**

* Add a gallery block and tap "Add Media"
* Select "Choose from device" option
* Select an image from the device and confirm the selection
* While the image is uploading, tap the image
<img src="../resources/gallery-upload-in-progress.jpg" width="360" valign="middle">

**Expected behavior:**

* A prompt for "Stop uploading" should be shown.
* Confiriming should cancel the upload if the upload didn't finish.
* Declining should allow the upload to continue.  

--------------------------------------------------------------------------------

##### TC012

### Rearrange images in Gallery

Gallery block should allow images to be rearranged in the gallery.

**Steps:**

* Add a gallery block and tap "Add Media"
* Add serveral images through the various options
* Select an image and change it's position.
* Test with:
    * Adding even and uneven image counts and rearranging the last image
    * Leaving the editor and coming back in
    * Validate order is reflected on the Web after saving
