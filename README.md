#  Summary of Methods of Array in JavaScript
Here is the summary of methods for array used frequently for the purpose of your reference and comparison among each of them. 

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
    <tr>
      <td align="center">12</td>
      <td align="center">.slice()</td>
      <td align="left">
       <code>
        var fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango'];
        var citrus = fruits.slice(1, 3);
    
        // citrus contains ['Orange','Lemon']
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">13</td>
      <td align="center">.some()</td>
      <td align="left">
       <code>
        function isBiggerThan10(element, index, array) {
          return element > 10;
        }
        [2, 5, 8, 1, 4].some(isBiggerThan10);  // false
        [12, 5, 8, 1, 4].some(isBiggerThan10); // true
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some">Link</a>
      </td>      
    </tr> 
    <tr>
      <td align="center">14</td>
      <td align="center">.sort()</td>
      <td align="left">
       <code>
        var numbers = [4, 2, 5, 1, 3];
        numbers.sort(function(a, b) {
          return a - b;
        });
        console.log(numbers);
        // [1, 2, 3, 4, 5]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort">Link</a>
      </td>      
    </tr>  
    <tr>
      <td align="center">15</td>
      <td align="center">.splice()</td>
      <td align="left">
       <code>
        var myFish = ['angel', 'clown', 'mandarin', 'surgeon'];
        
        // removes 0 elements from index 2, and inserts 'drum'
        var removed = myFish.splice(2, 0, 'drum');
        // myFish is ['angel', 'clown', 'drum', 'mandarin', 'surgeon']
        // removed is [], no elements removed
        
        // myFish is ['angel', 'clown', 'drum', 'mandarin', 'surgeon'] 
        // removes 1 element from index 3
        removed = myFish.splice(3, 1);
        // myFish is ['angel', 'clown', 'drum', 'surgeon']
        // removed is ['mandarin']
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice">Link</a>
      </td>      
    </tr>
    <tr>
      <td align="center">16</td>
      <td align="center">.unshift()</td>
      <td align="left">
       <code>
          var arr = [1, 2];
          
          arr.unshift(0); // result of call is 3, the new array length
          // arr is [0, 1, 2]
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift">Link</a>
      </td>      
    </tr>
    <tr>
      <td align="center">17</td>
      <td align="center">.join()</td>
      <td align="left">
       <code>
          var a = ['Wind', 'Rain', 'Fire'];
          var myVar2 = a.join(', ');  // assigns 'Wind, Rain, Fire' to myVar2

       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join">Link</a>
      </td>      
    </tr>
    <tr>
      <td align="center">18</td>
      <td align="center">.find()</td>
      <td align="left">
       <code>
        function isPrime(element, index, array) {
          var start = 2;
          while(start <= Marth.sqrt(element)) {
            if (element % start++ < 1) {
              return false;
            }
          }
          return element > 1;
        }
        console.log([4, 6, 8, 12].find(isPrime));
       </code>
      </td>
      <td>
       <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join">Link</a>
      </td>      
    </tr> 
  </tbody>
</table>
