## ParkApi Modules

This repository contains the city modules required by the [ParkApi](https://github.com/offenesdresden/ParkApi).
To make these modules available to other software and to maintain them independently of the actual server software they have been excluded to this repository.

### Adding support for a new city

You know of a city that publishes their current parking data but isn’t yet supported by this project? Or you want to help out with one of the cities listed [here](https://github.com/offenesdresden/ParkAPI/issues?q=is%3Aopen+is%3Aissue+label%3Anew_data)? Awesome! Let’s get you started.

Just fork this project and go ahead and duplicate `cities/Sample_City.py` as a place to get started. Also have a look at other city scrapers for reference. The basic idea is to include all code specific to gathering data for a city in its file.

If you have the necessary geodata it'd be great if you could create a geojson file as well. It's name is the same as the city and in the same directory, just with `.geojson` at the end.
[geojson.io](http://geojson.io) is definitely a recommended ressource as well!

When you're done don't forget to include your new city in the tests (`./tests/test_cities.py` - it's only three lines exactly identical to the other cities in there) and run them to see if it all works out.

Now all that's left to do is to send us a pull request with your new stuff :)

Very cool! Thanks for helping out! [You rock!](http://i.giphy.com/JVdF14CQQH7gs.gif)

*Note*: Please don't include umlauts or other special characters in the name of the city file(s). The correct city name is specified inside the `city.py` file, but the filename should be ascii-compatible and with underscores instead of spaces. Should a city with the same name already exist you're going to have to find some way to make it unique, maybe by including a state or region?

