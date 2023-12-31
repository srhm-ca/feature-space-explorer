# Feature Space Explorer
An embedding projector using `transformers` and `matplotlib`. Allows you to browse embeddings in a 3D scatterplot. You can zoom in and out, dump values to a `pandas`-compatible format, &c.

## Usage
1. Check through `python src/main.py --help` to learn about available options.
2. Pick 2+ ascii documents to compare. Run `python src/main.py $text1 $text2 $text3…` to start.
3. Explore!

## Notes
- the program will cache embeddings in a JSON file. 
- each embedding has four keys, one for the sentence and three for the `x`, `y`, `z` coordinates for the embedding.
- note the program will repack the latter three columns when displaying vectors.

## Example
![example](https://git.sr.ht/~srhm/feature-space-explorer/blob/master/example.png)

The above image provides a sense of what one should expect to see with this tool. In it, two books have had their sentences plotted out with GPT-2: one work of fiction and one work of non-fiction. While most of the sentences converge on each other, a clear wedge of sentence extends southwards. Examining this group reveals sentences like chapter labels and page numbers, structural strings whose semantic quality is different than the average sentence in a book. Perhaps not surprising, but certainly nice to see visually.
