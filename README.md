# A Recommendation System for Museum Selection
Anne Chen  
2016  

App: http://216.230.228.88:3838/bootcamp006_project/Project5-Capstone/Museo/app/

### Intro
I LOVE MUSEUMS (and FOOD). But, sometimes it takes time to find the museums that meet my interest. So, I created an application aiming to recommend museums based on users' preferences and to allow users to filter the musuems that match their needs.

### Codes
- WebScrap_TripAdvisor.ipyn: Scraped ~1600 museums data from Tripadvisor (US/World)
- Data_Cleaning_addingFeature.ipynb: 
  * Merge and clean US/World museums in the "Data" folder
  * Add features (including NLP)
  * impute missingness (KNN)
  * Create dummy variables
- Create_Files_For_Shiny.ipynb: Created files that will be used in the Shiny app
- Museum_Recommendation_System.ipynb: A file just to get a sense on how to build a recommendation system based on consine similarity 
- TripAdvisor_Rating_Prediction.ipynb: Predict the rating using random forest

### "app" Folder
- global.R, server.R, ui.R: Code for running Shiny app
- get_sorted_suggestion.py: Compute consine similarity between selected museums with all other ~1600 museums and return sorted recommended musuems
- "data" folder: stores files needed for operating the Shiny app
  -  clean_category.json: {'museum': ['museum type 1','museum type 2', ...]}
  -  imputed_df_with_name.csv: master museum dataframe with ~220 features and ~1600 museums
  -  museum_img_link.json: {'museum name': 'img_link'}
  -  museum_types.json: {'museum type': ['museum 1', 'museum 2', ...]}
  -  tag_counts.json: {'museum tag': frequency count }
  -  tags_cloud.json: {'museum': ['tag 1', 'tag 2', 'tag 3' ...]}
  -  tripadvisor_merged.csv: A file containing museum data collected from TripAdvisor
- "www" folder:
  - E_tower.jpg: an img used as the background img in my app (photo credit: me!)
  - bootstrap.css: file to customize Shiny ui.R

### "Data" Folder
Data scraped from tripadvisor  
- tripadvisor_museum
- traverler_type
- traverler_rating
- tag_clouds
- review_quote
- review_content
- img_links
- museum_categories  
Files created by "Create_Files_For_Shiny.ipynb" 
- museum_types
- museum_tags
File downloaded onine
- states.csv: full and abbreviation state name

