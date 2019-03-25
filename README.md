function rot13(str) { 
  let cypherArr = []
  cypherArr = str.split('')
  cypherArr =  cypherArr.map(char=>{
    if(char.toLowerCase()!=char.toUpperCase()){
      let initiaNum = char.charCodeAt(0)
      let newNum = initiaNum+13
      if(newNum>90){
        newNum-=26
      }
      return String.fromCharCode(newNum);
    }else{
      return char
    }
  })
  return cypherArr.join('');
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
