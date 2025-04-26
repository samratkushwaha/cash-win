# cash-win
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Color Prediction</title> 
    <link rel="stylesheet" href="styles.css"> 
</head> 
<body> 
    <h1>Color Prediction</h1> 
    <div id="color-picker"> 
        <input type="color" id="colorInput"> 
        <button id="predictBtn">Predict Color</button> 
    </div> 
    <div id="predictionResult"></div> 
    <script src="script.js"></script> 
</body> 
</html> 
CSS (styles.css)

body { 
    font-family: Arial, sans-serif; 
    text-align: center; 
    padding: 50px; 
    background-color: #f9f9f9; 
} 
 
#color-picker { 
    margin-bottom: 20px; 
} 
JavaScript (script.js)

document.getElementById('predictBtn').addEventListener('click', function() { 
    const color = document.getElementById('colorInput').value; 
    const prediction = predictColor(color); 
    document.getElementById('predictionResult').innerText = `Predicted Color: ${prediction}`; 
}); 
 
function predictColor(color) { 
    // Simple prediction logic (you can improve this) 
    return color === '#ff0000' ? 'Hot Color' : 'Cool Color'; 
} 
