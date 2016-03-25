# Methods For Array Summary in JavaScript
Here is the summary of methods for array, which are used frequently. 

<table>
  <tbody>
    <tr>
      <th>Num</th>
      <th align="center">Methods</th>
      <th align="center">Examples</th>
      <th align="center">Links(Mozilla)</th>
    </tr>
    <tr>
      <td align="center">1</td>
      <td align="center">.filter()</td>
      <td align="left">
       <code>
        function isPositive(value) {
          return  value > 0; 
        }
        var filtered = [-1, 1, 0].filter(isPositive);
        //filtered is [1]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter">Link</a>
      </td>
    </tr>
    <tr>
      <td align="center">2</td>
      <td align="center">.concat()</td>
      <td align="left">
       <code>
        var alpha = ['a', 'b', 'c'], numeric = [1, 2, 3]; 
        var alphaNumeric = alpha.concat(numeric); console.log(alphaNumeric);
        // Result: ['a', 'b', 'c', 1, 2, 3]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat">Link</a>
      </td>
    </tr>
    <tr>
      <td align="center">3</td>
      <td align="center">.every()</td>
      <td align="left">
       <code>
        function isBigEnough(element, index, array) { 
          return element >= 10; 
        } 
        [12, 5, 8, 130, 44].every(isBigEnough); // false 
        [12, 54, 18, 130, 44].every(isBigEnough); // true
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every">Link</a>
      </td>
    </tr>
    <tr>
      <td align="center">4</td>
      <td align="center">.forEach()</td>
      <td align="left">
       <code>
        function Counter() { 
          this.sum = 0; 
          this.count = 0; 
        } 
        
        Counter.prototype.add = function(array) {
          array.forEach(function(entry) {
            This.sum += entry;
            ++ this.count;
          })
        };
        
        var  obj = new Counter();
        obj.add([1, 2, 3]);
        obj.sum //6
        obj.count //3
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach">Link</a>
      </td>      
    </tr>
  </tbody>
</table>
