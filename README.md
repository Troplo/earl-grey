# earl-grey
Elegant dark theme for Gitea. *Gitea. Earl Grey. Hot.* 

I mostly bruteforced which colors to change by inspecting every element with undesirable colors, and I ended up with a theme that I'm quite proud of. However, it will definitely have a lot of bugs, please report them and fix them!

It's really easy to fix color inconsistencies, just use a color picker to get the color, then Inspect Element and go to the styling section. There, CTRL+F and search for the color (note that the letters must be lowercase, the colors whose letters aren't lowercase are most likely added by me)

![gitea-1](https://user-images.githubusercontent.com/45886986/128325883-e9a92c1c-fb01-43f5-8e25-3278b0780e8c.png)
![gitea-2](https://user-images.githubusercontent.com/45886986/128325892-8092a5de-642a-4168-99aa-80c65477d9c5.png)
![gitea-3](https://user-images.githubusercontent.com/45886986/128325905-aab0dec5-bd77-4687-a43c-9cb97415949b.png)

# Installation
1. To install, first check your CustomPath by visiting the admin panel of your instance. Mine is `/var/lib/gitea/custom`. You'll need to create 3 directories. Something like `/var/lib/gitea/custom/public/css` should be your final structure.

2. Clone the repository
   
`git clone https://github.com/acoolstraw/earl-grey`

3. Move `theme-earl-grey.css` into the `public/css` directory
   
`cp earl-grey/theme-earl-grey.css /var/lib/gitea/custom/public/css/`

4. Add (or replace) the following to your `app.ini`:
```
[ui]
DEFAULT_THEME = earl-grey
THEMES        = gitea,arc-green,earl-grey
```

5. Clean up
`rm -r earl-grey`
