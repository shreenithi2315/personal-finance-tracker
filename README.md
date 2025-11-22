
# Smart Indian Finance Analytics

Personal finance categorization system built from scratch to process Indian bank transactions with intelligent pattern recognition.

## What I Built

A hybrid categorization system that automatically classifies Indian banking transactions using:
- Exact pattern matching for Indian brands (Swiggy, Amazon, Flipkart, etc.)
- Amount-based logic for UPI transactions  
- Mode-based categorization (ATM, NEFT, UPI, etc.)
- Confidence scoring for transparent decision making

## My Results

- **509 real transactions** processed from Kaggle dataset
- **84.3% automatic categorization** accuracy (429/509 transactions)
- Confidence scores from 0.5 to 0.95 for each decision
- Indian-specific transaction handling (UPI, NEFT, IMPS, ATM)

## How It Works - My Approach

### Data Processing
1. Standardized raw Kaggle data to consistent format
2. Handled missing values and data type conversions
3. Created transaction IDs and proper date formatting

### Smart Categorization Logic
1. **Level 1**: Exact brand matching (Swiggy → Food, Amazon → Shopping)
2. **Level 2**: Amount-based UPI categorization
   - < ₹200: Personal Transfer
   - ₹200-800: Shopping  
   - ₹800-3000: Major Expense
   - > ₹3000: Large Transfer
3. **Level 3**: Mode-based fallback (ATM → Cash Withdrawal)

### Confidence System
Each categorization decision includes a confidence score (0.0-1.0) showing how certain the system is about the classification.

## Technical Implementation

- **Python** with Pandas for data processing
- **Streamlit** for dashboard interface
- **Rule-based logic** I designed and implemented
- **Real Kaggle dataset** instead of generated data

## Files Included

- `smart_categorized_with_confidence.csv` - Final categorized data with confidence scores
- `Bank_data_analysis.ipynb` - Jupyter notebook with my analysis
- `dashboard.py` - Streamlit dashboard for visualization

## Next Steps

- Anomaly detection for unusual spending patterns
- Expense forecasting using time series analysis
- Mobile app interface development
