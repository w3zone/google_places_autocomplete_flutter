# google_places_autocomplete_flutter

forked from google_places_flutter

# Add dependency into pubspec.yml

```
dependencies:
  flutter:
    sdk: flutter
  google_places_autocomplete_flutter: ^1.0.5
  
```  

# Google AutoComplete TextField Widget code


```
    GooglePlaceAutoCompleteFlutterTextField(
        textEditingController: controller,
        googleAPIKey: "YOUR_GOOGLE_API_KEY",
        inputDecoration: InputDecoration()
        debounceTime: 800 // default 600 ms,
        countries: ["in","fr"],// optional by default null is set
        isLatLngRequired:true,// if you required coordinates from place detail
        autcompleteBaseUrl: "", // if provided will use it as a base url for loading autocomplate data
        placesBaseUrl: "", // if provided will use it as a base url for loading place details
        getPlaceDetailWithLatLng: (Prediction prediction) {
         // this method will return latlng with place detail
        print("placeDetails" + prediction.lng.toString());
        }, // this callback is called when isLatLngRequired is true
        itmClick: (Prediction prediction) {
         controller.text=prediction.description;
          controller.selection = TextSelection.fromPosition(TextPosition(offset: prediction.description.length));
        }
    )
    
```
# Customization Option
 You can customize a text field input decoration and debounce time 

# Screenshorts
<img src="https://raw.githubusercontent.com/w3zone/google_places_autocomplete_flutter/master/sample.jpg" height="400">

