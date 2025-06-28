# 🎨 Doodler - AI-Powered Doodle Classification App

A complete machine learning web application for doodle classification built entirely with **vanilla JavaScript** - no external JS libraries or Python frameworks required! All classification algorithms, feature extraction, and visualizations are implemented from scratch.

## 🌟 Features

### 🖊️ Interactive Drawing Interface
- **Web-based Sketch Pad**: Draw doodles directly in your browser
- **Multi-class Support**: Classify 8 different object types:
  - 🚗 Car
  - 🐠 Fish  
  - 🏠 House
  - 🌳 Tree
  - 🚲 Bicycle
  - 🎸 Guitar
  - ✏️ Pencil
  - 🕒 Clock

### 🤖 Built-in Machine Learning
- **K-Nearest Neighbors (KNN) Classifier**: Implemented from scratch in vanilla JavaScript
- **Custom Feature Extraction**: Analyzes drawing characteristics including:
  - Width and height of drawings
  - Path count and point count
  - Geometric properties
- **Real-time Prediction**: Get instant classification results as you draw
- **Training/Testing Split**: Automatic data splitting for model evaluation

### 📊 Advanced Data Visualization
- **Interactive Scatter Plot**: Explore your dataset in 2D feature space
- **Decision Boundary Visualization**: See how the classifier separates different classes
- **Zoomable and Pannable Charts**: Navigate through data with mouse controls
- **Real-time Data Points**: Watch new drawings appear on the chart instantly
- **Nearest Neighbors Display**: Visualize which training samples influence each prediction

### 🗄️ Complete Dataset Management
- **Data Collection Tool**: Create your own training datasets through the web interface
- **JSON and CSV Export**: Multiple data format support
- **Image Generation**: Automatically convert drawings to PNG images
- **Dataset Statistics**: View accuracy metrics and performance statistics
- **Raw Data Processing**: Convert user drawings into structured datasets

### 🎯 Model Evaluation
- **Accuracy Metrics**: Real-time accuracy calculation on test data
- **Performance Visualization**: See how well your model performs
- **Cross-validation Ready**: Easy to extend with additional evaluation methods

## 🚀 Getting Started

### Prerequisites
- Node.js (for dataset processing only)
- Modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/doodler.git
   cd doodler
   ```

2. **Install minimal dependencies** (only for server-side image processing)
   ```bash
   cd node
   npm install
   ```

3. **Generate dataset** (if you have raw drawing data)
   ```bash
   npm run postinstall
   ```

4. **Open the app**
   - Open `index.html` in your web browser for the main classifier
   - Open `web/creator.html` for the data collection interface

## 📁 Project Structure

```
Doodler/
├── index.html              # Main classification app
├── web/                    # Web interface components
│   ├── creator.html        # Data collection interface
│   ├── js/                 # UI components
│   └── chart/              # Visualization engine
├── common/                 # Core ML algorithms (vanilla JS)
│   ├── classifiers/        # KNN implementation
│   ├── featureFunctions.js # Feature extraction
│   └── utils.js           # Mathematical utilities
├── node/                  # Dataset processing tools
├── data/                  # Training/testing datasets
└── resources/             # Decision boundary visualizations
```

## 🛠️ Technical Implementation

### Pure Vanilla JavaScript Architecture
- **No External Libraries**: All machine learning algorithms implemented from scratch
- **No Frameworks**: Pure HTML5 Canvas for drawings and visualizations  
- **No Python Dependencies**: Entire ML pipeline runs in the browser
- **Modular Design**: Clean separation between ML logic, UI, and data processing

### Core Algorithms
- **Distance Calculations**: Euclidean distance for nearest neighbor search
- **Normalization**: Min-max feature scaling
- **Classification**: Majority voting in KNN
- **Visualization**: Custom charting engine with zoom/pan capabilities

### Data Flow
1. **Collection**: Users draw doodles through web interface
2. **Processing**: Extract geometric features from drawing paths
3. **Training**: Use KNN to learn from training examples
4. **Prediction**: Classify new drawings in real-time
5. **Visualization**: Display results and decision boundaries

## 🎮 Usage

### Creating Training Data
1. Open `web/creator.html`
2. Enter your name
3. Draw the requested objects
4. Download your data file
5. Place it in the `data/raw/` directory

### Running Classification
1. Open `index.html`
2. Click "DOODLE" to start drawing
3. Watch real-time predictions
4. Explore the scatter plot visualization
5. Click on data points to see training examples

### Analyzing Performance
- View accuracy statistics in the control panel
- Explore decision boundaries in the chart
- Examine nearest neighbors for each prediction

## 🧠 Machine Learning Details

### Feature Engineering
The app extracts meaningful features from raw drawing data:
- **Geometric Features**: Width, height, aspect ratio
- **Structural Features**: Number of paths and points
- **Spatial Features**: Bounding box properties

### Classification Algorithm
- **Algorithm**: K-Nearest Neighbors (k=50 by default)
- **Distance Metric**: Euclidean distance in feature space
- **Voting**: Majority class among nearest neighbors
- **Normalization**: Features scaled to [0,1] range

### Model Training
- **Training Split**: 50% of data used for training
- **Testing Split**: 50% of data used for evaluation
- **Real-time Updates**: New drawings immediately available for classification

## 🎨 Customization

### Adding New Classes
1. Update the `classes` array in `web/creator.html`
2. Add corresponding styles in `common/utils.js`
3. Collect new training data
4. Regenerate the dataset

### Tuning Parameters
- Modify `k` value in KNN constructor
- Adjust feature functions in `featureFunctions.js`
- Customize visualization styles

### Extending Features
- Add new feature extraction functions
- Implement additional classifiers
- Create custom visualization types

## 📈 Performance

- **Real-time Classification**: Sub-millisecond prediction times
- **Interactive Visualization**: Smooth 60fps chart interactions
- **Scalable**: Handles thousands of training examples
- **Memory Efficient**: Optimized for browser environments


## 🎯 Educational Value

Perfect for learning:
- Machine learning fundamentals
- Feature engineering techniques
- Data visualization principles
- Vanilla JavaScript development
- HTML5 Canvas manipulation

**Note on Model Performance**: The classifier achieves approximately **40.85% accuracy**, which demonstrates an important trade-off in machine learning. Only height and width features are extracted from the drawings to enable visualization in a 2D chart. While this limitation reduces classification accuracy, it provides valuable educational insights into how feature selection impacts model performance and allows for intuitive visualization of the decision space.

---

**Built with ❤️ using pure vanilla JavaScript - no libraries, no frameworks, just code!**
