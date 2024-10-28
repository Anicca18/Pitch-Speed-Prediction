![download](https://github.com/user-attachments/assets/a5a6cf11-bbe4-4492-bb10-d4fc795c24c0)

# Pitch-Speed-Prediction
The aim of this project is to predict the pitch type and pitch speed of an individual pitcher during this year's World Series games featuring the Yankees and the Dodgers. The goal is to utilize machine learning models to make more accurate predictions and potentially outperform betting platforms like DraftKings.

## Data
The dataset comes from the `pybaseball` library, which provides detailed MLB data. The main features we're using for predictions are the type of pitch ('pitch_type'), the batter's stance ('stand'), the pitcher's throwing arm ('p_throws'), the number of balls and strikes, the year of the game ('game_year'), the number of outs ('outs_when_up'), the inning, the pitch count ('pitch_number'), the score of the batting team ('bat_score'), the speed of the pitch ('effective_speed'), the horizontal and vertical movement of the pitch ('pfx_x' and 'pfx_z'), the batter, the pitcher, and the score of the fielding team ('fld_score'). These features provide key details about each pitch, the game situation, and player information, which are important for making accurate predictions.

## Method
The methods used in this project include a RandomForestRegressor to calculate the probability of different pitch types and a RandomForestClassifier for building predictive models. Feature engineering was performed by adding new features to enhance the model's performance. This included creating dummy variables for each pitch type and generating interaction terms between pairs of important features to capture their combined effects.

### Manual Input
<img width="663" alt="Screenshot 2024-10-28 at 12 44 59 PM" src="https://github.com/user-attachments/assets/8be87723-f39d-4f3a-84d4-1b5706866908">

The model also allows users to manually input various game conditions during a live game to get real-time predictions. These inputs include information such as the batter's stance, the pitcher's throwing arm, the current count, and other game-specific details. This feature enables live predictions, providing insights into pitch type and speed as the game unfolds.

## Results
<img width="772" alt="Screenshot 2024-10-28 at 12 40 12 PM" src="https://github.com/user-attachments/assets/9e6a65ff-7859-4e43-89ea-c4f385167f2f">

The graph shows the distribution of effective speed for different pitch types thrown by Sean Manaea. Each violin plot represents the spread and density of the effective speed for a specific pitch type, such as FF (Four-seam Fastball), ST (Sinker), SL (Slider), CH (Changeup), and SI (Sinker). The wider sections indicate where the speeds are more frequent, while the central black bar represents the interquartile range, giving a clear visual representation of pitch speed variation by pitch type. If we can determine the pitch type, we will have a better idea of what the effective speed is likely to be.

<img width="719" alt="Screenshot 2024-10-28 at 12 42 42 PM" src="https://github.com/user-attachments/assets/ec93ac74-01af-406b-befa-36c5804b4e42">

The second graph shows a binomial-like distribution of effective speeds, with a clear distinction between pitch speeds above and below 90 mph. This indicates that if we can predict the pitch type, we have a good chance of predicting whether the speed will be above or below 90 mph, providing valuable insight for making informed predictions.

<img width="391" alt="Screenshot 2024-10-28 at 12 47 01 PM" src="https://github.com/user-attachments/assets/b096df53-be06-4fa5-b40a-e5c6201ab379">

The predictions are presented in a simple table format, showing the possible pitch types along with their respective probabilities and predicted effective speeds. This allows users to easily understand the model's output and make informed decisions based on the likely outcomes.

## Conclusion
The model provides valuable insights, but there are several areas for improvement:

- Integrate live imaging data to predict the pitch type based on the pitcher's stance and movements.
- Improve hyperparameter tuning to enhance the accuracy and efficiency of the predictions.
- Include more advanced feature engineering to capture additional contextual factors.
- Utilize deep learning techniques for better performance on complex patterns in the data like image processing.


## Directory
Data: [Pybaseball](https://pypi.org/project/pybaseball/2.0.0/)
Presentation: [Presentation.pdf](https://github.com/user-attachments/files/17546271/Presentation.pdf)