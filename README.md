# template
template.js

example: 
<div id="container"></div>

<script id="test" type="text/html">
  {{each data}}
   <p>{{data.name}}</p>
   <p>{{ getAge(data) }}</p>
  {{/each}}
</script>

<script>
  var data = [
    {
      name: 'sun',
      age: 18
    },
    {
      name: 'mon',
      age: 19
    }
  ];
  
  template.helper('getAge', function(data){
    return data.age;
  });
  
  var htmlStr = template('test', {data: data});
  
  document.getElementById('container').innerHTML = htmlStr;
</script>

参考文档：https://www.cnblogs.com/shiyou00/p/6841801.html
