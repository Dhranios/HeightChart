Adding charts:

Go to `entries.json`, and add the ID of the chart in the list of charts
Create `entries/<id>.json` with the value
```
{
    "chart": "<Chart display name>",
    "owners": []
}
```
Then you can find the chart at `https://dhranios.github.io/HeightChart/?server=<id>`, or in the dropdown if you exclude the server property

Adding owners to charts:

Go to `entries/<id>.json`, and add the discord username of the owner to the list of owners; exclude trailing and leading `_` and `.` to prevent issues with loading files.
Create `entries/<owner>/entries.json` with the value
```
{
    "owner_name": "<owner display name; optional, only needed if you had to exclude characters from the owner name>",
    "entries": []
}
```

Adding characters from owner:

Go to `entries/<owner>/entries.json`, and add the following value to the list of entries
```
{
    "name": "<Character name>",
    "height": "<height in either cm (200) or feet and inches (6`8``)",
    "art": "<file name of the art excluding .png suffix>",
    "align_bottom": <amount of pixels from the bottom to exclude/move below the floor to align feet to the ground>,
    "align_top": <amount of pixels from the top to exclude in height; should align with the top of the head excluding horns/ears/hair>
}
```
and add the art as `entries/<owner>/<art>.png`; suggested is to crop it to exclude as much whitespace as possible.
