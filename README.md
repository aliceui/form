# form

---

通用表单样式。

---

## 演示

> 演示中引用了 ui-button 和 ui-tiptext 。

````iframe:1000
<link type="text/css" rel="stylesheet" media="screen" href="http://modules.spmjs.org/alice/button/1.0.0/button.css">
<link type="text/css" rel="stylesheet" media="screen" href="http://modules.spmjs.org/alice/tiptext/1.0.0/tiptext.css">
<link type="text/css" rel="stylesheet" media="screen" href="src/form.css">
<link type="text/css" rel="stylesheet" media="screen" href="src/input.css">
<link type="text/css" rel="stylesheet" media="screen" href="src/label.css">

<form class="ui-form" name="" method="post" action="#" id="">
    <fieldset>
        <legend>表单标题</legend>
         
        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本：</label>
            <p class="ui-form-text">一个个文字文字
        </div>

        <div class="ui-form-item">
            <label for="" class="ui-label">表单项文本：</label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">添加备注</a></span>
            <p class="ui-form-explain">默认文案。</p>
        </div>

        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本：</label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">表单项其他</a></span>
            <p class="ui-form-explain ui-tiptext ui-tiptext-error">
                <i class="ui-tiptext-icon iconfont" title="出错">&#x006B;</i>此在DOM上保存属性值，请使用data-xxx的形式。
            </p>
        </div>
              
        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本：</label>
            <textarea class="ui-textarea">一二三四五六七八九十</textarea>
            <p class="ui-form-explain ui-tiptext ui-tiptext-error">
                <i class="ui-tiptext-icon iconfont" title="出错">&#x006B;</i>出错文案，含英语字母或数字，如 a,b,c,A,B,C,1,2,3。
            </p>
        </div>
         
        <div class="ui-form-item ui-form-item-success">
            <label class="ui-label" for="">表单项文本：</label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">表单项其他</a></span>
            <p class="ui-form-explain ui-tiptext ui-tiptext-success">
                <i class="ui-tiptext-icon iconfont" title="出错">&#x00EF;</i>成功文案。
            </p>
        </div>
         
        <div class="ui-form-item">
            <label for="" class="ui-label">下拉选择：</label>
            <select id="province" name="province">
                <option value="">
                请选择
                </option>
                <option value="北京">
                北京
                </option>
                <option value="上海">
                上海
                </option>
                <option value="天津">
                天津
                </option>
                <option value="浙江">
                浙江
                </option>
            </select>
            <p class="ui-form-explain">更多地区即将开通，敬请期待。</p>
        </div>
          
        <div class="ui-form-item">
            <label for="" class="ui-label ui-label-reset">不可用input：</label>
            <input class="ui-input ui-input-disable" type="text" disabled>       
            <p class="ui-form-explain">目前不可用</p>
        </div>
         
        <div class="ui-form-item">
            <label for="" class="ui-label">验证码：</label>
            <input class="ui-input ui-input-checkcode" type="text" data-explain="请输入右图中字符，不区分大小写。" maxlength="4" autocomplete="off" value="" name="fourcode">
            <img class="ui-checkcode-imgcode-img" align="absMiddle" alt="请输入您看到的内容" src="https://omeo.alipay.com/service/checkcode?sessionID=82012ab6b1f4ed9e675fb9092a25cb3b&r=0.9321065918075809"  title="点击刷新图片校验码">
            <a href="#">看不清，换一张</a>
            <div class="ui-form-explain">请输入右图中字符，不区分大小写。</div>
        </div>
 
        <div class="ui-form-item">
            <input id="test" value="" type="checkbox"> <label for="test">我已阅读并接受自主缴费服务协议</label>
        </div>
 
        <div class="ui-form-item">
            <input type="submit" class="ui-button ui-button-morange" value="确定">
            <input type="button" class="ui-button ui-button-mwhite" value="取消">
        </div>   
    </fieldset>
</form> <!-- .ui-form -->
````
