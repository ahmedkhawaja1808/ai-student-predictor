# AI Smart Student Predictor
# Uses Linear Regression from sklearn

from sklearn.linear_model import LinearRegression
import numpy as np

# Training data (hours studied vs result)
# 0 = Fail, 1 = Pass
hours = np.array([1, 2, 3, 4, 5, 6]).reshape(-1, 1)
results = np.array([0, 0, 0, 1, 1, 1])

# Train model
model = LinearRegression()
model.fit(hours, results)

def predict_result():
    h = float(input("Enter study hours: "))
    prediction = model.predict([[h]])

    if prediction[0] >= 0.5:
        print("✅ Prediction: PASS\n")
    else:
        print("❌ Prediction: FAIL\n")

while True:
    print("=== AI Student Predictor ===")
    print("1. Predict Result")
    print("2. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        predict_result()
    elif choice == "2":
        print("Goodbye!")
        break
    else:
        print("Invalid choice\n")
