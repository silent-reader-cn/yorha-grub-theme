# YoRHa GRUB theme

![Alt text](preview.png?raw=true "Preview")

## To install:

### Step 1
Determine your monitor's resolution and whether you prefer to use Comfortaa or NewCezanne Pro as your font. Copy the corresponding folder to `/boot/grub/themes`. If you prefer to use Comfortaa, skip to Step 3. If you prefer to use NewCezanne Pro, continue to Step 2.

### Step 2
Make the NewCezanne Pro font files.

**For example:** Suppose that you already have NewCezanne Pro installed at `~/.local/share/fonts/FOT-NewCezanne Pro/FOT-NewCezanne Pro M.otf`. To make the required font files for `yorha-2880x1800-newcezanne-pro`, use the commands below: 
> ```sh
> sudo grub-mkfont --size 24 --output /boot/grub/themes/yorha-2880x1800-newcezanne-pro/fot_newcezanne_pro_m_24.pf2  ~/.local/share/fonts/FOT-NewCezanne\ Pro/FOT-NewCezanne\ Pro\ M.otf
> sudo grub-mkfont --size 32 --output /boot/grub/themes/yorha-2880x1800-newcezanne-pro/fot_newcezanne_pro_m_32.pf2  ~/.local/share/fonts/FOT-NewCezanne\ Pro/FOT-NewCezanne\ Pro\ M.otf
> sudo grub-mkfont --size 36 --output /boot/grub/themes/yorha-2880x1800-newcezanne-pro/fot_newcezanne_pro_m_36.pf2  ~/.local/share/fonts/FOT-NewCezanne\ Pro/FOT-NewCezanne\ Pro\ M.otf
> sudo grub-mkfont --size 48 --output /boot/grub/themes/yorha-2880x1800-newcezanne-pro/fot_newcezanne_pro_m_48.pf2  ~/.local/share/fonts/FOT-NewCezanne\ Pro/FOT-NewCezanne\ Pro\ M.otf
> ```

To make the required font files for the other themes, modify the commands above to specify the required font size and output folder. The required font sizes for each output folder are shown in the table below.
|Output Folder|Required Font Sizes|
|---|---|
|`\boot\grub\themes\yorha-1920x1080-newcezanne-pro`|16, 18, 24, 36|
|`\boot\grub\themes\yorha-2256x1504-newcezanne-pro`|24, 26, 30, 36, 48|
|`\boot\grub\themes\yorha-2560x1440-newcezanne-pro`|24, 32, 36, 48|
|`\boot\grub\themes\yorha-2880x1800-newcezanne-pro`|24, 32, 36, 48|
|`\boot\grub\themes\yorha-3840x2160-newcezanne-pro`|36, 48, 72|



### Step 3
Edit your `/etc/default/grub` file to include `GRUB_THEME="/boot/grub/themes/ *folder you copied* /theme.txt"`

**For example:** `GRUB_THEME="/boot/grub/themes/yorha-1920x1080-comfortaa/theme.txt"`

### Step 4
For Debian or Ubuntu, finalize your changes with `sudo update-grub`. For other Linux distributions, finalize your changes with `sudo grub-mkconfig -o /boot/grub/grub.cfg`.

## Reference
- [Screenshot of NieR: Automata loading screen](https://interfaceingame.com/screenshots/nierautomata-loading/)