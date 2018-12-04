This theme is based upon the game "Age of Conan"
For copyright see the file "copyright"
Made by Elio R. Heinrich | downsource@googlemail.com | www.sequency.org
It's tested with a resolution of 1280x1024px, I don't know which issues other resolutions might cause.


To install this theme either run "install_ageofsystems.sh" or execute the following commands:
    sudo cp AgeOfSystems -R /usr/share/plymouth/themes/ # Some distributions use another path.
    sudo plymouth-set-default-theme AgeOfSystems
    sudo /usr/lib/plymouth/plymouth-update-initrd
    sudo mkinitrd

If you changed something in the script file, there is no need to re-run the last three commands.


    
How to customize the Theme:

To add your own preferred Text just add it into the array, I think it's self-explanatory. NOTE: you should add \n after 6-7 Words, the text is not automatically adjusted to the boxes.
    text_array = [["Title","Description Text"],["Second Title","Second Description"]];

Same goes for the hint text:
    text_hint_array = [["Tip:\nHit \"escape\" to show console output."]];

To use the text change the number in the first brackets to the desired ID. The number in the second brackets stands for: 0 - Title, 1 - Description. Hint text follows the same system.
    title_text = text_array[0][0];
    description_text = text_array[0][1];
    text_hint_title = text_hint_array[0][0];
    text_hint = text_hint_array[0][1];

The Background-Image is named "background_XX.png". The XX stands for a certain number, beginning with "0" ("background_0.png")
It's intended that you can use different backgrounds without the need to rename it. In the future there eventually may be a random generator which selects between the files, but at the moment this is not working.
    bgnumber = 1;
    
The Sizes of the Textboxes, should be self-explanatory too:
    textbox_top_distance_left=20;
    textbox_top_distance_top = 100;
    textbox_top_width = 420;
    textbox_top_height= 420;

    textbox_bottom_distance_left = textbox_top_distance_left;
    textbox_bottom_distance_top = textbox_top_distance_top + textbox_top_height + 50;
    textbox_bottom_width = textbox_top_width;
    textbox_bottom_height = 60;
    
Its possible to move or scale the background-image

Negative: Move to the left, Positive: Move to the right
    bg_image_shift_x = 0;

Negative: Move down, Positive: Move up
    bg_image_shift_y = 0;

Zoom horizontal (Min. 0.0, Standard 1)
    bg_image_zoom_width = 1;

Zoom vertical (Min. 0.0, Standard 1)
    bg_image_zoom_height = 1;
