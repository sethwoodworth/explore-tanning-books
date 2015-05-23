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
