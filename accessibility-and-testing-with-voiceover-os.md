---
layout: page
title: Accessibility and Testing with VoiceOver OS (Mac)
---

VoiceOver is the defualt screen reader on **Mac** desktop devices. 

It's recommended to use the **latest OS** that you have access to. Test with **Safari**.

**Not sure how to use VoiceOver**? Watch [Screen Reader Basics: VoiceOver -- A11ycasts](https://www.youtube.com/watch?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&params=OAFIAVgF&v=5R-6WvAihms&mode=NORMAL&app=desktop) and complete the on device tutorial, go to 'System Preferences', then 'Accessibility', then 'VoiceOver'. Then 'Open VoiceOver Training...'. 

## What should I test?
0. Test the feature by reading every element.
1. Test the feature by reading headers.
2. Test the feature by tabbing through links.
1. Test the feature by reading landmarks.
2. Test the feature for use of ARIA.

## Testing steps

The accessibility acceptance criteria can be used for additional manual testing steps on device, this is written by the [Business Analyst](accessibility-news-and-business-analysts) and part of their checklist.

### General 

0. Open **Safari**.
1. Go to the **testing url**.
2. **Turn VoiceOver on**, with shortcut keys 'CMD + F5'. 
3. Navigate to the last element in the feature before the feature to be tested, this will ensure you don't miss any visually hidden/off screen text at the beginning of the feature. Then use '[VO](#vo) + Right arrow' to read **through each element** in the feature (if you need to go back, 'VO + Left arrow'). 
- Is all the content read out and make sense? 
- Is the content read out in a logical order following the visual order? 
- Is any content read out more than once?
- Is any visually hidden/off screen text read out, such as for icons?
- Do images have alt text?
- Are there any empty key presses? e.g. You press the keys and you don't hear anything. If so, this maybe a bug.
4. Open the 'Rotor' menu ('VO + U'), then use the 'Right/Left arrow' keys to navigate to the list of '**Headings**', then use the 'Down/Up arrow' keys to read through all the headers in the feature.
- Are all headings read out and in a logical order? 
- Not sure what headings the feature should read out? You can use a desktop browser tool such as the [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) add-on for Chrome or Firefox. (Under ‘Information’ select ‘View Document Outline’ - This will show you the heading structure for the selected page.) 
5. Navigate to the end of the feature before the feature to be tested, then use the tab key to read out all '**Links**' in the feature. Are all links read out? Is any content that is not a link read out?
6. Open the 'Rotor' menu ('VO + U'), then use the 'Right/Left arrow' keys to navigate to the list of '**Landmarks**', then use the 'Down/Up arrow' keys to read through all the landmarks in the feature.
- Are all landmarks read out? 
- Not sure what landmarks are? See [W3C ARIA Landmarks Examples](https://w3c.github.io/aria-practices/examples/landmarks/index.html). Not sure what landmarks the feature should read out? See the accessibility acceptance criteria.
7. **ARIA** can be used simply to add landmarks/regions/labels to a page or more advanced usage can help with dynmaic content such as page updates or advanced user interface controls such as tabs. Use 'VO + Right arrow' to move through the feature checking that all ARIA is being acknowledge/read out correctly. See the accessibility acceptance criteria for details on what should be read out. Still not sure what should be acknowledged/read out? Ask an Accessiblity Champion.

### Tables

When testing a table use all of the [table keyboard shortcuts](#table-keyboard-shortcuts).

Note, **if numbers are not reading out correctly**, you may need to change the VoiceOver verbosity setting, go to 'System Preferences', then 'Accessibility', then 'VoiceOver', then 'Open VoiceOver Utility', then 'Verbosity', then 'Text', and toggle 'Read numbers as digits/words'.

0. Open **Safari**.
1. Go to the **testing url**.
2. **Turn VoiceOver on**, with shortcut keys 'CMD + F5'. 
3. Navigate to the last visible element before the table to be tested, this will ensure you don't miss any visually hidden/off screen text at the beginning of the table. Then **use all the [table keyboard shortcuts](#table-keyboard-shortcuts) to read through each element** in the table. 
- Are table row and column headers read out for each table cell?
- Is all the content read out and make sense? 
- Is the content read out in a logical order following the visual order? 
- Is any content read out more than once?
- Is any visually hidden/off screen text read out, such as for icons?
- Are there any empty key presses? e.g. You press the keys and you don't hear anything. If so, this maybe a bug.
4. Open the 'Rotor' menu ('VO + U'), then use the 'Right/Left arrow' keys to navigate to the list of 'Tables', then use the 'Down/Up arrow' keys to read **through table headers**.
- Do all tables have a unique caption? Captions help users to find a table and understand what it’s about. e.g. When you navigate to the table via the 'Rotor' menu or by using 'T' or 'T + SHIFT', is a heading announced for the table which helps users understand what the table is about?

## Shortcut keys
You will need to use the **<a name="vo"></a>VoiceOver modifier (VO) key** 'CTRL + OPTION/ALT' in combination with other keys for keyboard shortcuts.

### General
0. **Turn VoiceOver on/off**, either with the shortcut keys 'CMD + F5' or go to 'System Preferences', then 'Accessibility', then 'VoiceOver', here you can 'Enable VoiceOver'. 
1. **Move forwards through every page element**: 'VO + Right arrow'
2. **Move backwards through every page element**: 'VO + Left arrow'
3. Navigate by **forwards through headings**: 'VO + CMD + H'
4. Navigate by **backwards through headings**: 'VO + CMD + H + SHIFT'
5. Navigate **forwards through links**: 'TAB' (When doing this if you do not cycle through all links on the page, go to Safari Preference, then go to 'Advanced' then select 'Press Tab to highlight each item on a webpage')
6. Navigate **backwards through links**: 'TAB + SHIFT'
7. To **activate a link/button**: 'VO + Space bar'
8. Bring up the **Rotor**: 'VO + U'. When the menu is displayed use 'Right/Left arrow' to cycle through the different lists, to cycle through items in a list, use the 'Up/Down arrow'. Press 'Return/Enter' or the Space bar to select an item from a list and close the Rotor menu. Close the Rotor without selecting an item by pressing 'ESC'.
9. Filter headings by level in the Rotor menu e.g. Show a list of all h2s: 'VO + U', use 'Right/Left arrow'  to select the 'Headings' list, then press '2'.
10. To **pause/restart VoiceOver talking**: 'CTRL'
11. Decrease/Increase **speaking rate**: 'VO + CMD + Up/Down arrow'
12. **Interact with an element**: 'VO + SHIFT + Down arrow'. To stop interacting with an element: 'VO + SHIFT + Up arrow'.

Note, sometimes VoiceOver will not scroll the screen when navigating, by moving forward to the next element with 'VO + Right arrow', the page should scroll down to bring this element in view.

### <a name="table-keyboard-shortcuts"></a>Tables
0. Navigate **forwards through tables**: 'T'
1. Navigate **backwards through tables**: 'T + SHIFT'
2. **One cell forwards** (right): 'VO + Right arrow'
3. **One cell backwards** (left): 'VO + Left arrow'
4. **One cell down**: 'VO + Down arrow'
5. **One cell up**: 'VO + Up arrow'
6. Read **column header**: 'VO + C'
7. Read **row header**: 'VO + R'
8. Read **entire column**: 'VO + C, VO + C'
9. Read **entire row**: 'VO + R, VO + R'

## Test using other supported assistive technology

- [Dragon Naturallyspeaking](accessibility-and-testing-with-dragon)
- [JAWS](accessibility-and-testing-with-jaws)
- [NVDA](accessibility-and-testing-with-nvda)
- [Read&Write](accessibility-and-testing-with-read-and-write)
- [TalkBack](accessibility-and-testing-with-talkback)
- [VoiceOver iOS (iPhone/iPad)](accessibility-and-testing-with-voiceover-ios)
- [ZoomText Magnifier/Reader](accessibility-and-testing-with-zoomtext)

## Other pages

- [Accessibility and Supported Assistive Technology](accessibility-and-supported-assistive-technology)