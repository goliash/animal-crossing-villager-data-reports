# Animal Crossing villager data reports

An interactive data-analysis page about all 391 villagers in *Animal Crossing: New Horizons*: data
checks first (do three public sources agree?), then popularity, species, personality, hobby, style,
colour and birthday charts. Click any bar to filter the whole page, and try the same checks on your
own spreadsheet (CSV), all in your browser. Nothing is uploaded.

Live: [john.goliash.com/Animal-Crossing-Villager-Data-Reports](https://john.goliash.com/Animal-Crossing-Villager-Data-Reports)

## Run it

```bash
python -m http.server 8000                 # then open http://localhost:8000
pip install pillow && python tools/get-villager-pictures.py   # optional: the villager pictures
```

Without the pictures, each villager shows its initial. The pictures are Nintendo's game art, so
they're downloaded from the public [ACNH API](https://github.com/alexislours/ACNHAPI) project
rather than stored here. The GitHub Pages workflow fetches them when it publishes.

## Files

- `index.html`: the page. `js/analyst.js`: CSV reader, data checks, charts and explorer, all plain
  JavaScript. `js/villagers-data.js`: the data. `js/main.js`, `css/`: the site's shared look.
- `tools/get-villager-pictures.py`: downloads and converts the pictures.

## Data and credits

- Villagers: the Kaggle "Animal Crossing New Horizons" (Nookplaza) dataset, as used in
  [Jesse Mostipak's Kaggle notebook](https://www.kaggle.com/code/jessemostipak/animal-crossing-villager-analysis).
- Popularity: the Nook Market "most wished for" list (May 2020) and a fan tier list.
- Second copy for cross-checking: [TidyTuesday 2020-05-05](https://github.com/rfordatascience/tidytuesday/tree/master/data/2020/2020-05-05) (VillagerDB).

*Animal Crossing* and its characters belong to Nintendo. This is an unofficial fan analysis.

## License

The code is [MIT](LICENSE). The data belongs to its sources above.
