# Hacker-Rank-Simple-array-Sum
Given an array of integers, find the sum of its elements.  Input Format  The first line contains an integer, 

denoting the size of the array.  The second line contains  space-separated integers representing the array's elements. 

Output Format  Print the sum of the array's elements as a single integer.  Sample Input  6 1 2 3 4 10 11 Sample Output  

31 Explanation  We print the sum of the array's elements: .

JavaScript


            process.stdin.resume();
            process.stdin.setEncoding('ascii');

            var input_stdin = "";
            var input_stdin_array = "";
            var input_currentline = 0;

            process.stdin.on('data', function (data) {
                 input_stdin += data;
            });

            process.stdin.on('end', function () {
                input_stdin_array = input_stdin.split("\n");
                main();    
            });

            function readLine() {
                return input_stdin_array[input_currentline++];
            }

            /////////////// ignore above this line ////////////////////

            function main() {
                var n = parseInt(readLine());
                arr = readLine().split(' ');
                arr = arr.map(Number);
                var sum = arr.reduce(function(previousValue, currentValue, currentIndex, array) {
                return previousValue + currentValue;
            });
             console.log(sum);

        }  


C

            #include <math.h>
            #include <stdio.h>
            #include <string.h>
            #include <stdlib.h>
            #include <assert.h>
            #include <limits.h>
            #include <stdbool.h>

            int main(){
               int n, sum = 0;
             //printf("Enter the length of array");
              scanf("%d", &n);
              int arr[n];
              //printf("Enter the values of array one by one");
              for(int arr_i = 0; arr_i < n; arr_i++){
               scanf("%d",&arr[arr_i]);
            }
            for(int arr_i = 0; arr_i < n; arr_i++){
              sum = sum + arr[arr_i];
            }

            printf("%d", sum);

            }


PHP

            <?php
            $handle = fopen ("php://stdin","r");
            fscanf($handle,"%d",$n);
            $arr_temp = fgets($handle);
            $arr = explode(" ",$arr_temp);
            array_walk($arr,'intval');
            ?>
