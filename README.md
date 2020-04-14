# Text Changes for SPAs Extension

This Optimizely extension allows to apply plain-text changes on SPAs where the below scenarios occur: 

that re-inject content on the chosen element(s) more than twice during pageload and/or for SPAs where elements get de-attached from the SPA once changed via **_innerHTML_** (meaning elements don't respond to updates triggered natively by the SPA after they have been modified by Optimizely using **_innerHTML_**).

1) In some situations SPAs may inject and re-inject content more than twice during pageload. This may result in Optimizely not blocking/re-applying changes indefinitely during pageload (to prevent the browser from overheating) allowing original content to persist/remain and not displaying the variation change

2) In some SPAs elements don't respond to updates triggered natively by the SPA after they have been modified using **_innerHTML_** even if the experiment/Page is deactivated. (The feature "_**Element Change**_" from the Visual Editor uses **_innerHTML_**).<br/>_(For more info regarding this phenomenon visit the link below:<br/>https://stackoverflow.com/questions/39960933/manual-innerhtml-modification-on-dom-halts-reactjs-listeners)_

This extension applies changes in a different manner than the Visual Editor, allowing to apply changes even in the cases mentioned above.

(**_*Note_**: this extension is meant to allow plain-text changes only. It **_does not_** cover further HTML changes).


## Install the "Text Changes for SPAs" Extension

1. In your Optimizely account, navigate to "**_Implementation > Extensions_**".

2. Click Create New... and select "**_Using JSON_**".

![Image description](https://github.com/luis-colman/text-changes-for-spas/blob/master/images/create_extension.png)

3. Copy the content of the JSON of the repository [Text Changes for SPAs](https://github.com/luis-colman/text-changes-for-spas/blob/master/config.json).

4. Paste the code in the "**_Create Extension From JSON_**" field and click "**_Create Extension_**".

![Image description](https://github.com/luis-colman/text-changes-for-spas/blob/master/images/create_extension_from_json.png)

5. If you want to see how the extension is built, simply click the extension name "**_Text Changes for SPAs_**". In the Editable Fields panel, you can see and change the current fields the extension contains (selector and textbox). Here you can also see the JavaScript code the extension uses by clicking on "**_Apply JS_**", where can also make changes if desired.

6. Before you can use this extension, you need to enable it. After uploading the JSON file the extension will in "**_draft_**" state. To enable the extension, navigate to "**_Implementation > Extensions_**" and click the **_..._** icon for the "**_Text Changes for SPAs**_" extension and select "**_Enable_**".

![Image description](https://github.com/luis-colman/text-changes-for-spas/blob/master/images/enable_extension.png)

7. To start using your extension in experiments, simply go into the variation where you want to use this extension and click "**_Create_**" (as you normally do for any other visual change).

8. Under "**_Create Options_**", select "**_Text Changes for SPAs_**".

9. Select the element to change. (Make sure you select the exact element that contains the text that you want to change and not parent elements higher in the HTML structure).

10. Enter the desired text in the textbox below the selector field and save your changes


**_-- END --_**
