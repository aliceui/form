# form

---

[![spm package](http://spmjs.io/badge/alice-form)](http://spmjs.io/package/alice-form)

通用表单样式。可基于此表单样式构建各类功能表单。

---

## 演示

> 演示中还引用了 [alice/button](http://aliceui.org/button) 和 [alice/tiptext](http://aliceui.org/tiptext) 。

`````html
<style>
@font-face {
    font-family: "rei";
    src: url("https://i.alipayobjects.com/common/fonts/rei.eot?20140606"); /* IE9 */
    src: url("https://i.alipayobjects.com/common/fonts/rei.eot?20140606#iefix") format("embedded-opentype"), /* IE6-IE8 */
    url("https://i.alipayobjects.com/common/fonts/rei.woff?20140606") format("woff"), /* chrome 6+、firefox 3.6+、Safari5.1+、Opera 11+ */
    url("https://i.alipayobjects.com/common/fonts/rei.ttf?20140606")  format("truetype"), /* chrome、firefox、opera、Safari, Android, iOS 4.2+ */
    url("https://i.alipayobjects.com/common/fonts/rei.svg?20140606#rei") format("svg"); /* iOS 4.1- */
}
.iconfont {
    font-family:"rei";
    font-style: normal;
    font-weight: normal;
    cursor: default;
    -webkit-font-smoothing: antialiased;
}
</style>
`````

<link type="text/css" rel="stylesheet" media="screen" href="/alice-button/1.3.0/button.css">
<link type="text/css" rel="stylesheet" media="screen" href="/alice-tiptext/1.3.0/src/tiptext.css">
<link type="text/css" rel="stylesheet" media="screen" href="src/form.css">

### 基本用法

````html
<form class="ui-form" name="" method="post" action="#" id="">
    <fieldset>
        <legend>表单标题</legend>

        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本</label>
            <p class="ui-form-text">一个个文字文字
        </div>

        <div class="ui-form-item">
            <label for="" class="ui-label">
                <span class="ui-form-required">*</span>表单项文本
            </label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">添加备注</a></span>
            <p class="ui-form-explain">默认文案。</p>
        </div>

        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本</label>
            <input class="ui-input ui-input-large" type="text"> <span class="ui-form-other"><a href="#">表单项其他</a></span>
            <p class="ui-form-explain ui-tiptext ui-tiptext-error">
                <i class="ui-tiptext-icon iconfont" title="出错">&#xF045;</i>
                此在DOM上保存属性值，请使用data-xxx的形式。
            </p>
        </div>

        <div class="ui-form-item ui-form-item-error ui-form-item-focus">
            <label for="" class="ui-label">表单项文本</label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">表单项其他</a></span>
            <p class="ui-form-explain ui-tiptext ui-tiptext-error">
                <i class="ui-tiptext-icon iconfont" title="出错">&#xF045;</i>
                ui-form-item-focus 的效果。
            </p>
        </div>
              
        <div class="ui-form-item ui-form-item-success">
            <label for="" class="ui-label">表单项文本</label>
            <textarea class="ui-textarea">一二三四五六七八九十</textarea>
            <p class="ui-form-explain ui-tiptext ui-tiptext-success">
                <i class="ui-tiptext-icon iconfont" title="成功">&#xF049;</i>
                成功文案。
            </p>
        </div>
         
        <div class="ui-form-item">
            <label for="" class="ui-label">下拉选择</label>
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
            <label for="" class="ui-label ui-label-reset">不可用input</label>
            <input class="ui-input ui-input-disable" type="text" disabled>       
            <p class="ui-form-explain">目前不可用</p>
        </div>
         
        <div class="ui-form-item">
            <label for="" class="ui-label">验证码</label>
            <input class="ui-input ui-input-checkcode" type="text" data-explain="请输入右图中字符，不区分大小写。" maxlength="4" autocomplete="off" value="" name="fourcode">
            <img class="ui-checkcode-imgcode-img" align="absMiddle" alt="请输入您看到的内容" src="https://omeo.alipay.com/service/checkcode?sessionID=82012ab6b1f4ed9e675fb9092a25cb3b&r=0.9321065918075809"  title="点击刷新图片校验码">
            <a href="#">看不清，换一张</a>
            <div class="ui-form-explain">请输入右图中字符，不区分大小写。</div>
        </div>
 
        <div class="ui-form-item">
            <label for="test">
                <input class="ui-checkbox" id="test" value="" type="checkbox">
                我已阅读并接受自主缴费服务协议
            </label>
        </div>
 
        <div class="ui-form-item">
            <input type="submit" class="ui-button ui-button-morange" value="确定">
            <input type="button" class="ui-button ui-button-mwhite" value="取消">
        </div>
    </fieldset>
</form>
````

> input 和 textarea 的 :focus 、:hover 效果在 IE6 下无效，
  可使用 `ui-input-focus` 和 `ui-input-hover` 类来修复。


### 大表单

````html
<form class="ui-form ui-form-large" name="" method="post" action="#" id="">
    <fieldset>
        <legend>表单标题</legend>
         
        <div class="ui-form-item">
            <label for="" class="ui-label">
                <span class="ui-form-required">*</span>表单项文本
            </label>
            <input class="ui-input" type="text"> <span class="ui-form-other"><a href="#">添加备注</a></span>
            <p class="ui-form-explain">默认文案。</p>
        </div>

        <div class="ui-form-item ui-form-item-error">
            <label for="" class="ui-label">表单项文本</label>
            <input class="ui-input ui-input-large" type="text"> <span class="ui-form-other"><a href="#">表单项其他</a></span>
            <p class="ui-form-explain ui-tiptext ui-tiptext-error">
                <i class="ui-tiptext-icon iconfont" title="出错">&#xF045;</i>
                此在DOM上保存属性值，请使用data-xxx的形式。
            </p>
        </div>

        <div class="ui-form-item">
            <input class="ui-checkbox" id="test2" value="" type="checkbox">
            <label class="ui-checkbox-label" for="test2">我已阅读并接受自主缴费服务协议</label>
        </div>

        <div class="ui-form-item">
            <input type="submit" class="ui-button ui-button-lorange" value="确定">
        </div>

    </fieldset>
</form>
````

和 arale/validator 配合使用：http://aralejs.org/validator/examples/with-alice-form.html
