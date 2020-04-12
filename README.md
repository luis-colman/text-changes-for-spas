# Text Changes for SPAs Extension

This Optimizely extension allows to apply plain-text changes on SPAs where the below scenarios occur: 

that re-inject content on the chosen element(s) more than twice during pageload and/or for SPAs where elements get de-attached from the SPA once changed via **innerHTML** (meaning elements don't respond to updates triggered natively by the SPA after they have been modified by Optimizely using **innerHTML**).

1) In some situations SPAs may inject and re-inject content more than twice during pageload. This may result in Optimizely not blocking/re-applying changes indefinitely during pageload (to prevent the browser from overheating) allowing original content to persist/remain and not displaying the variation change

2) In some SPAs elements don't respond to updates triggered natively by the SPA after they have been modified by Optimizely using **innerHTML** even if the experiment/Page is deactivated.

This extension applies changes in a different manner than the Visual Editor, allowing to apply changes even in the cases mentioned above.

(*Note*: this extension is meant to allow plain text changes only. It *does not* cover further HTML changes).


## Install the "Text Changes for SPAs" Extension

1. In your Optimizely account, navigate to "**Implementation > Extensions**".

2. Click Create New... and select "**Using JSON**".

![Image description](link-to-image)

3. Copy the content of the JSON of this repository.

4. Paste the code in the "**Create Extension From JSON**" field and click "**Create Extension**".

![Image description](link-to-image)

5. If you want to see how the extension is built, simply click the extension name "**Text Changes for SPAs**". In the Editable Fields panel, you can see and change the current fields the extension contains (selector and textbox). Here you can also see the JavaScript code the extension uses by clicking on "Apply JS", where can also make changes if desired.

6. Before you can use this extension, you need to enable it. After uploading the JSON file the extension will in "**draft**" state. To enable the extension, navigate to "**Implementation > Extensions**" and click the **...** icon for the "**Text Changes for SPAs**" extension and select "**Enable**".

![Image description](link-to-image)

7. To start using your extension in experiments, simply go into the variation where you want to use this extension and click "**Create**" (as you normally do for any other visual change).

8. Under "**Create Options**", select "**Text Changes for SPAs**".

9. Select the element to change. (Make sure you select the exact element that contains the text that you want to change and not parent elements higher in the HTML structure).

10. Enter the desired text in the textbox below the selector field and save your changes


**-- END --**
