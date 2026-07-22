# Flaberpengu's Awesome Graph

This plugin provides a graph view of your Joplin notes, with arrows denoting connections between notes. See [Features](#features) below.

This is a fork of [@sepremento](https://github.com/sepremento)'s [Sepremento's Awesome Graph](https://github.com/sepremento/joplin-graph-view) plugin with some tweaks applied for my personal taste. The broad structure of the app and the bulk of the code is untouched. I have also inherited many of the listed [bugs](#bugs).

In general, I prefer an Obsidian-style to my graph with respect to node movement and feel, which I am trying to emulate here. I have also added miscellaneous quality of life improvements. For planned features/changes, see [plans](#plans).

## AI Usage

I have no background in Javascript or Typescript, and have no real interest in learning either of these at this time. I do, however, have extensive background in programming in other languages. Thus, this plugin serves as my first exploration into using [Opencode](https://opencode.ai/) and coding agents - it is highly likely that any changes in this repository were not written by me. Therefore, I expect bugs and poor performance, at least for now.

# Features

- Collect and draw all connections between notes in your Joplin database. Backlinks
are included. There is a feature pending for a toggle "Backlinks on/off".
- Vary depth of your linked tree rooted in the current note.
    - Click on the `Max. distance` slider to set tree depth between `0` and
    `5`. Zero is like "Global view" in Obsidian, all notes are displayed.
- Adjustable centre strength, charge strength, and link distance between nodes.
    - Set all of these to `0` for completely free placement of nodes (like in Obsidian).
- Select multiple notes to draw in the Graph UI.
- Open note or tag associated with node under curset with `CTRL-LeftClick`.
- Build a graph according to some query independent of selected notes.
    - Type your query in the "Query" input field and press `Enter`. Query syntax
    is [Joplin search syntax](https://discourse.joplinapp.org/t/search-syntax-documentation/9110).
- Filter notes accorning to some query defined in the UI.
    - Type your filter query in "Filter" input field and precc `Enter`. All
    notes that satisfy the condition in the "Filter" input field are EXCLUDED from the graph.
- Toggle tag nodes on and off in the UI.
- Flexible forces tweaks for each force in the graph UI in "Graph parameters" block.
- Add coloured groups to your graph in "Groups" block.
    - For each group type your condition in the last input field and press `Enter`
    or click the `+` button.
    - Colours are assigned automatically but can be adjusted.
    - You can adjust your filters dynamically afterwards, don't forget to press `Enter`,
    otherwise the filter would not be updated.
- Colour nodes by their parent notebook.
    - Toggleable on or off.
    - Default colours with per-notebook colour picker, should you wish to change the colours.

**Note:** Requires Joplin 1.7.0+

https://github.com/user-attachments/assets/3b9d0786-83f7-4f9e-8c5d-2eb87b6f532f

# Bugs

- When adding new note if that note falls into one of the coloured groups defined by user it is not coloured until the graph is restarted or filter query is updated.
- When you switch quickly between notes in the same tree sometimes graph does not update. Toggle graph off and on to rebuild

# Plans

- Option for opening the graph view in a window.
- Option to toggle notebooks off when in "Global" view.
- Make focus smoother when hovering/selecting nodes.
- Improve performance + reduce CPU usage.

# Development

1. Check out the Git repository
1. `cd` into the repository and run `npm install` to install dependencies.
1. Run `npm run dist` to build the plugin file.
1. Launch [Joplin in dev
   mode](https://joplinapp.org/api/references/development_mode/) and load the
   plugin.

# License

In the spirit of Sepremento's plugin, this library is licensed under the MIT license. See [LICENSE](LICENSE) for more info.

keywords: joplin-plugin
