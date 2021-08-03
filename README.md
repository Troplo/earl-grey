# earl-grey
Elegant dark theme for Gitea. 

I mostly bruteforced which colors to change by inspecting every element with undesirable colors, and I ended up with a theme that I'm quite proud of. However, it will definitely have a lot of bugs, please report them and fix them!

It's really easy to fix color inconsistencies, just use a color picker to get the color, then Inspect Element and go to the styling section. There, CTRL+F and search for the color (note that the letters must be lowercase, the colors whose letters aren't lowercase are most likely added by me)

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
