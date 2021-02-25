---
layout: layouts/home.njk
title: Practical 1
templateClass: tmpl-home
eleventyNavigation:
  key: Practical1
  parent: Javascript
  order: 3
---

<h1> Tasks for practical 1</h1>

<p>Open console to see results</p>

<script>
    function percentage(number, percentage){
        return number * percentage / 100.0;
    }

    function drinkOrder(size,drink){
        var mediumPrice = 2.80;
        var price;
        var strMessage = 'You have ordered a ';
        var strError = '';
        switch (size) {
            case 'small': 
                price = 1.2 * mediumPrice;
                break;
            case 'medium':
                price = mediumPrice;
                break;
            case'large': 
                price = 0.8 * mediumPrice;
                break;
            default:
                strError += "The value for size is not valid. It should be one of small, medium, large";
                break;
        }
        strMessage += size + ' ';

        switch (drink){
            case 'cola':
                strMessage += ' Cola ';
            break;
            case 'lemon':
                strMessage += ' Lemonade ';
            break;
            case 'orange':
                strMessage += ' Orangeade ';
            break;
            default:
                strError += 'You have ordered a drink we don\'t sell';
            break;
        }

        /*if (size != 'large' && size != 'medium' && size != 'small'){
            strError = 'You have ordered a drink we don\'t sell';
        }*/

        if (strError)
            return strError;
        else
            return strMessage + 'which costs £' + price.toFixed(2);
    }

    function calculator(number1, number2, operator){
        let blnValidation = true;
        let strMessage = '';
        var sum;
        if (isNaN(number1)) {
            blnValidation = false;
            strMessage += 'First argument must be a number. ';
        }
        if (isNaN(number2)) {
            blnValidation = false;
            strMessage += 'Second argument must be a number. ';
        }

        if (blnValidation){
            switch (operator) {
                case '%':
                    sum = number1 % number2;
                break;
                case '/':
                    sum = number1 / number2;
                break;
                case '*':
                    sum = number1 * number2;
                break;
                case '+':
                    sum = number1 + number2;
                break;
                case '-':
                    sum = number1 - number2;
                break;
                default:
                    blnValidation = false;
                    strMessage += 'Third argument must be a valid operatior. ';
            }
            strMessage = number1 + ' ' + operator + ' ' + number2 + ' ' + '=' + ' ' + sum;
        }
        return strMessage + '\n\n';
    }

    function triangle(number){
        if (isNaN(number))
            return 'the argumnet to triangle should be a number';
        return number * (number + 1) / 2;
    }

    function factorial(number) {
        if (isNaN(number))
            return 'the argumnet to factorial should be a number';
        else if (number == 1)
            return 1;
        else
            return number * factorial(number - 1)
    }

    /* calculate the number of balls need to make a tetrahedron of side length number
        This works out as the sum of the triangle numbers because each time, you add a layer that is a triangle.*/
    function pyramid(number){
        if (isNaN(number))
            return 'the argumnet to pyramid should be a number';
        else return number * (number + 1) * (number + 2) / 6;
    }

    console.log('------task 1 ------');
    console.log(percentage(20,5));
    console.log(percentage(100,50));
    console.log(percentage(60,20));
    console.log(percentage(75,5));
    console.log('--------end task 1 ------\n\n');

    console.log('------task 2 ------');
    let order1 = drinkOrder('small','cola');
    let order2 = drinkOrder('medium','lemon');
    let order3 = drinkOrder('large','orange');
    let order4 = drinkOrder('alex','lemon');
    let order5 = drinkOrder('large','alex');

    console.log(order1);
    console.log(order2);
    console.log(order3);
    console.log(order4);
    console.log(order5);

    console.log('------ end task 2 ------\n\n'); 

    console.log('------ end task 3 ------');
    console.log(calculator('alex','alex','alex'));
    console.log(calculator('alex',10,'alex'));
    console.log(calculator(3,6,'+'));
    console.log(calculator(100,10,'+'));
    console.log(calculator(100,10,'-'));
    console.log(calculator(100,10,'*'));
    console.log(calculator(100,10,'/'));
    console.log(calculator(100,10,'%'));
    console.log('------task 3 ------\n');
</script>