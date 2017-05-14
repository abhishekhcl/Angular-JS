<!doctype html>
<html ng-app='myApp'>
 <head>
 <title>ng-include directives in AngularJS</title>
 <link href="style.css" rel='stylesheet' type='text/css'>
 <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.6/angular.min.js" type='text/javascript'></script>
 <script src='controller.js' type='text/javascript'></script>
 </head>
 <body ng-controller="myController"> 
 
 <table border='1'>
 <tr >
 <th ng-click='sortColumn("userId")' ng-class='sortClass("userId")'>S.no</th>
 <th ng-click='sortColumn("id")' ng-class='sortClass("id")'>Name</th>
 <th ng-click='sortColumn("title")' ng-class='sortClass("title")'>Age</th>
 <th ng-click='sortColumn("body")' ng-class='sortClass("body")'>Gender</th>
 </tr>
 <tr ng-repeat='friend in friends|orderBy:column:reverse'>
 <td width='20%' align='center'>{{user.userId}}</td>
 <td width='35%' align='center'>{{user.id}}</td>
 <td width='20%' align='center'>{{user.title}}</td>
 <td width='25%' align='center'>{{user.body}}</td>
 </tr>
 </table>
 
 </body>
</html>
