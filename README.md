# explore-tanning-books
A notebook describing experiments with a collection of books on Tanning from Open Library

## Open Library list
I've created an [OpenLibrary 'list'](https://openlibrary.org/people/sethish/lists/OL72694L/Tanning)
that includes several books about tanning from the public domain.

We will get a machine readable version of this as a starting point downloading and analyzing book text.

## Machine readable export

### Data Export
On the Tanning list page, there are links for exporting the list as json, html or bibtex.
Lists are also available as Atom feeds
(unclear if this is related to ODPS, an extension of Atom for books).

At the time of this writing, all of the export formats return 
[empty content](https://openlibrary.org/people/sethish/lists/OL72694L/Tanning/export?format=json).
This appears to be a known issue for OL [#181](https://github.com/internetarchive/openlibrary/issues/181)
but hasn't had any progress since 2013 :-|).

Luckily, there is an alternate [restful api](https://openlibrary.org/dev/docs/api/lists)
that provides a separate json interface to lists. 
Listing the 'seeds' in my Tanning list gives us this [json result](https://openlibrary.org/people/sethish/lists/OL72694L/seeds.json).
The seed json is in `data/seeds.json`.

### Readable text files

There doesn't appear to be an API endpoint for fetching the raw text verions of books,
nor a unique identifier that specifies what to fetch from IA.

Text-book of Tanning leads to:

    https://ia902602.us.archive.org/28/items/textbookoftannin00proc/textbookoftannin00proc_djvu.txt

Which is on achive.org as:

    https://archive.org/details/textbookoftannin00proc


Searching for the `OL17085608W` value doesn't come up with any results on archive.org
