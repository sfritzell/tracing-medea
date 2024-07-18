# Documentation for GitHub  - simplified

**Remember to commit your changes and leave a description of your changes in your commit message. :)**

## Adding a new play page

- To add a new play page start at the repository home page. Navigate to the pages folder and create a new file. In the file name, use the convention of **title-authorlastname.md**
- Don’t use capital letters or spaces. 
For example, to create the page for Mojada by Luis Alfaro I went to the pages folder and created a new file named **mojada-alfaro.md**
By the Bog of Cats by Marina Carr would be: **bythebogofcats-carr.md**

## Adding new content to a play page

- When adding content to the page, follow the template play page (sample-play-page.md). **Replace the headings while leaving the code and YAML header in place.** The yaml header is encased inside the three hash marks
- Go to the YAML header and replace “Sample Play Page” with the name of the play. Leave the layout the same.

- Next, add a line underneath layout. In that line write <font color="green">**permalink: filename.html**</font>
- When you’re finished, it should look like this. 

This is the link to this play page.


## Adding images and embedded video to play page
- **To add single images** to the page you will need to use the following syntax: 
{% include feature/image.html objectid="image_url" width="75" alt="Alt_text" caption="caption"%}
- For **online images** the image url can be found by right clicking on the image you want and selecting “copy image address” from the menu.

- Replace image_url with the URL you copied, but keep the quotes
- Replace the Alt_text with the alt text you have written
- Remember for both linked and embedded images to **write meaningful alt text that describes the image in the context of the page**.
- Replace the “caption” with the caption of the image, using the standards laid out below.
- To add **local images**, they must first be uploaded to the **img** folder which is inside the **assets** folder. 
- After they are uploaded, to link to the image in the Markdown for the play page, use the same syntax as with online images. 
This time, the image url is the file path within Github, called a relative link. So if I want to input the home page banner into a play page I will enter in the file path to the image
/assets/img/homepage-banner.jpg
So the entire command would look like this: {% include feature/image.html objectid="/assets/img/homepage-banner.jpg" width="75" alt="A collage of adaptations of Medea" caption="Homepage Banner"%}
(The banner may not be the best to do captions on, but this is just to present the syntax.)
- Commit your changes and wait for them to appear. 

**Adding embedded YouTube videos**
To embed a Youtube Video into a play page the following syntax can be copy-pasted with two modifications. 
- {% include feature/video.html objectid="youtube_url" width="50" caption="youtube caption" %}
- Replace youtube_url with the link to your video, but leave the quotes. The link can be found by either right clicking on the video itself and selecting “copy video url” or clicking share and copying the url from there. (Don’t use the embed option, it just breaks things!)
 

- Then change the caption, following the caption guide below.
- Be patient after you commit the changes.  This can take a while.
### Multiple Images (side by side)
To **add multiple images**, you need need the following syntax template 
- {% include feature/image.html objectid="firstimage_url;secondimage_url" caption="caption1;caption2" link="linktosource1;linktosource2" alt="alt-text1;alt-2" %}
- Replace the image urls with the new ones, preserving the quotes and **semicolons**. 
- Replace the captions in the same manner
The link section allows the image itself to link to the original source, so if I took a picture off the New York Times, clicking on the image would take me to the New York Times website. 
I think you can do this on the single images as well, using similar syntax, but I haven’t tried it yet.
- Replace the links as needed (if the images are local and you can’t find the source try a reverse google image search) 
- Replace the alt text placeholders with the correct alt text, following the style guidelines. 
- Commit. Wait. 
You can add more than two images by simply putting a semicolon and the correct information after the second url/alt/caption/link.  
## Adding link to the new play page
- To **link the new play page** to the regional page or anywhere else you use similar syntax to linking in images. 
[play title](filename)
- Mojada’s link on the Americas’ page looks like this: 

- This gives you a hyperlink that appears like this: 

- By the Bog of Cats would be linked like this: 
- [By the Bog of Cats](bythebogofcats-carr)


## Adding captions to images and videos
The captions for images and videos should not be the same as the alt text (for images) or the title of the video.  A succinct statement, connected to the production, suffices.  For example
- Scene from Alfaro’s Mojada production, Los Angeles, 2012
- Interview of Alfaro, with name of interviewer

## Adding new play to csv file so that it shows up on map

To add a new play to the map, enter information in the play-demo-metadata.csv, housed in _data

### Required fields relevant to the map pop-up are
- objectID - format is play###.  Determine what the next number in sequence is
- filename - format:  full URL of image source
- title - format:  text, name of the play
- creator - format:  text, name of the playwright
- date - format:  numeric, date of publication or first performance
- description - format:  text, very short description of key point about play
- location - format:  text, region, e.g. Europe, America, Australia
- city-country - format:  text, name of city and country (for US, this often becomes city and state)
- latitude - format:  text, number of latitude, retrieved from Open Street Map
- longitude - format:  text, number of longitude, retrieved from Open Street Map
- On the pop up, we have a subject line.  Its content is determined by indicating TRUE for any and all identities you want to display on the popup.  These start at column Q

For more details see
https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/

### Optional fields include
**type:**
An object’s type distinguishes between types of image, sound, text, etc. using a one- or two-value input. At minimum, the input should contain a value chosen from the DCMI Type Vocabulary. If using a second value, the second value does not need to relate to a controlled vocabulary, but should give further specification of the object type. The two values in a pair should be separated by a semicolon (;). See examples below.
Example value: Image;StillImage, Image;MovingImage, Text, Sound
**language:**
This field indicates the language associated with the object. Recommended best practice is to use a controlled vocabulary such as the ISO 639-2 Codes for the Representation of Names and Languages to designate language tags.
Example value: eng, fra, deu
**rights:**
The rights field should include a free-text rights statement describing information about rights held in and over the object.
Example value: Educational use includes non-commercial use of text and images in materials for teaching and research purposes. Digital reproduction rights granted by the University of Idaho Library. For other uses beyond free use, please contact University of Idaho Library Special Collections and Archives Department.
**rightsstatement:**
This field is a standardized rights statement, designated in the form of a URI. It should be presented as a creativecommons.org URI or a rightsstatements.org URI.
Example value: http://rightsstatements.org/vocab/NoC-US/1.0/

## Accessibility
The site aims to adhere to WCAG AA standards, with a focus on 
**Text:**  
Use headings and sub headings consistently.
Limit use of italics and other specialized characters to, for example titles (italics) or hyperlinks (underline)
Use widely available font families with at least 12 size font and appropriate spacing
Use white space
**Links:** 
Ensure that the text used for linking is meaningful.  Avoid such link language as Click here
Set links visually apart from the text through 2 ways, usually color (e.g. blue) and underline.
**Images:**  
Resize images to ensure faster load time.  
Create meaningful succinct alt text for all images to add meaning to the content and avoid redundancy.  Exception:  decorative images should be marked as such
Ensure that markers on maps also have alt text
If possible, include images that appeal to a diverse audience
**Videos:**  
Ensure that close captions are enabled
Ensure that captions are accurate
**Colors:**  
Check that the color contrast is clear.
Check for a color scheme that is not a hurdle for colorblind.

Why is this important?
It is the right thing to do - making our materials available and accessible to as many users as possible is important.  We do not want to turn people away because they cannot see or hear the content of this site.
It is the law:  “Title II extends the prohibition on discrimination established by section 504 of the Rehabilitation Act of 1973, as amended, 29 U.S.C. 794, to all activities of State and local governments regardless of whether these entities receive Federal financial assistance.”  Educational institutions, no matter what type, receive state and federal funding so their websites need to be ADA compliant.  This is a personally hosted site, but we still want to ensure that the materials comply for the times we will use this in teaching situations.


