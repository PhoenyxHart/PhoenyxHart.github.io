# How to Add a Flannel to the Website
## Creating a Flannel Design
First, create a flannel design using [this website](https://doodlenerd.com/web-tool/plaid-designer). Save it as an image by right-clicking on the flannel and selecting "Save Image As..." (the exact syntax may differ depending on browser, but it should be relatively similar).

![Save Flannel](/images/tutorial/01-Save_Flannel.png)

Name the file something descriptive (such as with color or theme). For an example, I've named this one "red-and-black" for obvious reasons.

## Uploading to the Repository
On your repository page, navigate to `images`, then `flannels` by clicking on the folders.

![Goto Images](/images/tutorial/02-Goto_Images.png)
![Goto Flannels](/images/tutorial/03-Goto_Flannels.png)

Once in the flannels subfolder, click on the "Add file" dropdown, then on "Upload files" to open the upload prompt.

![Click Upload](/images/tutorial/04-Click_Upload.png)

You can either drag and drop the file, or select it in the file prompt ("choose your files"). This should be the design you just saved. The image name should now be visible in the center of the page.

![Upload Prompt](/images/tutorial/05-Upload_Prompt.png)

Once this is added, you can click on "Commit changes" to submit the file upload. If you navigate back to the `flannels` folder, you'll see the file you just uploaded.

![Successful Upload](/images/tutorial/06-Successful_Upload.png)

## Editing the HTML
Although the image is uploaded, there are a few more things that need to be done for the flannel to be displayed on the website. Luckily, these changes are relatively simple. First, ensure that you're back on the [repository homepage](https://github.com/PhoenyxHart/PhoenyxHart.github.io). Click on `index.html` to open the code for the website. I'm sure it'll look confusing for somebody unfamiliar with HTML, but I'll guide you through the process. On this page, click on the pencil icon near the top right (hovering over it should read "Edit this file").

![HTML Code Display](/images/tutorial/07-HTML_Code_Display.png)

The area you'll want to edit is near the bottom, within the following section:
```
<div class="flex-container">

</div>
```
This will be blank the first time you edit it, but will have elements inside it as you add more flannels to your site. In this section, enter the following code (you can copy and paste if it's easier):
```
<div class="plaid plaid-your-color"></div>
```
Replace "your-color" with whatever you named your design. As an example, here's what the code looks like after I add the red and black flannel:

![Edited HTML](/images/tutorial/08-Edited_HTML.png)

As you add more, make sure they're placed on separate lines. This will make the code appear neat and organized. Additionally, the order of these elements will determine the order they appear on the website. For example, a section that looks like this will have the listed flannels appear in rainbow order:
```
<div class="flex-container">
  <div class="plaid plaid-red"></div>
  <div class="plaid plaid-orange"></div>
  <div class="plaid plaid-yellow"></div>
  <div class="plaid plaid-green"></div>
  <div class="plaid plaid-blue"></div>
  <div class="plaid plaid-indigo"></div>
  <div class="plaid plaid-violet"></div>
</div>
```
After you've added your line, click on the "Commit changes..." button in the top-right corner.

![Commit HTML](/images/tutorial/09-Commit_HTML.png)

GitHub's Copilot (basically their AI) will auto-generate a commit message, which you can keep or remove. Click on "Commit changes" when you're done.

## Editing the CSS
Don't worry, you're almost done! There's one more file left to edit. This time, navigate to the `styles` folder and open the `flannels.css` file for editing like you did with `index.html`. Within this file is a section header that looks like this:
```
/* Owned Flannels */
```
Add this section of code, once again replacing "your-color" with your design's name:
```
.plaid-your-color {
  background-image: url("../images/flannels/your-color.png");
}
```
Note that there are two instances of "your-color" in this section. The first iteration is linked to the HTML file (the first text file you edited), and the second is linked to the image's filename. Here's my sample edit for reference:

![Edited CSS](/images/tutorial/10-Edited_CSS.png)

Repeat the upload process by clicking on "Commit changes..." to open the commit prompt, then by clicking on "Commit changes" to lock in your edits.

![Commit CSS](/images/tutorial/11-Commit_CSS.png)

The changes will take some time to update on the website. You'll see this section in the right pane of the repository's homepage, which indicates that it's loading.

![Awaiting Deployment](/images/tutorial/12-Awaiting_Deployment.png)

And it'll turn green when it's done (you'll need to refresh the page).

![Completed Deployment](/images/tutorial/13-Completed_Deployment.png)

## Final Result
Assuming you completed the previous steps correctly, you will now be able to find a new flannel design on [your website](https://phoenyxhart.github.io/). If it doesn't show up, check the text files again to make sure no errors were made.

![Final Result](/images/tutorial/14-Final_Result.png)

Please note that any changes I made during this tutorial have been reverted, and let me know if you have any questions or there's anything else you'd like me to touch upon in the tutorial.