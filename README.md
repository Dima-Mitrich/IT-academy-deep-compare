# IT-academy-deep-compare

Дополнительное задание на глубокое сравнение;

С3+
Напишите функцию deepComp для глубокого сравнения переданных ей значений.
Значения могут быть числами, строками, хэшами, массивами, в т.ч. любого уровня вложения.
Учтите, что цикл for..in не гарантирует перебора ключей хэша в каком-либо порядке.
Не используйте Object.is().
Напишите тесты правильной работы функции, как минимум такие:
var H1={ a:5, b: { b1:6, b2:7 } };
var H2={ b: { b1:6, b2:7 }, a:5 };
var H3={ a:5, b: { b1:6 } };
var H4={ a:5, b: { b1:66, b2:7 } };
var H5={ a:5, b: { b1:6, b2:7, b3:8 } };
var H6={ a:null, b:undefined, c:Number.NaN };
var H7={ c:Number.NaN, b:undefined, a:null };
var H8={a:5,b:6};
var H9={c:5,d:6};
var H10={a:5};
var A1=[5,7];
var A2=[5,5,7];
var A3=[5,8,7];
deepComp(H1,H2) будет true
deepComp(H1,H3) будет false
deepComp(H1,H4) будет false
deepComp(H1,H5) будет false
deepComp(H6,H7) будет true
deepComp(H8,H9) будет false
deepComp(H8,H10) будет false
deepComp(null,H10) будет false
deepComp(H10,null) будет false
deepComp(null,null) будет true
deepComp(null,undefined) будет false
deepComp(5,"5") будет false
deepComp(5,H1) будет false
deepComp(A1,H1) будет false
deepComp(A2,A3) будет false
deepComp( {a:5,b:undefined}, {a:5,c:undefined} ) будет false
deepComp([5,7],{0:5,1:7}) будет false
deepComp("aaa","bbb") будет false