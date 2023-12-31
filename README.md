This is a simple Python package that aims to make using linear regression easier for programmers.

You can create a simple linear regression model as following:

```
from regrez import Models

m = Models.Simple("path/to/csv", "label for column that'll be used for x axis", "label for column that'll be used for y axis")
```

After that, you can train your model using `m.Train()` and test using `m.Test(test_x, test_y)`. Alternatively, there is a function called `m.TrainAndTest()` you can use if you only want to see how accurate would the model work. It separates 20% of the data for testing, trains the model with the rest of it, tests the model with separated data and shows how accurate your model is. You can use `m.Visualize()` after training if you want to see a plot showing both data points and the line to see how relative your variables are.

You can create a multiple regression model as following:

```
from regrez import Models
m = Models.Multiple("path/to/csv", ["X Label 1", "X Label 2", "X Label 3"], ["Y Label"])
```

After that, you can train your model using `m.Train()` and test using `m.Test(test_x, test_y)`. Alternatively, there is a function called `m.TrainAndTest()` you can use if you only want to see how accurate would the model work. It separates 20% of the data for testing, trains the model with the rest of it, tests the model with separated data and shows how accurate your model is. There is no `m.Visualize()` for multiple linear regression models.
