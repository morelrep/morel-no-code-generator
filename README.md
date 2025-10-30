# Build your MOREL website from a Zotero collection in 8 simple steps
1. **Check if you have the requirements**
  - A [Zotero account](https://www.zotero.org/user/register/)
  - A [GitHub account](https://github.com/signup)
2. **Prepare the Zotero Fields** for a MOREL website. MOREL items are added in the same way that items are added in any [Zotero library](https://www.zotero.org/support/adding_items_to_zotero). In its current version, MOREL can only process items of type `book`. Since not all the fields needed for MOREL are available for the `book` content type, some considerations must be made:
  - Excerpt: the fragment from each MOREL record corresponds to the `notes` of Zotero (see the [documentation](https://www.zotero.org/support/notes) about Zotero notes). In its current version, MOREL *only accepts one excerpt per book*.
  - Cover: the cover is a jpg file that is added as an `attachment` to the Zotero item (see the Zotero attachments [documentation](https://www.zotero.org/support/attaching_files)).
3. **[Fork](https://github.com/morelrep/morel-no-code-generator/fork) this repository** — that is, [create a copy](https://github.com/morelrep/morel-no-code-generator/fork) in your [GitHub](https://github.com) account.
4. **Go to the `actions` tab** and enable workflows.
5. **Open `_config.yml` and change**:
  - The `title` to your site's.
  - The `tagline` to your site's.
  - The `email` and/or social media accounts to your site's.
  - The `jotform` link (create your free account at https://www.jotform.com/).
6. **Go to the `settings` tab**, open the `pages` section, and select `gh-pages` as the branch that will build the site.
7. **Open the file `_abouts/site-description.md`** and write a description for your site. The `<!-- more -->` line separates what appears in the footer across all pages from the longer description that appears on the `about` page only.
8. **Generate the content from Zotero** by [exporting a collection](https://forums.zotero.org/discussion/5286/can-one-export-a-collection-and-not-the-entire-library), subcollection or library as a `csv` file, and replacing the content of `assets/data/books_zotero.csv`.
# Other features
To add cover images to your site, follow these steps:
1. Add a cover image to your item in your Zotero library by dragging it as an attachment
2. Open your terminal in the MOREL folder
3. Create a Python environment using ```python3 -m venv assets/env```
4. Run ```pip install requirements.txt``
5. Export your library or collection from Zotero as .csv file. Remember to check the "add notes" option to add excerpts.
6. Copy the content of the CSV file in assets/data/books_zotero.csv
7. Run ```source assets/env/bin/activate```
8. 