# identity_card
验证中国居民身份证号码

#
// 验证身份证号码是否正确
// var p = /^[1-9]\d{5}(18|19|20)\d{2}((0[1-9])|(1[0-2]))(([0-2][1-9])|10|20|30|31)\d{3}[0-9Xx]$/;
// //输出 true
// console.log(p.test("11010519491231002X"));
// //输出 false 不能以0开头
// console.log(p.test("01010519491231002X"));
// //输出 false 年份不能以17开头
// console.log(p.test("11010517491231002X"));
// //输出 false 月份不能为13
// console.log(p.test("11010519491331002X"));
// //输出 false 日期不能为32
// console.log(p.test("11010519491232002X"));
// //输出 false 不能以a结尾
// console.log(p.test("11010519491232002a"));
function verificate($str) 
{
	//
	$reg = "/^[1-9]\d{5}(18|19|20)\d{2}((0[1-9])|(1[0-2]))(([0-2][1-9])|10|20|30|31)\d{3}[0-9Xx]$/";
  $status = preg_match($reg, $str);

  //
  return $status > 0 ? true : false;
}
