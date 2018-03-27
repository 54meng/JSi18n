基于javascrip开发的前端国际化
===========================
### 实现切换语言
### 采用localStorage存储语言
    $(function () {
    	//是否存在语言项
       if (!localStorage.currentLang) {
            //本地存储当前选中语言
            localStorage.currentLang = $('#lang option:selected').val();
        } else {
            //定义当前语言
            var currLang = localStorage.currentLang;
            $("#lang option[value=" + currLang + "]").attr("selected", true);
            $("#lang").on('change', function () {
               //存储当前选中的语言
            localStorage.currentLang = $(this).children('option:selected').val();
            //刷新  单页面可以注释
            location.reload();
        });
    }
    langString(localStorage.currentLang)
});
###语言包使用JS文件
var data_ch = {

    "name":"蔚为",
   
};
