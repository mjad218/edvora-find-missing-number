const A = [1, 2, 3, 6, 8, 9, 10, 15, 20, 30, 40, 50];
// 4 
// at index 3
// 
const findMissingNumbers = (arr) => {
    let missingNumbers = [];
    // lets assume its already sorted
    for(let i = 0; i < arr.length ; i++) {
        if(i === arr.length - 1) {
            continue;
        }
        if(arr[i] === (arr[i + 1] - 1) ) {
            continue;
        } else {
            let num = arr[i] + 1;
            while(num !== arr[i + 1]) {
                missingNumbers.push(num++);
            }
        }
    }
    return missingNumbers;
}

// const result = findMissingNumbers(A);
console.log(findMissingNumbers(A)); 