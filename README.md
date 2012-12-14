forEachSync
===========

带游标的数组同步forEach,执行完一个才会执行下一个。

Examples:

var worker = require('./forEachSync');

var array = [];

for(var i = 0;i<100000;i++){

  array.push(i);
  
}

array.forEachSync(function(item,index,cback){

	console.log('index='+index+','+item);
  
	cback();
  
},function(){

	console.log('it is over.');
  
});
