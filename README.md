# Course Recommendation System

This project is a **Course Recommendation System** built with machine learning techniques to suggest relevant courses to users based on either popularity or content similarity. The system leverages Udemy course data, including course titles, the number of subscribers, reviews, subjects, and more, to generate personalized recommendations.

---

## Features

- **Popularity-based Recommendations**: Recommends the most popular courses based on the number of subscribers and reviews.
- **Content-based Recommendations**: Suggests courses based on the similarity of course titles and subjects using Cosine Similarity.
- **User Interface (GUI)**: Built using Tkinter, the GUI provides a simple and interactive platform for users to receive recommendations.

---

## Technologies Used

- **Python 3.x**: For programming and implementing the recommendation logic.
- **Pandas**: For data manipulation and analysis.
- **Scikit-learn**: For machine learning techniques such as vectorization and cosine similarity.
- **Tkinter**: For creating the graphical user interface.
- **NeatText**: For text preprocessing (removal of stopwords and special characters).

---

## Setup Instructions

### 1. Download the Dataset
Download the course dataset (`udemy_courses.csv`) from a publicly available source or use your own dataset. Place it in the project directory.

### 2. Install Dependencies
Install the required Python libraries:

```bash
pip install pandas scikit-learn neattext tkinter
```

### 3. Run the Application
Navigate to the project directory and execute the `course_recommender.py` script:

```bash
python course_recommender.py
```

### 4. Using the GUI
Once the application runs, the GUI will open. You can:

- Select a course from the dropdown list.
- Click the **Recommend** button to view recommendations.

The system will display:

- **Popularity-based Recommendations**: Courses with the highest subscribers and reviews.
- **Content-based Recommendations**: Courses similar in title and subject.

---

## Code Overview

### 1. Data Preprocessing

- **Load Data**: The `udemy_courses.csv` file is loaded using Pandas and cleaned by removing duplicates and handling missing data.
- **Text Preprocessing**: Course titles are preprocessed to remove stopwords and special characters using the NeatText library.

### 2. Popularity-based Recommendation

- **Popularity Score Calculation**: The popularity score is calculated using the formula:

```python
popularity_score = (0.6 * number_of_subscribers) + (0.4 * number_of_reviews)
```

- **Recommendation Logic**: Courses are sorted by their popularity score, and the top 5 are displayed as recommendations.

### 3. Content-based Recommendation

- **Text Vectorization**: Course titles and subjects are combined into a new column and vectorized using CountVectorizer from Scikit-learn.
- **Cosine Similarity**: Cosine similarity is calculated between the vectorized course data to find courses with similar content.

### 4. GUI

- **Dropdown Menu**: Allows the user to select a course from the dataset.
- **Recommendation Button**: Generates recommendations based on user input.
- **Labels**: Displays the popularity-based and content-based recommendations.

### 5. Recommendation Function

Based on user input, the system provides:

- **Popularity-based Recommendations**.
- **Content-based Recommendations**.

---

## Testing

### Running the Project Locally

1. Ensure that the dataset (`udemy_courses.csv`) is placed in the project directory.
2. Follow the setup instructions to install dependencies.
3. Execute the script using Python to test the GUI and recommendation functionality.

### Testing Recommendations

- **Popularity-based Recommendations**: Verify that the courses with the highest subscribers and reviews are displayed correctly.
- **Content-based Recommendations**: Test the similarity of suggested courses to ensure relevance.

---

