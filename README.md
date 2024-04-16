# Paleo Classification for COL
The Catalogue of Life is missing out many fossil groups.
This dataset tries to fill these gaps down to family level at most 
and is listed in [CheckistBank](https://www.checklistbank.org/dataset/293559/).

## Files
The main taxonomy tree lives in [taxonomy.txtree](taxonomy.txtree). 
Information about the dataset as a whole and how to cite it is kept in metadata.yaml,
a list of structured references is in [BibTex](reference.bib). 
References from this list are [cited in the taxonomy file](https://github.com/CatalogueOfLife/coldp/blob/master/docs/publishing-guide-txtree.md).

BibTex content can be retrieved from CrossRef for most DOIs when known.
For example by using curl on the terminal like this:
> curl --location --silent --header "Accept: application/x-bibtex" https://doi.org/10.1080/11035890601282097 
> @article{Eriksson_2006,
    doi = {10.1080/11035890601282097},
    url = {https://doi.org/10.1080%2F11035890601282097},
    year = 2006,
    month = {jun},
    publisher = {Informa {UK} Limited},
    volume = {128},
    number = {2},
    pages = {97--101},
    author = {Mats E. Eriksson},
    title = {Polychaete jaw apparatuses and scolecodonts from the Silurian Ireviken Event interval of Gotland, Sweden},
    journal = {{GFF}}
}

## Example data
Prefix extinct taxa with the dagger symbol and use the following properties in brackets where needed:

 - `PUB`: the bibtex identifier for the nomenclatural reference where the exact name was originally published
 - `ENV`: a list of environment values, separated by commas
 - `CHRONO`: a geochronological time range for the earliest-latest appearance of the taxon. The range is delimited by a hyphen, e.g. `Jurassic-Cretaceous`

```
    †Kalloprion kilmisteri [species] {PUB=Eriksson_2006 ENV=marine CHRONO=Llandovery-Wenlock}
```
