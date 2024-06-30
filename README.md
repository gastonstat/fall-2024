# Principles of Data Visualization

This repository contains a Quarto-based website for the DeCal course 
__Principles of Data Visualization__ Fall-2024 edition. You can see 
a preview of it at: <https://dataviz.quarto.pub/fall-2024/>.



## Instructions for Course Staff

These instructions have been tested under MacOS.

1. Install [Quarto](https://quarto.org/docs/get-started) for Mac, Windows, or Linux.

2. [Install Git](https://git-scm.com/downloads) if you don't have it installed.

3. When department staff notify you that the class repository is ready, clone it into a local working directory on your computer. For the purposes of these instructions, we'll pretend your repository is at https://github.com/gastonstat/fall-2024.
   - You can do this from the terminal/command line or within a Git graphical application (e.g., `GitHub Desktop`).
   - From the terminal it would look like this:
     ```bash
     git clone https://github.com/gastonstat/fall-2024
     cd fall-2024
     ```
   If you need to maintain several of these websites and there is a conflict in working directory names, you can just rename the working directory after cloning it, e.g. `mv fall-2024 stat198-fall-2024; cd stat198-fall-2024`.


4. Begin making changes relevant to your course. 
   - Modify the site's metadata and table of contents in `_quarto.yml` to reflect the structure you want.

   - Update `README.md` as needed.
   - Edit the other Markdown (or Quarto Markdown) files in the working directory and add files as desired.
     - You can make use of various Quarto features discussed in the [Quarto docs](https://quarto.org/docs/authoring).

5. Update your repository with the changes to your source files. If you are using a git repository, first tell git about all files that should be in your repo.

   ```bash
   git add NEWFILE1.md NEWFILE2.md NEWDIRECTORY
   ```

   Then commit your changes:
   ```bash
   git commit -m "Initial checkin for Stat 198."
   ```

   If you modify an existing file, you can either do `git add currentfile.md` or include the `-a` flag when you run `git commit` to automatically update files that Git is already keeping track of, e.g., after modifying unit 7 files, `git commit -am "Updated Unit 7"`.

6. Push your changed to GitHub (you might choose to wait to do this until after previewing the site, discussed in the next section).
   
   ```bash
   git push
   ```


### Preview Changes (Optional)

If you want to preview the website locally on your own computer before they go live, follow these instructions. It is not strictly necessary, but we recommend doing so to spot errors. If you are confident that your changes will not break anything (for example for quick fixes), you can skip this section.

Run `quarto preview` to see your site locally. Quarto will bring up the website in a browser tab pointed to a localhost URL, such as `http://localhost:7931`. 

   - You can leave the preview running as you make changes to the source files; saving changes to the source files will generally be reflected live in your browser. You may need to refresh your browser.

   - You can also run `quarto render` to create the HTML (in the `_site` directory) without automatically displaying it. Or `quarto render file.qmd` to just render a single file. 
      - Note that you shouldn't commit the files in `_site` to your repository as they will be frequently regenerated and having them in the repository can complicate matters.



### Publish Your Changes

1. Run `quarto publish` from the command line to push updates to the course website.
BTW: we are using _Quarto Pub_ for website purposes.

You will be prompted with the following message:

```
? Publish update to:
> https://quartopub.com/sites/dataviz/fall-2024
```

Hit return, and observe the build process. It usually takes a couple of 
seconds for this to complete. 

3. If there are no problems, your website will be publicly available at <https://dataviz.quarto.pub/fall-2024/>

4. As you make changes, you can continue to run `quarto publish`.

