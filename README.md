# gtfs-to-osm

Converts a gtfs schedule feed into .osm files.

The .osm files contain an empty way of the route, + all stops and their names.

Each different variant of a route is exported as its own .osm file.

Direction of travel follows the direction of the way.

Please note this was coded in an afternoon by me, with no prior knowledge of gtfs. The code is not great. But it works.

## Usage

Requires [.NET 7.0 to run.](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)

Download a gtfs file online. Then, extract its contents into `/gtfs`.

Run gtfs-reader. If you are on Windows, double-click the executable.

If you are on Linux, open a terminal where the app is and run `./gtfs-reader`.

Upon launching, you will be given a list of routes available. Select one by typing in the index number (leftmost number)

Afterward, all variants of the route will be given as .osm files in `/out`.

My recommendation is to open it in JOSM as a separate layer to compare existing routes with GTFS.

## Building

Install [.NET SDK 7.0.](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)

Clone the repo, and inside the repo run `dotnet build --configuration Release gtfs-reader.sln`

Navigate to `bin/Release/net7.0`, and create two folders `gtfs` and `out`.

Proceed to Usage for further use.