# Multimodal Student Engagement Detection System
# Quick Start Guide and Usage Instructions

## Overview
This system detects student engagement levels using multimodal AI that combines:
- **Visual features**: Facial expressions, head pose, eye gaze
- **Behavioral features**: Click patterns, scrolling, interaction metrics  
- **Audio features**: Speech prosody and tone analysis

## Quick Start in Google Colab

### 1. Upload Files
Upload these files to your Colab environment:
- `enhanced_engagement_detection.py`
- `requirements.txt` 
- `high_quality_engagement_dataset.zip` (your dataset)

### 2. Install Dependencies
```python
!pip install -r requirements.txt
```

### 3. Run the System
```python
# Import and run the enhanced system
exec(open('enhanced_engagement_detection.py').read())
```

The system will:
1. ✅ Automatically load your dataset
2. 🚀 Train the multimodal model  
3. 📊 Generate evaluation metrics and plots
4. 💾 Save trained model and results

## Expected Results
- **High Accuracy**: 80-95% (vs 18% with random data)
- **Clear Class Separation**: Confusion matrix with diagonal pattern
- **Strong ROC Curves**: AUC scores > 0.8 for all classes
- **Comprehensive Metrics**: Precision, Recall, F1-scores per class

## Output Files
All results saved in `evaluation_results/`:
- `confusion_matrix.png` - Classification confusion matrix
- `classification_metrics.png` - Precision/Recall/F1 bar charts  
- `roc_curves.png` - ROC curves for all engagement levels
- `training_history.png` - Loss and accuracy over epochs
- `performance_report.json` - Numerical performance metrics
- `multimodal_engagement_model.h5` - Trained model weights

## Real-time Usage
After training, use the system for live engagement detection:

```python
# Initialize the full system
system = EngagementDetectionSystem()

# Sample session data
session_data = {
    'login_duration': 3600,
    'total_clicks': 45, 
    'scroll_events': 23,
    'pause_events': 5,
    'quiz_attempts': 3,
    'time_on_task': 2700
}

# Start real-time webcam detection
system.real_time_detection(session_data)
```

## Key Features
- 🎯 **Attention-based fusion** of multiple modalities
- 🔄 **Early stopping** and learning rate scheduling  
- 📈 **Comprehensive evaluation** with multiple metrics
- 🎨 **Professional visualizations** for all results
- 💪 **Robust architecture** with dropout and regularization
- 🚀 **Real-time capable** for live engagement monitoring

## Model Architecture
- **Visual pathway**: 170D → 128 → 64 neurons
- **Behavioral pathway**: 8D → 32 → 16 neurons  
- **Audio pathway**: 20D → 64 → 32 neurons
- **Fusion layer**: Concatenation → 128 → 64 → 5 classes
- **Regularization**: Dropout (0.3-0.4) + Early stopping

## Troubleshooting
- **Dataset not found**: Ensure `high_quality_engagement_dataset.zip` is uploaded
- **Low accuracy**: Check dataset quality and increase training epochs
- **Memory issues**: Reduce batch size from 64 to 32
- **Colab timeouts**: Save model checkpoints during training

## Customization
- **Change engagement levels**: Modify `self.class_names` list
- **Adjust model size**: Change Dense layer dimensions
- **Add new modalities**: Extend fusion architecture  
- **Tune hyperparameters**: Modify learning rate, dropout, epochs

## Citation
Based on research: "AI-Driven Multimodal Framework for Student Engagement Detection in Sustainable Distance Learning: Models and Green AI Perspectives"

---
Ready to achieve **maximum accuracy** with your engagement detection system!
