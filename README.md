# NYC-Restaurant-Week-Map

This project's goal is to provide a basic map view of most NYC Restaurant Week locations since there isn't a map view provided yet.

You can find the original NYC Restaurant Week site here:
https://www.nyctourism.com/restaurant-week

## To use
You can generate your own maps by opening and running the jupyter notebook files.

If you don't feel like running anything and just want to view the results, for now you can use something like [nbviewer](https://nbviewer.org/github/asdfblarg/NYC-Restaurant-Week-Map/blob/main/mapping_2025-01.ipynb)

## Todo
- Do some cleanup
- Add basic category filtering to the maps
- Set up a standalone html file for just the map
- Categorize and display restaurant tags better
- Improve this README

## Some Boring Background Context
Feel free to skip or ignore this section if you don't feel like reading what ended up being a stream of consciousness short story.

<details>

<summary>How this project came to be:</summary>


Sometime back in summer of 2023, I got fed up with the state of the NYC Restaurant Week site. For reasons I eventually uncovered, the site would take somewhere between 5-7 seconds to load on each page refresh, you would not be able to open each restaurant result in new tabs, clicking on a restaurant result and then going back to the search would trigger another page refresh and reset your search filters and etc. Going through the list of restaurants extremely frustrating to say the least, but a necessary evil to hunt for some great prix fixe deals.

While searching for decent locations, at some point I came across a reddit post from dx724 with a working map view of the restaurants.
https://github.com/dx724/RestaurantWeekMap

I found it quite useful, but would have preferred a tiny bit more functionality (and maybe better visuals). The repo only displayed the end result of parsed but didn't give any indication of how the data was obtained. Thus I decided to give my own crack at attempting something similar myself as a side project for the heck of it.

It turns out that at the the NYC Restaurant Week site was embedding their entire convoluted nested json structure in the html under a `__NEXT_DATA__` script tag. Retrieving that data and formatting the json yielded a 92 mb json file. Go figure. No wonder the performance of the site was horrible. After painfully fiddling with the json data, I was able to eventually grab the data I needed and store it in an easier format to work with, and eventually get a simple map generated in a jupyter notebook using folium. This worked well enough for my personal needs and I shelved the project without ever feeling the need to put it up publicly.

Eventually, time went on and next time the NYC Restaurant Week rolled around, I found that they no longer had a cursed mass of json embedded into the html and had a proper api to fetch data from. Hurrah. This little project became less useful for me after that. I also became less interested in trying out additional Resturant Week locations as well.

Fast forward to Winter 2025, for reasons I won't bother getting into as this story has gone long enough, I've decided to revisit the code and update the maps with the new api data. Only this time, I might as well have this in a public repo.

</details>
