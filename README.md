# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.
Use JavaScript functions for dynamic behavior.
Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Animations and Local Storage</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 20px;
        }

        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        button:hover {
            background-color: #45a049;
            transform: scale(1.1);
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }

        .animate {
            animation: bounce 1s ease infinite;
        }

    </style>
</head>
<body>

    <button id="animateButton">Animate Me!</button>
    <p id="statusMessage">Welcome back! Your preferences have been loaded.</p>

    <script>
        document.getElementById('animateButton').addEventListener('click', () => {
            document.getElementById('animateButton').classList.add('animate');
            localStorage.setItem('buttonClicked', 'true');
        });

        window.onload = () => {
            if (localStorage.getItem('buttonClicked') === 'true') {
                document.getElementById('statusMessage').textContent = "Button was clicked before!";
            }
        };
    </script>

</body>
</html>

