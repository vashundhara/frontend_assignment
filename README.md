📘 Project Overview

This repository contains solutions for two different tasks:

DSA Problem – Second Largest Unique Number (Java)

Frontend Task – User Directory App (HTML/CSS/JS)

Both sections include explanations, approaches, and sample outputs.

🧮 DSA Problem: Second Largest Unique Number (Java)
✅ Problem Statement

Given an array of integers, return the second largest UNIQUE number.
If it doesn't exist, return -1.

Example
Input	Output
[3, 5, 2, 5, 6, 6, 1]	5
[7, 7, 7]	-1
✅ Approach (O(n) Time — O(1) Space)

Traverse the array and track unique values using a HashSet.

Find the largest and second largest unique numbers.

Handle duplicates correctly.

Return -1 if no second largest exists.

✅ Java Code
public class SecondLargestUnique {

    public static int findSecondLargestUnique(int[] arr) {
        if (arr == null || arr.length == 0) return -1;

        Integer largest = null;
        Integer secondLargest = null;

        java.util.HashSet<Integer> seen = new java.util.HashSet<>();

        for (int num : arr) {
            seen.add(num);
        }

        for (int num : seen) {
            if (largest == null || num > largest) {
                secondLargest = largest;
                largest = num;
            } else if ((secondLargest == null || num > secondLargest) && num != largest) {
                secondLargest = num;
            }
        }

        return secondLargest == null ? -1 : secondLargest;
    }

    public static void main(String[] args) {
        int[] input1 = {3, 5, 2, 5, 6, 6, 1};
        int[] input2 = {7, 7, 7};

        System.out.println("Output 1: " + findSecondLargestUnique(input1)); 
        System.out.println("Output 2: " + findSecondLargestUnique(input2));
    }
}

🎨 Frontend Task: User Directory App

This section describes the frontend UI assignment you worked on previously.

📌 Project Description

A simple User Directory Web App that allows users to:

Add new users

Display user details

Maintain user information visually

Navigate the app smoothly with a clean UI

🛠️ Tech Stack

HTML5

CSS3

JavaScript

Responsive Design

📁 Project Structure
/frontend_task_complete
│── index.html
│── styles.css
│── script.js
│── assets/
│── README.md

✨ Features
✔ Add User

Form to add new user details.

✔ Display User List

Users appear in a structured list/grid.

✔ Client-side Validation

Ensures valid user input.

✔ CSS Styling

Includes navigation bar, form design, grid layout, and spacing for clean UI.

📸 Screenshots

(Add screenshots here once uploaded)

🚀 How to Run the Project

Clone the repository:

git clone https://github.com/your-username/user_directory_app.git


Open the project folder.

Run the app by opening index.html in your browser.

📝 Author

Vasundhara Gour
Java | Spring Boot | Frontend | DSA
(You can add social links here)

⭐ Contribute

Feel free to open issues or submit PRs.
