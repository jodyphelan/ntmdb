# Repo moved

> [!IMPORTANT]
> This development of this database has moved to https://github.com/pathogen-profiler/ntm-db (and ntm-profiler now pulls from there)

# ntmdb

This repository hosts resistance databases for several non-tuberculous mycobacterial species as well as kmers which can be used to identify species.
The databases are hosted on github to promote collaboration and knowledge sharing. 

# Want to contribute?

If you think a mutation/gene should be removed or added please raise and issue [here](https://github.com/jodyphelan/ntmdb/issues). 

### Adding/removing mutations and genes
Mutations/genes for existing or new can be added by submitting a pull request on a fork. If that previous sentence made no sense to you then you can suggest a change using an [issue]((https://github.com/jodyphelan/ntmdb/issues)) and we will try help. 

# Why is there a seperate github repository?
With analysis pipelines pretty much standardised, it is evident that accuracy of prediction is affected mostly by the underlying library of mutations. As new evidence for the inclusion or exclusion of mutations is generated, there is a constant need to update and re-evaluate the mutation library. Moreover, it is important for the control of the library to be put in the hands of the end-users. By hosting the library on a separate repository (rather than buried deep in the profiling tool code) it makes it easier to find out exactly which mutations are present. Additionally, github has a number of useful features which can be utilised:

* All changes to the library are tracked and can be easily be reverted to previous versions.
* Users can raise concerns or discuss the library using the Issues section of the github repository.
* Different versions of the library can be maintained using Forks. Allowing users to experiment with the library without affecting the main project. These changes can then be merged into the main repo after the changes are reviewed.
* Multiple users/developers can contribute towards the library.

**tl;dr** - Hosting it here makes it easier to update the library.

It can be used as a direct input to [NTM-Profiler](https://github.com/jodyphelan/NTM-Profiler), but can also be used for any custom pipeline.




# How does it work?

The databases are hosted in [db](https://github.com/jodyphelan/ntmdb/tree/main/db). The [ntm_db.kmers.txt](https://github.com/jodyphelan/ntmdb/blob/main/db/ntm_db.kmers.txt) file contains the kmers which have been associated with different species. Subfolders, such as [Mycobacteroides_abscessus](https://github.com/jodyphelan/ntmdb/tree/main/db/Mycobacteroides_abscessus), contain species specific resistance databases (look for the [csv files](https://github.com/jodyphelan/ntmdb/blob/main/db/Mycobacteroides_abscessus/Mycobacteroides_abscessus.csv)), as well as the reference genome and annotation files as well as some other files which are used by [NTM-Profiler](https://github.com/jodyphelan/NTM-Profiler).