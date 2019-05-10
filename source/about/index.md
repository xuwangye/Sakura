---
title: about
date: 2018-12-12 22:14:36
keywords: 关于
description: 
comments: false
photos: https://cdn.jsdelivr.net/gh/xuwangye/cdn@1.3/img/banner/about.jpg
---
{% raw %}
<div class="moe-mashiro" style="text-align:center; font-size: 50px; margin-bottom: 20px;">[さくら荘の徐王爷]</div>
<div id="hello-mashiro" class="popcontainer" style="min-height: 300px; padding: 2px 6px 4px; background-color: rgba(242, 242, 242, 0.5); border-radius: 10px;">
  <center>
  <p>
  </p>
  <h4>
  与&nbsp;<ruby>
  徐王爷&nbsp;<rp>
  （</rp>
  <rt>
  真（ま）白（しろ）</rt>
  <rp>
  ）</rp>
  </ruby>
  对话中...</h4>
  <p>
  </p>
  </center>
  <bot-ui></botui>
</div>
<script src="https://cdn.jsdelivr.net/vue/latest/vue.min.js"></script>
<script src="https://unpkg.com/botui/build/botui.min.js"></script>
<script>
function bot_ui_ini() {
    var botui = new BotUI("hello-mashiro");
    botui.message.add({
        delay: 800,
        content: "Hi！！！👋"
    }).then(function () {
        botui.message.add({
            delay: 1100,
            content: "我就是 徐王爷啦"
        }).then(function () {
            botui.message.add({
                delay: 1100,
                content: "一个可爱正义的蓝孩子~"
            }).then(function () {
                botui.action.button({
                    delay: 1600,
                    action: [{
                        text: "然后呢？ 😃",
                        value: "sure"
                    }, {
                        text: "少废话！ 🙄",
                        value: "skip"
                    }]
                }).then(function (a) {
                    "sure" == a.value && sure();
                    "skip" == a.value && end()
                })
            })
        })
    });
    var sure = function () {
            botui.message.add({
                delay: 600,
                content: "😘"
            }).then(function () {
                secondpart()
            })
        },
        end = function () {
            botui.message.add({
                delay: 600,
                content: "![...](https://view.moezx.cc/images/2018/05/06/a1c4cd0452528b572af37952489372b6.md.jpg)"
            })
        },
        secondpart = function () {
            botui.message.add({
                delay: 1500,
                content: "毕业于浙江经贸职业技术学院"
            }).then(function () {
                botui.message.add({
                    delay: 1500,
                    content: "一心一意想做技术大佬，最终还是个小辣鸡…"
                }).then(function () {
                    botui.message.add({
                        delay: 1200,
                        content: "职业：开发JAVA后端"
                    }).then(function () {
                        botui.message.add({
                            delay: 1500,
                            content: "主攻 JAVA 语言"
                        }).then(function () {
                            botui.message.add({
                                delay: 1500,
                                content: "研究的方向分布式"
                            }).then(function () {
                                botui.message.add({
                                    delay: 1800,
                                    content: "喜欢画画，希望有一天能够被称为画师"
                                }).then(function () {
                                    botui.action.button({
                                        delay: 1100,
                                        action: [{
                                            text: "为什么叫徐王爷呢？ 🤔",
                                            value: "why-mashiro"
                                        }]
                                    }).then(function (a) {
                                        thirdpart()
                                    })
                                })
                            })
                        })
                    })
                })
            })
        },
        thirdpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "因为姓徐想做一个王爷，负责咸鱼就好~"
            }).then(function () {
                botui.action.button({
                    delay: 1500,
                    action: [{
                        text: "你喜欢什么？ 🤔",
                        value: "why-cat"
                    }]
                }).then(function (a) {
                    fourthpart()
                })
            })
        },
        fourthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "猫咪！！！ "
            }).then(function () {
                botui.message.add({
                    delay: 1100,
                    content: "而且我真的是猫控！"
                }).then(function () {
                    botui.action.button({
                        delay: 1500,
                        action: [{
                            text: "域名有什么含意吗？(ง •_•)ง",
                            value: "why-domain"
                        }]
                    }).then(function (a) {
                        fifthpart()
                    })
                })
            })
        },
        fifthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "emmmm，一看就知道是GitHub域名，想买一个但是穷。。"
            }).then(function () {
                botui.message.add({
                    delay: 1600,
                    content: "那么，仔细看看我的博客吧？ ^_^"
                })
            })
        } 
}
bot_ui_ini()
</script>
{% endraw %}