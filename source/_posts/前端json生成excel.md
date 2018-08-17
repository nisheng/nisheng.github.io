---
layout: '[layout]'
title: js生成excel并导出
date: 2018-08-10 14:29:00
tags: 代码
---
>代码
   ```
   <!doctype html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport"
             content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
       <meta http-equiv="X-UA-Compatible" content="ie=edge">
       <title>Document</title>
   </head>
   <body>
   <script>
       JSONToExcelConvertor(
           [
           {
               "id": 13148,
               "companyName": "厦门指掌天下文化传媒有限公司1",
               "contactName": "龙少",
               "contactMail": "1234567890@qq.com",
               "contactTel": "13152521217",
               "contactQQ": "123456789",
               "fundSum": "0",
               "consumeTotal": "0",
               "opName": "王灿锋",
               "opUserId": 13426
           },
               {
                   "id": 13248,
                   "companyName": "中华万年历-男性补肾",
                   "contactName": "谭经理",
                   "contactMail": "3337056311@qq.com",
                   "contactTel": "15173195628",
                   "contactQQ": "3337056311",
                   "fundSum": "0",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13249,
                   "companyName": "全民夺旗",
                   "contactName": "卓泽坚",
                   "contactMail": "zhuozj@pv.cc",
                   "contactTel": "13760847644",
                   "contactQQ": "13760847644",
                   "fundSum": "-0.25",
                   "consumeTotal": "0"
               },
               {
                   "id": 13261,
                   "companyName": "互动营销减肥户1",
                   "contactName": "彭总",
                   "contactMail": "807070024@qq.com",
                   "contactTel": "807070024",
                   "contactQQ": "807070024",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13269,
                   "companyName": "广州棒谷网络科技有限公司",
                   "contactName": "刘睿乾",
                   "contactMail": "707867811@qq.com",
                   "contactTel": "暂无",
                   "contactQQ": "1299839253",
                   "fundSum": "9.2",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13270,
                   "companyName": "快乐生活树熊网络",
                   "contactName": "刘睿乾",
                   "contactMail": "331313711@qq.com",
                   "contactTel": "暂无",
                   "contactQQ": "1299839253",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13280,
                   "companyName": "棋棋-斗地主",
                   "contactName": "豆",
                   "contactMail": "286816592@qq.com",
                   "contactTel": "1",
                   "contactQQ": "1",
                   "fundSum": "-0.24",
                   "consumeTotal": "0",
                   "opName": "卢宇",
                   "opUserId": 14076
               },
               {
                   "id": 13281,
                   "companyName": "北京每日优鲜电子商务有限公司",
                   "contactName": "李茜雯",
                   "contactMail": "lixw@missfresh.cn",
                   "contactTel": "13581576932",
                   "contactQQ": "411731961",
                   "fundSum": "-0.2",
                   "consumeTotal": "0"
               },
               {
                   "id": 13287,
                   "companyName": "绿色健康减肥",
                   "contactName": "陈总",
                   "contactMail": "460931534@qq.com",
                   "contactTel": "X",
                   "contactQQ": "X",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13294,
                   "companyName": "北京狂想时代科技有限公司",
                   "contactName": "丁锟",
                   "contactMail": "7055563@qq.com",
                   "contactTel": "13255713626",
                   "contactQQ": "2653771303",
                   "fundSum": "18711.09",
                   "consumeTotal": "5850",
                   "opName": "赖珊珊",
                   "opUserId": 13938
               },
               {
                   "id": 13331,
                   "companyName": "浙江土拨鼠网络科技有限公司",
                   "contactName": "胥思虹",
                   "contactMail": "13828885773@189.com",
                   "contactTel": "13828885773",
                   "contactQQ": "1",
                   "fundSum": "-0.03",
                   "consumeTotal": "0"
               },
               {
                   "id": 13332,
                   "companyName": "大富翁斗地主",
                   "contactName": "丁锟",
                   "contactMail": "wang@qq.com",
                   "contactTel": "13255713626",
                   "contactQQ": "2653771303",
                   "fundSum": "-0.41",
                   "consumeTotal": "0",
                   "opName": "丁锟操作",
                   "opUserId": 37
               },
               {
                   "id": 13338,
                   "companyName": "广州万兔斯瑞广告有限公司-男性",
                   "contactName": "李大仁",
                   "contactMail": "1125965557@qq.com",
                   "contactTel": "1125965557",
                   "contactQQ": "1125965557",
                   "fundSum": "-0.25",
                   "consumeTotal": "0"
               },
               {
                   "id": 13339,
                   "companyName": "杭州东塑信息技术有限公司",
                   "contactName": "丁锟",
                   "contactMail": "627206812@qq.com",
                   "contactTel": "13255713626",
                   "contactQQ": "2653771303",
                   "fundSum": "-0.5",
                   "consumeTotal": "0",
                   "opName": "丁锟操作",
                   "opUserId": 37
               },
               {
                   "id": 13340,
                   "companyName": "北京诺神州科技有限公司",
                   "contactName": "Nancy",
                   "contactMail": "2558601685@qq.com",
                   "contactTel": "17082470063",
                   "contactQQ": "2558601685",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13343,
                   "companyName": "海洋渔夫",
                   "contactName": "丁锟",
                   "contactMail": "460040802@qq.com",
                   "contactTel": "13255713626",
                   "contactQQ": "2653771303",
                   "fundSum": "998.23",
                   "consumeTotal": "0",
                   "opName": "赖珊珊",
                   "opUserId": 13938
               },
               {
                   "id": 13344,
                   "companyName": "黄玉玲",
                   "contactName": "黄玉玲",
                   "contactMail": "839699501@qq.com",
                   "contactTel": "15801480542",
                   "contactQQ": "839699501",
                   "fundSum": "-0.55",
                   "consumeTotal": "0"
               },
               {
                   "id": 13365,
                   "companyName": "丰胸免费领取",
                   "contactName": "方先森",
                   "contactMail": "610479464@qq.com",
                   "contactTel": "18702000016",
                   "contactQQ": "610479464",
                   "fundSum": "-0.4",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13367,
                   "companyName": "趣网成人用品专营店",
                   "contactName": "陈福聪",
                   "contactMail": "642252541@qq.com",
                   "contactTel": "18680868864",
                   "contactQQ": "642252541",
                   "fundSum": "-38.98",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13370,
                   "companyName": "上海卫裤",
                   "contactName": "王海峰",
                   "contactMail": "16988@qq.com",
                   "contactTel": "暂无",
                   "contactQQ": "625666551",
                   "fundSum": "-0.5",
                   "consumeTotal": "0"
               },
               {
                   "id": 13371,
                   "companyName": "游酷盛世科技（北京）有限公司",
                   "contactName": "张林娟",
                   "contactMail": "2011037576@qq.com",
                   "contactTel": "15081860163",
                   "contactQQ": "2011037576",
                   "fundSum": "-0.22",
                   "consumeTotal": "0",
                   "opName": "汪康",
                   "opUserId": 13760
               },
               {
                   "id": 13374,
                   "companyName": "0808棋棋",
                   "contactName": "1",
                   "contactMail": "2761047325@qq.com",
                   "contactTel": "2",
                   "contactQQ": "3",
                   "fundSum": "1754.23",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13375,
                   "companyName": "厦门初日科技有限公司",
                   "contactName": "邓慧",
                   "contactMail": "2491843175@qq.com",
                   "contactTel": "13043047019",
                   "contactQQ": "2491843175",
                   "fundSum": "-0.03",
                   "consumeTotal": "0"
               },
               {
                   "id": 13387,
                   "companyName": "欢乐购",
                   "contactName": "林先生",
                   "contactMail": "1693330467@qq.com",
                   "contactTel": "13000000000",
                   "contactQQ": "1693330467",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13389,
                   "companyName": "夜缘觅爱",
                   "contactName": "丁锟",
                   "contactMail": "691281479@qq.com",
                   "contactTel": "13255713626",
                   "contactQQ": "2653771303",
                   "fundSum": "-0.33",
                   "consumeTotal": "0",
                   "opName": "丁锟操作",
                   "opUserId": 37
               },
               {
                   "id": 13390,
                   "companyName": "武汉金易韵健康科技有限公司",
                   "contactName": "彭小成",
                   "contactMail": "460867740@qq.com",
                   "contactTel": "17371195588",
                   "contactQQ": "460867740",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13391,
                   "companyName": "时时彩",
                   "contactName": "郑世强",
                   "contactMail": "2534699562@qq.com",
                   "contactTel": "15088622568",
                   "contactQQ": "2534699562",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13392,
                   "companyName": "豪哥捕鱼",
                   "contactName": "豪哥",
                   "contactMail": "13263156017@qq.com",
                   "contactTel": "13263156017",
                   "contactQQ": "123456",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13393,
                   "companyName": "杭州昭宁贸易有限公司",
                   "contactName": "1",
                   "contactMail": "8656@qq.com",
                   "contactTel": "18111111111",
                   "contactQQ": "1",
                   "fundSum": "0",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13394,
                   "companyName": "北京华诚东方科技有限公司",
                   "contactName": "林牧",
                   "contactMail": "victorialin0916@gmail.com",
                   "contactTel": "13000000000",
                   "contactQQ": "1693330467",
                   "fundSum": "-0.18",
                   "consumeTotal": "0"
               },
               {
                   "id": 13395,
                   "companyName": "左先生",
                   "contactName": "左先生",
                   "contactMail": "18911441405@qq.com",
                   "contactTel": "18911441405",
                   "contactQQ": "1301411566",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13396,
                   "companyName": "杭州稠城信息技术有限公司",
                   "contactName": "滑新颖",
                   "contactMail": "2166573749@qq.com",
                   "contactTel": "13158813456",
                   "contactQQ": "2166573749",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13399,
                   "companyName": "杨泽-男科",
                   "contactName": "杨泽",
                   "contactMail": "1301411566@qq.com",
                   "contactTel": "18618266932",
                   "contactQQ": "1301411566",
                   "fundSum": "-0.4",
                   "consumeTotal": "0"
               },
               {
                   "id": 13400,
                   "companyName": "深圳市拾色科技网络有限公司",
                   "contactName": "滑新颖",
                   "contactMail": "123654@qq.com",
                   "contactTel": "13232323232",
                   "contactQQ": "1123654",
                   "fundSum": "-0.14",
                   "consumeTotal": "0"
               },
               {
                   "id": 13401,
                   "companyName": "上海黑桃互动网络科技有限公司",
                   "contactName": "黄年达",
                   "contactMail": "245985552@qq.com",
                   "contactTel": "15112124921",
                   "contactQQ": "245985552",
                   "fundSum": "510.43",
                   "consumeTotal": "0",
                   "opName": "王灿锋",
                   "opUserId": 13426
               },
               {
                   "id": 13402,
                   "companyName": "兼职-王欣",
                   "contactName": "王欣",
                   "contactMail": "406121590@qq.com",
                   "contactTel": "13886095001",
                   "contactQQ": "406121590",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13408,
                   "companyName": "鑫傲龙祥(北京）投资管理有限公司",
                   "contactName": "张先生",
                   "contactMail": "2055517344@qq.com",
                   "contactTel": "18810249062",
                   "contactQQ": "2055517344",
                   "fundSum": "-0.12",
                   "consumeTotal": "0"
               },
               {
                   "id": 13409,
                   "companyName": "杭州新湖美丽洲置业有限公司",
                   "contactName": "李",
                   "contactMail": "768798765@qq.com",
                   "contactTel": "13888887777",
                   "contactQQ": "768798765",
                   "fundSum": "0",
                   "consumeTotal": "0"
               },
               {
                   "id": 13410,
                   "companyName": "棋棋--杨泽",
                   "contactName": "杨泽",
                   "contactMail": "qipai@qq.com",
                   "contactTel": "18618266932",
                   "contactQQ": "1301411566",
                   "fundSum": "-0.28",
                   "consumeTotal": "0",
                   "opName": "卢宇",
                   "opUserId": 14076
               }
               ]
       ,'财务excel')
       //json数据转excel
       function JSONToExcelConvertor(JSONData, FileName) {
           //先转化json
           var arrData = typeof JSONData != 'object' ? JSON.parse(JSONData) : JSONData;
           var excel = '<table>';
           var row = "<tr>";
           //设置表头
           var keys = Object.keys(JSONData[0]);
           // console.log(keys); //key
           keys.forEach(function (item) {
               row += "<td>" + item + '</td>';
           });
           //换行
           excel += row + "</tr>";
           //设置数据

           for (var i = 0; i < arrData.length; i++) {
               var row = "<tr>";
               for (var index in arrData[i]) {
                   // console.log(arrData[i][index]);
                   //var value = arrData[i][index] === "." ? "" : arrData[i][index];
                   row += '<td>' + arrData[i][index] + '</td>';
               }
               excel += row + "</tr>";
           }

           excel += "</table>";
           // console.log(excel)  //最终表格数据

           var excelFile = "<html xmlns:o='urn:schemas-microsoft-com:office:office' xmlns:x='urn:schemas-microsoft-com:office:excel' xmlns='http://www.w3.org/TR/REC-html40'>";
           excelFile += '<meta http-equiv="content-type" content="application/vnd.ms-excel; charset=UTF-8">';
           excelFile += '<meta http-equiv="content-type" content="application/vnd.ms-excel';
           excelFile += '; charset=UTF-8">';
           excelFile += "<head>";
           excelFile += "<!--[if gte mso 9]>";
           excelFile += "<xml>";
           excelFile += "<x:ExcelWorkbook>";
           excelFile += "<x:ExcelWorksheets>";
           excelFile += "<x:ExcelWorksheet>";
           excelFile += "<x:Name>";
           excelFile += "{worksheet}";
           excelFile += "</x:Name>";
           excelFile += "<x:WorksheetOptions>";
           excelFile += "<x:DisplayGridlines/>";
           excelFile += "</x:WorksheetOptions>";
           excelFile += "</x:ExcelWorksheet>";
           excelFile += "</x:ExcelWorksheets>";
           excelFile += "</x:ExcelWorkbook>";
           excelFile += "</xml>";
           excelFile += "<![endif]-->";
           excelFile += "</head>";
           excelFile += "<body>";
           excelFile += excel;
           excelFile += "</body>";
           excelFile += "</html>";

           // console.log(excelFile)
           var uri = 'data:application/vnd.ms-excel;charset=utf-8,' + encodeURIComponent(excelFile);

           var link = document.createElement("a");
           link.href = uri;

           link.style = "visibility:hidden";
           link.download = FileName + ".xls";

           document.body.appendChild(link);
           console.log(link);
           link.click();

           document.body.removeChild(link);
       }
   </script>



   <a href="https://blog.csdn.net/m0_37970224/article/details/79581429">原文链接：https://blog.csdn.net/m0_37970224/article/details/79581429</a>
   <!--<script>-->
       <!--//判断是否为JSON格式数据-->
       <!--function isJSON(str) {-->
           <!--try {-->
               <!--if (typeof JSON.parse(str) == "object") {-->
                   <!--return true;-->
               <!--}-->
           <!--} catch(e) {-->
           <!--}-->
           <!--return false;-->
       <!--}-->



   <!--</script>-->
   </body>
   </html>

   ```

