## **Setup in OBS**

1. **Add to OBS:**  
   * Add a new **Browser Source** in OBS.  
   * Paste your configured URL *Example:* https://synnbunn.github.io/discount-media-request/?twitch=synnbunn&list=PLRBp0Fe2GpgnIh0AiYKh7o7HnYAej-5ph\&vol=20.  
   * Set Width to 550 and Height to 150 (or whatever fits your layout).  
   * Check **"Control Audio via OBS"** so you can adjust the volume in your audio mixer.  
2. **Interact:**  
   * Right-click the Browser Source in OBS and select **Interact** to click the Play/Pause or Skip buttons directly\!

## **URL Configuration Parameters**

You customize how the player behaves by adding these parameters to the end of your URL, separated by the & symbol.  
| **Parameter** | **What it does** | **Example** | **Default** |  
| twitch | Your Twitch channel name to listen for \!sr commands. | ?twitch=synnbunn | *None (SR disabled)* |  
| list | The YouTube Playlist ID for background music. | \&list=PLRBp0Fe... | *Backup Playlist* |  
| vol | Starting volume from 0 to 100\. | \&vol=40 | 30 |  
| shuffle | Set to 0 to disable shuffling the background playlist. | \&shuffle=0 | 1 (Enabled) |  
| maxq | Maximum number of songs allowed in the request queue. | \&maxq=100 | 50 |

## **Chat Commands**

Users in your configured Twitch channel can simply type:

* \!sr https://www.youtube.com/watch?v=dQw4w9WgXcQ  
* \!sr dQw4w9WgXcQ


## **Customizing Colors**

You don't need to edit the HTML file to change the colors\! You can override them directly inside OBS.  
Double-click your Browser Source in OBS, scroll down to the **Custom CSS** box, and paste this snippet, changing the Hex colors to whatever you like:  
:root {  
    \--bg-color: rgba(18, 18, 18, 0.95);      /\* Main widget background \*/  
    \--bg-queue: rgba(18, 18, 18, 0.85);      /\* Dropdown queue background \*/  
    \--accent-color: \#9146FF;                 /\* Twitch Purple (Badges & Usernames) \*/  
    \--text-primary: \#ffffff;                 /\* Main text color \*/  
    \--text-secondary: \#a0a0a0;               /\* Subtitles / Channel name \*/  
    \--border-color: rgba(255, 255, 255, 0.1);/\* Outlines \*/  
    \--success-color: \#22c55e;                /\* Green toast when song added \*/  
    \--error-color: \#ef4444;                  /\* Red toast for errors \*/  
}
