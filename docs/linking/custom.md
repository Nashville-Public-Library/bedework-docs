---
title: Creating Custom URLs
---

# Creating Custom URLs

To build a link, you need to place the block number right after `bwNav`

In the array, this is how it is written: First the bwNav block number, then a dash, then the alias OR view OR block name

Here are your alias / view / block name examples:

- 0 Age
    - Children - `useragrpcalsuiteMainCampusChildrens`
    - Teens - `useragrpcalsuiteMainCampusTeens`
- 1 Locations
    - Green Hills - `publicaliasesLocationsGreenHills`
- 2 Topics
    - Writing - `publicaliasesBrowseByTopicWriting`
- 3 Series
    - Studio NPL - `useragrpcalsuiteMainCampusSeriesStudioNPL`

To build a search, add your search terms in the parentheses right after `https://events.library.nashville.org/cal/main/listEvents.do?b=de&listMode=true&setappvar=bwQuery(Nashville%20Public%20Library%20Board%20of%20Trustees%20Meeting)`

Use `%20` in between each search term to act as a space in the search box.

## Age Groups

The variable part is after `useragrpcalsuite`

- Adults:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(bwNav0-useragrpcalsuiteMainCampusAdults|||)&setappvar=bwQuery()  
- Teens:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(bwNav0-useragrpcalsuiteMainCampusTeens|||)&setappvar=bwQuery()
- Children:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(bwNav0-useragrpcalsuiteMainCampusChildrens|||)&setappvar=bwQuery()

## Locations

The variable part is after `publicaliasesLocations`

- Bellevue: https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsBellevue||)&setappvar=bwQuery()
- Edgehill: https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsEdgehill||)&setappvar=bwQuery()

## Browse by Topic

The variable part is after `publicaliasesBrowseByTopic`

- Arts and Crafts: https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicArtsandCrafts|)&setappvar=bwQuery()
- Music: https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicMusic|)&setappvar=bwQuery()
- Computers & Technology:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicComputersandTechnology,bwNav2-publicaliasesBrowseByTopicJobs|)&setappvar=bwQuery()

## Series

The variable part is after `useragrpcalsuiteMainCampusSeries`

- Be Well at NPL:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesBeWellatNPL)&setappvar=bwQuery()
- Salon@615:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesSalonat615)&setappvar=bwQuery()
- StudioNPL
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()
- Movies at Main
https://events.library.nashville.org/cal/main/listEvents.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesMoviesatMain)&setappvar=bwQuery()
## Example Links

- Topic > Writing: https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicWriting|)&setappvar=bwQuery()

- Topic > Health and Wellness:
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicHealthandWellness|)&setappvar=bwQuery()   

- Series > Studio NPL: https://events.library.nashville.org/cal/main/listEvents.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Series > Be Well at NPL issues:
https://events.library.nashville.org/cal/main/listEvents.do?b=de&listMode=true&setappvar=bwFilters(|||bwNav3-useragrpcalsuiteMainCampusSeriesBeWellatNPL)&setappvar=bwQuery()

- Topic > Story Time AND Location > Green Hills AND Age > Children:
https://events.library.nashville.org/cal/main/listEvents.do?setappvar=bwFilters(bwNav0-useragrpcalsuiteMainCampusChildrens|bwNav1-publicaliasesLocationsGreenHills|bwNav2-publicaliasesBrowseByTopicStoryTime|)&setappvar=bwQuery()  

- Age > Teen AND Series > Studio NPL AND Topic > Music AND Location > East: https://events.library.nashville.org/cal/main/listEvents.do?setappvar=bwFilters(bwNav0-useragrpcalsuiteMainCampusTeens|bwNav1-publicaliasesLocationsEast|bwNav2-publicaliasesBrowseByTopicMusic|bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- One Location: Online (NPL Universe): https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsOnline||)&setappvar=bwQuery()

- TWO locations:
https://events.library.nashville.org/cal/main/listEvents.do?setappvar=bwFilters(|bwNav1-publicaliasesLocationsEast,bwNav1-publicaliasesLocationsSoutheast||)&setappvar=bwQuery()    
comma after the first location then put in the second location - because it is an array and those are separated by commas
both locations need to be in the same pipe

- Story Time around the system
https://events.library.nashville.org/cal/main/listEvents.do?setappvar=bwFilters(||bwNav2-publicaliasesBrowseByTopicStoryTime|)&setappvar=bwQuery()    

- Search ONE term:
https://events.library.nashville.org/cal/main/listEvents.do?b=de&listMode=true&setappvar=bwQuery(meditation)  

### Studio NPL

- Main Studio NPL https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsMAIN||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- East Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsEast||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Edgehill Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsEdgehill||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Goodlettsville Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsGoodlettsville||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Madison Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsMadison||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Southeast Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsSoutheast||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- Main Studio Audio Production
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsMAIN||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery(audio)

- Bordeaux Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsBordeaux||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

- East Cypher
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsEast||)&setappvar=bwQuery(cypher)

- Edmondson Pike Studio
https://events.library.nashville.org/cal/main/setSelectionList.do?b=de&listMode=true&setappvar=bwFilters(|bwNav1-publicaliasesLocationsEdmondsonPike||bwNav3-useragrpcalsuiteMainCampusSeriesStudioNPL)&setappvar=bwQuery()

### Week to Week
- See the Week-to-week view with descriptions in the results list:
https://events.library.nashville.org/cal/main/showEvents.rdo?b=de&setappvar=summaryMode(details)
