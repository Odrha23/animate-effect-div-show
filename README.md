# animate-effect-div-show
Animasi div bergerak jika discroll, bukan animasi page

<!--
<script type="text/javascript">
$(document).ready(function(){
    $(window).on("load scroll resize", function(){
        $('.header').scrollzip({
            showFunction    : function() { $(this).css("visibility", "visible").addClass('animated bounceInDown'); },
        });
        $('.section1,.section3,.section5,.section7,.block-left').scrollzip({
            showFunction    : function() { $(this).css("visibility", "visible").addClass('animated bounceInLeft'); },
            hideFunction    : function() { $(this).css("visibility", "hidden").removeClass('animated'); },
            showShift       : 100,
            hideShift       : 15,
        });
        $('.section2,.section4,.section6,.block-right').scrollzip({
            showFunction    : function() { $(this).css("visibility", "visible").addClass('animated bounceInRight'); },
            hideFunction    : function() { $(this).css("visibility", "hidden").removeClass('animated'); },
            showShift       : 50,
            hideShift       :50,
        });
    });
});
</script>
    
<style>
    a{text-decoration: none;color: #3181CA;}
    .subtitle{}
    .header{text-align: center;visibility: hidden;}
    .title{font-size:50px;}
    .title,.description{}
    body{background: #eeeeee;color: #333333;font-family: arial;font-size:14px;margin: 0;padding: 0;overflow-x:hidden;}
    .container{width: 800px;margin: 50px auto;max-width:90%;}
    .section{background: #ffffff;border: 1px solid #dddddd;margin-top: 50px;padding: 20px;visibility: hidden;}
    #content,#content2{background:#ddd;height:200px;display:hidden;}
    .t1{width:100px;height:100px;background:#ef8603;margin:20px;visibility:hidden;}
    .highlight{font-weight:bold;}
    .option-table tr{vertical-align:top;}
    table.option-table{border-width: 1px;border-spacing: 0px;border-style: outset;border-color: #f7f7f7;border-collapse: separate;background-color: white;}
    table.option-table th {border-width: 1px;padding: 5px;border-style: inset;border-color: #f7f7f7;background-color: white;}
    table.option-table td {border-width: 1px;padding: 5px;border-style: inset;border-color: #f7f7f7;background-color: white;}
    .footer{margin-top: 50px;margin-bottom: 50px;text-align: right;}
    .share{margin-top: 20px;}
    .clear{clear: both;}
</style>

</head>
<body>

<div class='container'>
    <div class='header'>
        <h1 class='title'>ScrollZip</h1>
        <div class='description'>jQuery plugin to trigger functions when element/content becomes visibile/hidden while scrolling</div>
        <div class='share'>SHARE</div>
    </div>
    
    <div class='section section1'><h2 class='subtitle'>Intro</h2>
    ScrollZip is a jQuery plugin that is used <span class='highlight'>to add some event/action/effect to the web elements when it is becoming visibile or hidden while scrolling</span> the web page.
    This plugin doesn't actually add any action, It just finds whether the element is coming into or going out of the visible part of the browser viewport and triggers the function in the showFunction, hideFunction part accordingly.
                
    </div>
                <div class='section section2'><h2 class='subtitle'>Example Usage</h2>
                <a href='http://github.com/tinywall/scrollzip' target='_blank'>Download</a> and include the <a href='http://jquery.com' target='_blank'>jQuery</a> library and the <a href='https://raw.github.com/tinywall/scrollzip/master/jquery.scrollzip.js' target='_blank'>ScrollZip</a> plugin in your web page.
                <pre class="  language-markup"><code>
&lt;script src="jquery-1.10.2.min.js"&gt;&lt;/script&gt;
&lt;script src="jquery.scrollzip.js"&gt;&lt;/script&gt;
                </code></pre>
                Now write the function to be called for the elements like the below code,
                <pre><code class="  language-javascript">
$(document).ready(function(){
    $(window).on("load scroll resize", function(){
        $('element').scrollzip({
            showFunction    :   function() {
                                    alert('Element has come into the view.');
                                },//optional
            hideFunction    :   function() {
                                    alert('Element has gone out of the view.');
                                },//optional
            wholeVisible    :     false,//optional (default false)
            showShift       :     100,//optional (default 0)
            hideShift       :     100,//optional (default 0)
        });
    });
});
                </code></pre>
                </div>
    <div class='section section3'><h2 class='subtitle'>Options</h2>
        <table class="option-table" border='1'>
        <tr>
        <td>showFunction</td>
        <td>This function is used to write some code to be executed when the given element is becoming visible to user when scrolling. i.e. coming into the visible part of the browser viewport.</td>
        </tr>
        <tr>
        <td>hideFunction</td>
        <td>Same like showFunction but for the event of the element going out of the visible part of the screen.</td>
        </tr>
        <tr>
        <td>wholeVisible</td>
        <td>By default, Even when the small part of the element enters/exists the visibile part, the respective function is being called. But if you make wholeVisible to true, When the whole part of the element comes into the visibil area only the function triggers.</td>
        </tr>
        <tr>
        <td>showShift</td>
        <td>To manually specify the distance after how much px it is into the screen, it should trigger the event. Nagative value to trigger the function for the distance before it is being displayed.</td>
        </tr>
        <tr>
        <td>hideShift</td>
        <td>Same like showShift but for hiding the element.</td>
        </tr>
        </table>
   </div>
    <div class='section section4'><h2 class='subtitle'>Beware</h2>
        Yes, there is already some good old jQuery plugins there for the scenario. But whats wrong? Let this be yet another solution.
        And by the way I am new to jQuery plugins. So beware, this may be a creepy unoptimised implementation?!.<br/> 
        But still it works!!.. Isn't that enough?
        <br/><br/>Here in this demo, I am using the <a href='http://daneden.me/animate/' target='_blank'>Animate.css</a> by <a href='https://twitter.com/_dte' target='_blank'>@_dte</a> for the CSS3 animations.<br/><br/>
                <div style='margin-top:10px;float:left;'>
                By the way, I am <a href='http://www.arundavid.com/' target='_blank'>Arun David</a>.
                </div>
                <div style='margin-top:8px;float:left;'>
                    &nbsp;&nbsp;&nbsp;<a href="https://twitter.com/ArnDvd" class="twitter-follow-button" data-show-count="false">Follow @ArnDvd</a>

                </div>
                <div class='clear'></div>
    </div>
    <div class='section block-right'>HTML5</div>
    <div class='section block-left'>CSS3</div>
    <div class='section block-right'>JavaScript <br/>
    <pre><code class="  language-javascript">
$(document).ready(function(){
    $(window).on("load scroll resize", function(){
        $('element').scrollzip({
            showFunction    :   function() {
                                    alert('Element has come into the view.');
                                },//optional
            hideFunction    :   function() {
                                    alert('Element has gone out of the view.');
                                },//optional
            wholeVisible    :     false,//optional (default false)
            showShift       :     100,//optional (default 0)
            hideShift       :     100,//optional (default 0)
        });
    });
});
                </code></pre>
    </div>
    <div class='footer'>Copyright &copy; Tinywall</div>
</div>
