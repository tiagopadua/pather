# pather

Javascript library to generate/calculate linear 2d trajectories / paths


# How to use

First include the script

    <script src="js/pather.min.js" type="text/javascript"></script>

If you are using the cubic path, you need the [Sylvester](http://sylvester.jcoglan.com/) js library to calculate the equations system using matrices.

    <script src="js/sylvester.min.js" type="text/javascript"></script>


Then create a new object passing the start and end points [x, y] you want to make the trajectory.

    var point1 = { x: 0, y: 0 };
    var point2 = { x: 50, y: 100 };
    var myPath = new Path(point1.x, point1.y, point2.x, point2.y, 'bezier');


Now you can get the 'y' value given any 'x' input, like this:

    var y = myPath.getValue(13.5);

