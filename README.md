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
    <tr>
      <td align="center">5</td>
      <td align="center">.map()</td>
      <td align="left">
       <code>
        var numbers = [1, 4, 9]; 
        var roots = numbers.map(Math.sqrt);
         // roots is now [1, 2, 3], numbers is still [1, 4, 9]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map">Link</a>
      </td>      
    </tr>
    <tr>
      <td align="center">6</td>
      <td align="center">.pop()</td>
      <td align="left">
       <code>
        var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
        
        var popped = myFish.pop();
        
        console.log(myFish); // ['angel', 'clown', 'mandarin' ] 
        
        console.log(popped); // 'sturgeon'
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop">Link</a>
      </td>      
    </tr>  
    <tr>
      <td align="center">7</td>
      <td align="center">.push()</td>
      <td align="left">
       <code>
        var sports = ['soccer', 'baseball'];
        var total = sports.push('football', 'swimming');
        
        console.log(sports); // ['soccer', 'baseball', 'football', 'swimming']
        console.log(total);  // length: 4
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">8</td>
      <td align="center">.reduce()</td>
      <td align="left">
       <code>
        var total = [0, 1, 2, 3].reduce(function(a, b) {
        return a + b;
        });
        // total == 6
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">9</td>
      <td align="center">.reduceRight()</td>
      <td align="left">
       <code>
        var flattened = [[0, 1], [2, 3], [4, 5]].reduceRight(function(a, b) {
            return a.concat(b);
        }, []);
        // flattened is [4, 5, 2, 3, 0, 1]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/ReduceRight">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">10</td>
      <td align="center">.reverse()</td>
      <td align="left">
       <code>
        var myArray = ['one', 'two', 'three'];
        myArray.reverse(); 
        
        console.log(myArray) // ['three', 'two', 'one']
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">11</td>
      <td align="center">.shift()</td>
      <td align="left">
       <code>
        var myFish = ['angel', 'clown', 'mandarin', 'surgeon'];
        
        console.log('myFish before: ' + myFish);
        // "myFish before: angel,clown,mandarin,surgeon"
        
        var shifted = myFish.shift(); 
        
        console.log('myFish after: ' + myFish); 
        // "myFish after: clown,mandarin,surgeon" 
        
        console.log('Removed this element: ' + shifted); 
        // "Removed this element: angel"
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift">Link</a>
      </td>      
    </tr>    
  </tbody>
</table>
