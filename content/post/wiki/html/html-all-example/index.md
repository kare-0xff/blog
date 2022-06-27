---
title: "（三）HTML常用标签之综合案例"
date: 2021-06-28T16:44:57+08:00
slug: html-all-example
image: html.png
draft: false
tags: [html]
categories: html
---

# （三）HTML常用标签之综合案例

## Html常用标签综合案例

```html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=<>, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h4>青春不常在，抓紧谈恋爱</h4><br>
    <table width="500">
        <tr>
            <td>
                性别:</td>
            <td>
                <input type="radio" name="sex" id="man"><img src="images/男.png" width="16"><label for="man">男</label>
                <input type="radio" name="sex" id="woman"><img src="images/女.png" width="16"><label for="woman">女</label><br>
            </td>
        </tr>
            <td>
                生日:
            </td>
            <td>
                <select>
                    <option>1985</option>
                    <option>1986</option>
                    <option>1987</option>
                    <option>1988</option>
                    <option>1989</option>
                    <option>1990</option>
                    <option selected="selected">-请选择年-</option>
                </select>
                <select>
                    <option>01</option>
                    <option>02</option>
                    <option>03</option>
                    <option>04</option>
                    <option>05</option>
                    <option>06</option>
                    <option selected="selected">-请选择月-</option>
                </select>
                <select>
                    <option>01</option>
                    <option>02</option>
                    <option>03</option>
                    <option>04</option>
                    <option>05</option>
                    <option>06</option>
                    <option selected="selected">-请选择日-</option>
                </select><br>
            </td>
        </tr>
        <!-- 第三行 -->
        <tr>
            <td>
                <label for="dq">所在地区:</label>
            </td>
            <td>
                <input type="text" name="adress" id="dq"><br>
            </td>
        </tr>
        <!-- 第四行 -->
        <tr>
            <td>
                婚姻状况
            </td>
            <td>
                <input type="radio" name="marry" id="m"><label for="m">未婚</label>

                <input type="radio" name="marry" id="li"><label for="li">离婚</label></label><br>
            </td>
        </tr>
        <!-- 第五行 -->
        <tr>
            <td>
                <label for="degree">学历</label>
            </td>
            <td>
                <input type="text" name="de" id="degree"></label><br>
            </td>
        </tr>
        <!-- 第六行 -->
        <tr>
            <td>
                喜欢的类型
            </td>
            <td>
                <input type="radio" name="kind" id="k"><label for="k">可爱的</label>
                <input type="radio" name="kind" id="k"><label for="k">可爱的</label>
                <input type="radio" name="kind" id="ki"><label for="ki">妩媚的</label>
                <input type="radio" name="kind" id="xiao"><label for="xiao">小鲜肉</label>
                <input type="radio" name="kind" id="lao"><label for="lao">老腊肉</label>
                <input type="radio" name="kind" id="all"><label for="all">都喜欢</label><br>
            </td>
        </tr>
        <tr>
            <td>
                自我介绍
            </td>
            <td>
                <textarea cols="50" rows="5"> 
                    自我介绍
                </textarea><br>
            </td>
        </tr>
        <tr>
            <td></td>
            <td>
                <input type="submit" value="免费注册"><br>
            </td>
        </tr>
        <tr>
            <td></td>
            <td>
                <input type="checkbox" checked="checked" >我同意服务条款<br>
            </td>
        </tr>
        <tr>
            <td></td>
            <td>
                <a href="#">我是会员，立即登录</a><br>
            </td>
        </tr>
        <tr>
            <td></td>
            <td>
                <h4>我承诺</h4>
                <ul>
                    <li>年满18，单身</li>
                    <li>抱着严肃的态度</li>
                    <li>真诚寻找另一半</li>
                </ul>
            </td>
        </tr>
    </table>
    <form > 

    </form>
</body>
</html>
```

