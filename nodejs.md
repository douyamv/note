#nodejs解析json字符
    var obj = {  
        "name": "LiLi", 
        "age": 22,  
        "sex": "F"  
    }; 
     
    var str = JSON.stringify(obj); 
    console.log(str); 
     
    var obj2 = JSON.parse(str); 
    console.log(obj2); 
