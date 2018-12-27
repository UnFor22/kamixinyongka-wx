<template>
  <!-- 主页 -->
  <div>
    <!-- 不必显示的养卡攻略 -->
    <div v-if="SHOW">
      <!-- 页顶导航栏 -->
        <div class="cardraiders">
          <div class="funList">     
            <div @click="toyongkajingyan" style="display: inline-block;">
                <img src='../../assets/yangka.png' alt="">
                <p style="font-size: 14px; color: #333;">用卡经验</p>
            </div>
          <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
              <img src='../../assets/jihuo.png' alt="">
              <p style="font-size: 14px; color: #333;">进度查询</p>
          </div>
          <div class="funListMiddle" @click="toyanjiuwanka" style="display: inline-block;">
              <img src='../../assets/chaxun.png' alt="">
              <p style="font-size: 14px; color: #333;">研究玩卡</p>
          </div>
        
        </div>  
        <!-- 热门查询导航 -->
        <div class="hotBanks_no">
          <div class="hotBanks_header">
            <p class="theme_p" style="color: #363636;"><span class="leftBorder"></span>热门查询</p>          
            
          </div>
          <div class="hotBanks_chaxun" style="background:#fff;">
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/jt-2x.png'  mode="widthFix"  alt="">
                <p style="font-size: 14px; color: #333;">交通</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/js-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">建设</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/gs-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">工商</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/zx-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">中信</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/ny-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">农业</p>
            </div>
          </div>
          <div class="hotBanks_chaxun" style="background:#fff;">
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/pa-2x.png'  mode="widthFix"  alt="">
                <p style="font-size: 14px; color: #333;">平安</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/gd-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">光大</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/gf-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">广发</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/zg-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">中国</p>
            </div>
            <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
                <img src='https://api.51datakey.com/h5/logo/bank/xy-2x.png' mode="widthFix" alt="">
                <p style="font-size: 14px; color: #333;">兴业</p>
            </div>
          </div>
        </div>
        <!-- 推荐信息标题 -->
        <div class="hotBanks">
          <div class="hotBanks_header">
            <p class="theme_p" style="color: #363636;"><span class="leftBorder"></span>推荐信息</p>          
            
          </div>
        </div>
        <!-- 推荐信息内容 -->
        <div class="articleList">
          <div @click="tocardraidersdetails('中信首刷礼怎么领取 中信银行信用卡首刷礼',34)">
            <div class="content">
              <div class="content_left">
                <p>中信首刷礼怎么领取 中信银行信用卡首刷礼</p>
                <p>中信银行为信用卡首刷用户提供了丰富的首刷礼，那么这个中信首刷礼怎么领取？ </p>
                <span>2018-06-08</span>
                <span><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 9845</span>
              </div>
              <!-- <div class="content_right">
                <img src="http://image.sudaizhijia.com/production/20171229/bank/20171229171255-146.png" mode="widthFix" alt="">
              </div> -->
            </div>
          </div>
          <div @click="tocardraidersdetails('光大信用卡首刷哪里领 光大信用卡首刷礼',35)">
            <div class="content">
              <div class="content_left">
                <p>光大信用卡首刷哪里领 光大信用卡首刷礼</p>
                <p>活动期间，通过网络渠道在线申请光大信用卡指定卡种的新客户，活动期间首刷不限金额即有机会获赠50元刷卡金。</p>
                <span>2018-06-08</span>
                <span><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 9845</span>
              </div>
              <!-- <div class="content_right">
                <img src="http://image.sudaizhijia.com/production/20171229/bank/20171229171255-146.png" mode="widthFix" alt="">
              </div> -->
            </div>
          </div>
          <div @click="tocardraidersdetails('浦发开卡礼在哪里领取 浦发银行信用卡首刷礼',36)">
            <div class="content">
              <div class="content_left">
                <p>浦发开卡礼在哪里领取 浦发银行信用卡首刷礼</p>
                <p>浦发银行信用卡首刷礼品是什么？</p>
                <span>2018-06-08</span>
                <span><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 9845</span>
              </div>
              <!-- <div class="content_right">
                <img src="http://image.sudaizhijia.com/production/20171229/bank/20171229171255-146.png" mode="widthFix" alt="">
              </div> -->
            </div>
          </div>
          <!--“爱购全球”境外畅购折扣享不停 返现高达16%-->
          <div @click="tocardraidersdetails('“爱购全球”境外畅购折扣享不停 返现高达16%',14)">
            <div class="content">
              <div class="content_left">
                <p> “爱购全球”境外畅购折扣享不停 返现高达16%</p>
                <!-- <p>活动时间：北京时间2018年10月1日至2018年12月31日</p> -->
                <span>2018-06-08</span>
                <span class="right_span"><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 3530</span>
              </div>
              <!-- <div class="content_right">
                <img src="http://image.sudaizhijia.com/production/20170920/bank/20170920151057-269.png" mode="widthFix" alt="">
              </div> -->
            </div>
          </div>

          <div  @click="tocardraidersdetails('降额是什么原因 信用卡被降额补救办法',15)">
            <div class="content">
              <div class="content_left">
                <p>降额是什么原因 信用卡被降额补救办法</p>
                <span>2018-06-08</span>
                <span><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 6680</span>
              </div>
              <!-- <div class="content_right">
                <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b10000_10000&sec=1530103741&di=f9639e4e2b06ca0eedd9d4680fd99b32&src=http://imgsrc.baidu.com/forum/pic/item/7e3e6709c93d70cf4f46d499f8dcd100bba12be1.jpg" mode="widthFix" alt="">
              </div> -->
            </div>
          </div>

          <div @click="tocardraidersdetails('办理分期划算吗 信用卡怎样还款最划算',18)">
            <div class="content">
              <div class="content_left">
                <p>办理分期划算吗 信用卡怎样还款最划算</p>
                <span>2018-06-08</span>
                <span><img style="width:30rpx;" src="../../assets/liulan@2x.png" mode="widthFix" alt=""> 5541</span>
              </div>            
            </div>
          </div>
        </div>
      </div>
    </div>

    <div v-if='!SHOW' class="card">
      <div class="active_fuchuang" @click="toactive(1)">
        <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/active_img.png" mode="widthFix" alt="">
      </div>
      <!-- 蒙版  -->
      <div class="mengban" v-if="showmengban">
        <div @click="toquxiao" class="toquxiao">
        </div>
        <img src="../../assets/active/quxiao_active.png" mode="widthFix" alt="">
      </div>
      <!-- 开奖页 -->
      <div class="kaijiang" v-if="showkaijiang">
        <img class="main_img" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/kaijiang.png" mode="widthFix" alt="">
        
        <div class="kaijiang_btn">
          <button v-if="isshouquan" @click="toaward"></button>
          <button v-else open-type='getUserInfo' lang="zh_CN" @getuserinfo="onGotUserInfo"></button>
          <img class="kaijiang_button" mode="widthFix" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/kaijiang_btn.png" alt="">          
        </div>
        <div class="kaijiang_title1">
          <p>哇 第一个猪年红包</p>
        </div>
        <div class="kaijiang_title2">
          <p>由您开启!</p>
        </div>
       
      </div>
      <!-- 奖品页 -->
      <div class="award" v-if="showaward">
        <img class="main_img" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/award.png" mode="widthFix" alt="">
        <div class="award_rule" @click="toactiveshuoming">
          <img src="../../assets/active/award_rule.png" mode="widthFix" alt="">
        </div>
        <div class="award_title">
          <p>恭喜您获得￥{{award}}</p>
          <p>100金币=1元红包,可提现</p>
        </div>
        <div class="award_btn" @click="tofenxiang">
          <img class="award_button" mode="widthFix" src="../../assets/active/award_btn.png" alt=""> 
        </div>
        
      </div>
      <!-- 分享好友助力页 -->
      <div class="share" v-if="showshare">
        <img class="main_img" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/share.png" mode="widthFix" alt="">
        <div class="share_swiper">
          <swiper :show-indicators="false" interval="3000" autoplay='true' circular='true' vertical='true' style="font-size:14px; height:30rpx; color:rgba(0,0,0,0.4);">
            <swiper-item catchtouchmove="stopTouchMove" v-for="(item, index) in tixianUser" :key="index">
              <img :src="item.img" alt="">
              <span style="font-size:10px; color:#F22216;">{{item.name}}通过好友助力成功提现</span>
            </swiper-item>
          </swiper>
        </div>
        <div class="to_share_right">
          <button class="share_button" open-type='share'></button>
          <img class="share_right" mode="widthFix" src="../../assets/active/share_btn1.png" alt="">
        </div>
        <div class="share_userInfo">
          <div class="share_userimg">
            <img class="user_img" :src="userImg" alt="">
            <p>还差<span style="font-size:26px;">{{haicharenshu}}</span>人</p>
            <p>即可获得￥{{award}}</p>
          </div>
        </div>
        <div class="share_main">
          <p>距结束：<span class="time">{{times.days}}</span>天<span class="time">{{times.hours}}</span>时<span class="time">{{times.mins}}</span>分<span class="time">{{times.secs}}</span></p>
          <p>{{peoplenum}}人已经兑换提现</p>
        </div>
        <div class="share_user" @click="tozhulixiangqing">
          <li v-for="(item,index) in userArr" :key="index">
            <img mode="widthFix" :src="item.img" alt="">
          </li>
        </div>
        <div class="share_btn" @click="tofenxiang">
          <button open-type='share'></button>
          <img class="share_button" mode="widthFix" src="../../assets/active/share_btn.png" alt=""> 
        </div>
        <div class="share_tips">
          <p>超过5人后，每增加1位好友可累积获得10-100金币不等，分享越多，提现金额越多</p>
        </div>
        
      </div>
      <!-- 助力完成页 -->
      <div class="complete" v-if="showcomplete">
        <img class="main_img" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/complete.jpg" mode="widthFix" alt="">
        <div class="share_swiper">
          <swiper :show-indicators="false" interval="3000" autoplay='true' circular='true' vertical='true' style="font-size:14px; height:30rpx; color:rgba(0,0,0,0.4);">
            <swiper-item catchtouchmove="stopTouchMove" v-for="(item, index) in tixianUser" :key="index">
              <img :src="item.img" alt="">
              <span style="font-size:10px; color:#F22216;">{{item.name}}通过好友助力成功提现</span>
            </swiper-item>
          </swiper>
        </div>
        <div class="to_share_right">
          <button class="share_button" open-type='share'></button>
          <img class="share_right" mode="widthFix" src="../../assets/active/share_btn1.png" alt="">
        </div>
        <div class="complete_title">
          <p>{{complete_ttt}}</p>
          <p>累积获得<span style="font-size:24px;  font-weight:600;">￥{{award}}</span>金币</p>
        </div>
        <div class="share_main">
          <p>距结束：<span class="time">{{times.days}}</span>天<span class="time">{{times.hours}}</span>时<span class="time">{{times.mins}}</span>分<span class="time">{{times.secs}}</span>秒</p>
        </div>
        <div class="share_user" @click="tozhulixiangqing">
          <li v-for="(item,index) in userArr" :key="index">
            <img mode="widthFix" :src="item.img" alt="">
            <!-- <span>{{item.name}}</span> -->
          </li>
        </div>
        <div class="complete_more" @click="tozhulixiangqing">
          <p>共有<span style='font-weight: 700;'>{{helpNum}}</span>位好友和你一起接龙</p>
          <p>查看>></p>
        </div>
        <div class="complete_btn">
          <button open-type='share'></button>
          <img class="totixian_button" @click="totixian" mode="widthFix" src="../../assets/active/tixian_button.png" alt="">
          <img class="complete_button" mode="widthFix" src="../../assets/active/complete_btn.png" alt="">
          
        </div>
        <div class="complete_tips">
          <p>账户余额：{{award}}金币</p>
          
        </div>
      
      </div>
      <!-- 帮助好友助力页 -->
      <div class="helphe" v-if="showhelphe">
        <img class="main_img" src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/helphe.png" mode="widthFix" alt="">
        <div class="helphe_title">
          <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/helphe_title.png" mode="widthFix" alt="">
          <!-- <p>快来和我一起玩接龙</p> -->
        </div>
        <div class="helphe_user">
          <img class="helphe_userimg" :src="fenxiangImg" mode="widthFix" alt="">
          <p class="helphe_username">{{fenxiangname}}</p>
          <p class="helphe_usertitle">还差<span>1</span>人</p>
          <p class="helphe_usertitle">就可以兑换提现啦</p>
        </div>
        <div class="helphe_btn">  
          <button class="helphe_btn1" v-if="isshouquan"  @click="tosuccess"></button>
          <button class="helphe_btn1" v-else open-type='getUserInfo' lang="zh_CN" @getuserinfo="GotUserInfo"></button>
          <img class="helphe_button1" src="../../assets/active/helphe_btn1.png" mode="widthFix" alt="">
          <button class="helphe_btn2" @click="tokaijiang"></button>
          <img class="helphe_button2" src="../../assets/active/helphe_btn2.png" mode="widthFix" alt="">
        </div>
      
      </div>
      <!-- 助力成功 -->
      <div class="success" v-if="showsuccess">
        <img class="main_img" src="../../assets/active/success.png" mode="widthFix" alt="">
        <div class="success_title">
          <p>接龙成功啦</p>
        </div>
        <div class="success_tips">
          <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/success_tips.png" mode="widthFix" alt="">
          <p>小手抖一抖，红包就到手</p>
        </div>
        <div class="success_btn">
          <button @click="tokaijiang(1)"></button>
          <img class="success_button" mode="widthFix" src="../../assets/active/success_btn.png" alt=""> 
        </div>
       
      </div>
      <!-- 提现 -->
      <div class="tixian" v-if="showtixian">
        <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/phone.png" mode="widthFix" class="main_img" alt="">
        <div class="share_swiper">
          <swiper :show-indicators="false" interval="3000" autoplay='true' circular='true' vertical='true' style="font-size:14px; height:30rpx; color:rgba(0,0,0,0.4);">
            <swiper-item catchtouchmove="stopTouchMove" v-for="(item, index) in tixianUser" :key="index">
              <img :src="item.img" alt="">
              <span style="font-size:10px; color:#F22216;">{{item.name}}通过好友助力成功提现</span>
            </swiper-item>
          </swiper>
        </div>
        <div class="to_share_right">
          <button class="share_button" open-type='share'></button>
          <img class="share_right" mode="widthFix" src="../../assets/active/share_btn1.png" alt="">
        </div>
        <div class="tixian_title">
          <p>可兑换现金</p>
          <p>{{tixianNum}}元</p>
        </div>
        <div class="tixian_input">
          <div class="tixian_input_phone">
            <input type="text" v-model="phoneNum" placeholder="输入手机号">
          </div>
          <div class="tixian_input_code">
            <input type="text" v-model="QRcode" placeholder="输入验证码">
            <div class="getcode" v-if="codejishi" @click="getcode">点击获取</div>
            <div class="getcode" v-else>{{codeTime}}秒</div>
          </div>
        </div>
        <div class="tixian_btn">
          <button class="tixian_button" @click="bindphone"></button>
          <img mode="widthFix" class="tixian_button" src="../../assets/active/phone_btn.png" alt="">
        </div>
        <div class="tixian_tips" @click="toactiveshuoming">
          <p>小提示：好友接龙越多，金币越多，兑换现金越多</p>
          <p>查看活动说明 >></p>
        </div>
        
      </div>
      <!-- 提现页有手机 -->
      <div class="phone" v-if="showphone">
        <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/havephone.png" mode="widthFix" class="main_img" alt="">
        <div class="share_swiper">
          <swiper :show-indicators="false" interval="3000" autoplay='true' circular='true' vertical='true' style="font-size:14px; height:30rpx; color:rgba(0,0,0,0.4);">
            <swiper-item catchtouchmove="stopTouchMove" v-for="(item, index) in tixianUser" :key="index">
              <img :src="item.img" alt="">
              <span style="font-size:10px; color:#F22216;">{{item.name}}通过好友助力成功提现</span>
            </swiper-item>
          </swiper>
        </div>
        <div class="to_share_right">
          <button class="share_button" open-type='share'></button>
          <img class="share_right" mode="widthFix" src="../../assets/active/share_btn1.png" alt="">
        </div>
        <div class="tixian_title">
          <p>可兑换现金</p>
          <p>{{tixianNum}}元</p>
        </div>
        <div class="phone_num">
          <img src="../../assets/active/havephone_duihao.png" alt="">
          <p>已绑定手机号</p>
          <p>{{mob}}</p>
        </div>
        <div class="phone_btn">
          <button class="phone_button" @click="tojiakefu"></button>
          <img mode="widthFix" class="phone_button" src="../../assets/active/phone_btn.png" alt="">
        </div>
        <div class="tixian_tips" @click="toactiveshuoming">
          <p>小提示：好友接龙越多，金币越多，兑换现金越多</p>
          <p>查看活动说明 >></p>
        </div>
        
      </div>
      <!-- 加客服页 -->
      <div class="jiakefu" v-if="showjiakefu">
        <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/jiakefu.png" mode="widthFix" class="main_img" alt="">
        <div class="jiakefu_title">
          <p>添加客服微信给您发红包</p>
        </div>
        <div class="jiakefu_erweima">
          <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/jiekefu_qrcode.png" @tap="previewImage" mode="widthFix" alt="">
        </div>
        <div class="jiakefu_methods">
          <p>领取方式</p>
        </div>
        <div class="jiakefu_tips">
          <li>
            <img src="../../assets/active/jiakefu_coin.png" mode="widthFix" alt="">
            <p>点击二维码 -> 长按图片保存 -> 添加客服</p>
          </li>
          <li>
            <img src="../../assets/active/jiakefu_coin.png" mode="widthFix" alt="">
            <p>添加时备注手机号+金额</p>
          </li>
        </div>
      </div>
      <!-- 功能导航 -->
      <div class="funList">   
        <div v-if="!SHOW" @click="toOnbehalf" style="display: inline-block;">
            <img src='https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/samll_daihuan.png' alt="">
            <p style="font-size: 14px; color: #333;">代还</p>
        </div>  
        <div class="funListMiddle" @click="toprogresscheck" style="display: inline-block;">
            <img src='https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/samll_chaxun.png' alt="">
            <p style="font-size: 14px; color: #333;">进度查询</p>
        </div>
        <div @click="toyongkajingyan" style="display: inline-block;">
          <img src='https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/samll_yangka.png' alt="">
          <p style="font-size: 14px; color: #333;">用卡经验</p>
        </div>
        <div class="funListMiddle" @click="toyanjiuwanka" style="display: inline-block;">
          <img src='https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/samll_wanka.png' alt="">
          <p style="font-size: 14px; color: #333;">研究玩卡</p>
        </div>
        <!-- <div @click="toGonglue" style="display: inline-block;">
            <img src='../../assets/yangka.png' alt="">
            <p style="font-size: 14px; color: #333;">养卡攻略</p>
        </div> -->
        <!-- <div v-if="isCredit==true" class="funListMiddle" @click="toProgresscheck" style="display: inline-block;">
            <img src='https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/samll_quxian.png' alt="">
            <img src='../../assets/hot.gif' alt="" class="hotGif">
            <p style="font-size: 14px; color: #333;">取现</p>
        </div> -->
        
        <!-- <div class="funListMiddle" @click="toActivation" style="display: inline-block;">
          <img src='../../assets/jihuo.png' alt="">
          <p style="font-size: 14px; color: #333;">激活</p>
        </div> -->
        
      </div>  
      <!-- 分割线 -->
      <div class="splitLine" style="margin: 0;"></div>   
      <!-- 需要显示的主体部分 -->
      <div>
      <!-- <div v-if="true"> -->
        <!-- 热门 -->
        <div class="hotBanks">
          <div class="hotBanks_header">
            <p class="theme_p" style="color: #363636;"><span class="leftBorder"></span>热门</p>          
            <span @click="tofiltercard" style="color: #7370FF;font-size: 14px;">全部卡片<img src="../../assets/cardCenterMore.png" alt="" style="width: 12rpx; height:22rpx; vertical-align: middle; margin-left: 6rpx;margin-top: -2rpx;"></span>
          </div>
          <div class="hotBanks_content">
            <!-- loading图 -->
            <div class="loading" v-if=isLoading_hotBank>
              <img src="../../assets/loading22.gif" alt="">
            </div>
            <ul>             
              <li v-for="(item,index) in showList" @click="toHotbank(item)" :key="index">                
                  <span v-if="item.banktips!=''"  :class="{tips}">{{item.banktips}}</span>
                  <div>
                    <img :src=item.banklogo alt="">
                    <p>{{item.bankname}}</p>
                    <p style="color: #999;">{{item.bankcontent}}</p>
                  </div>                
              </li> 
            </ul>
            <div v-if="!showGD" class="moreItem" style="height:64rpx" @click="toggleShowList">{{word1}}<img :src=gengduo style="width: 28rpx; height:15rpx; vertical-align: middle; margin-left: 10rpx" alt=""></div>
            <div v-else class="moreItem" style="height:64rpx" @click="toggleShowList">{{word2}}<img :src=shouqi style="width: 28rpx; height:15rpx; vertical-align: middle; margin-left: 10rpx" alt=""></div>
          </div>
        </div>
        <!-- 分割线 -->
        <div class="splitLine2" ></div>
        <!--主题精选-->
        <div class="theme">
          <p class="theme_p" style="color: #363636;"><span class="leftBorder"></span>主题精选</p>
          <!-- loading -->
          <div class="loading" v-if=isLoading_banner>
            <img src="../../assets/loading22.gif" alt="">
          </div>
          <div class="theme_content">
            <div class="theme_div" style="display: inline-block;" @click="toNovicecard">
                <div style="display: inline-block; margin-left:8rpx; margin-top: 6rpx;">
                  <p>{{noviceCard.topicname}}</p>
                  <p style="color: #9a9a9a; font-size: 11px">{{noviceCard.topiccontent}}</p>
                </div>
                <img src='../../assets/xinshoubanka@3x.png' alt="" style="width:margin-right: 14rpx;">
            </div>
            <div class="theme_verticalline"></div>
            <div class="theme_div" style="display: inline-block;" @click="tolargemonute">
                <div style="display: inline-block;margin-top: 6rpx;">
                  <p>{{bigQuota.topicname}}</p>
                  <p style="color: #9a9a9a; font-size: 11px">{{bigQuota.topiccontent}}</p>
                </div>
                <img src='../../assets/daedu@3x.png' alt="">
            </div>
              <div class="theme_transverseline" style="margin-left: 2%;"></div>
              <div class="theme_transverseline" style="margin-right: 2%;"></div>

            <div class="theme_div" style="display: inline-block;" @click="tofastproval">
                <div style="display: inline-block;margin-left:8rpx;margin-top: 6rpx;">
                  <p>{{fastApproval.topicname}}</p>
                  <p style="color: #9a9a9a; font-size: 11px">{{fastApproval.topiccontent}}</p>
                </div>
                <img src='../../assets/shenpikuai@3x.png' alt="" style="margin-right: 14rpx;">
            </div>
            <div class="theme_verticalline" style="margin-top: -10rpx;"></div>
            <div class="theme_div" style="display: inline-block;" @click="topolitecard">
                <div style="display: inline-block;margin-top: 6rpx;">
                  <p>{{politeCard.topicname}}</p>
                  <p style="color: #9a9a9a; font-size: 11px">{{politeCard.topiccontent}}</p>
                </div>
                <img src='../../assets/liwu@3x.png' alt="">
            </div>

          </div>
        </div>
        <!--轮播图-->
        <div class="banner">
          <div class="loading" v-if=isLoading_hotBank>
              <img src="../../assets/loading22.gif" alt="">
          </div>
          <swiper style="height:150rpx" autoplay='true' interval="2000">
            <swiper-item class="banneritem" v-for="(item, index) in bannerData" :key="index" >
              <a @click="tokefu('用卡',item.picurl)">
                <img style="width:740rpx; height:150rpx;" :src=item.pic_url alt="">
              </a>         
            </swiper-item>
          </swiper>

          <div class="lamititleswiper" style="width: 100%; height: 30rpx;margin-top:30rpx">
            <div style="float:left">
              <img id="kamiTitlePic" src="../../assets/kamititle.png">
            </div>
            <div style="margin-left:160rpx;">
              <swiper :show-indicators="false" interval="3000" autoplay='true' circular='true' vertical='true' style="font-size:14px; height:30rpx; color:rgba(0,0,0,0.4);">
                <swiper-item catchtouchmove="stopTouchMove" v-for="(item, index) in bannerDataTxt" :key="index">
                  <a @click="toswiperdetails(item.url,index,'光大')">
                    <span>{{item.title}}</span>
                  </a>
                </swiper-item>
              </swiper>
            </div>
          </div>
        </div>

        <div class="splitLine"></div>
        <!--热门-->
        <div class="hotCard" ref="test">
          <p class="hotCard_p" style="color: #363636;"><span class="leftBorder"></span>热门推荐</p>
          <div class="hotCard_content">
            <div class="loading" v-if=isLoading_hotCard>
                <img src="../../assets/loading22.gif" alt="">
            </div>
              <ul>
                <li v-for="(item, index) in pageList" :key="index" @click="tokefu(item.creditname,item.crediturl)">   
                  <a style="width: 100%; height: 100%">
                    <img :src=item.creditphotourl mode="widthFix" alt="">
                    <div class="bankContent">
                      <p>{{item.creditname}}</p>
                      <p>{{item.creditcontent}}</p>
                      <span class="itemTipsCss" v-for="(itemTips, i) in cardTips[index]" :key="i">{{itemTips}}</span>
                      <div class="cardNum">
                        <span><span style="color:#ff5b3d">{{item.cardcount}}</span>人拥有</span>
                      </div>  
                    </div>
                  </a>
                  <div class="imgBox">
                    <img v-if="index==0" :src=back_img1 alt="">
                    <img v-if="index==1" :src=back_img2 alt="">
                    <img v-if="index==2" :src=back_img3 alt="">
                  </div>      
                </li>
              </ul>
          </div>       
          <div class="noMore" v-if="!ReachBotton">
            <p>{{bottomText}}</p>
          </div>
        </div>
      </div>     
    </div>
    <vue-tab-bar  v-if='!SHOW'
      @fetch-index="clickIndexNav"
      :selectNavIndex=selectNavIndex
      :needButton="needButton"
      :handButton="handButton"
      :btnText="btnText">
    </vue-tab-bar>
  </div>        
</template>
<script>
  import md5 from 'js-md5';
  import Qs from 'qs';
  import vueTabBar from '../../components/tabBar'
  // import tab from '../../components/tabBar2'
  import {getHotBankInfoList, getContent, getTopicSelect, getBannerImg, getHotCard, getBannerTxt, registerHref, userOperation, getUserOpenid, postUser,postUserInfo, getTaskInfo, startTask, getRWInfo, helpHe, getCode, bandPhone} from '../../requestAPI/requestAPI';
  import { setInterval, clearInterval } from 'timers';
  import { fail } from 'assert';
  export default {
    data(){
      return {
        showmengban: false, // 控制开奖页显隐
        showkaijiang: false, // 控制奖品页显隐
        showaward: false,
        showshare: false,
        showcomplete: false,
        showhelphe: false,
        showsuccess: false,
        showtixian: false,
        showphone: false,
        showjiakefu: false,
        helpNum: 0,
        screenHeight:'',
        title: '',
        url:'',
        Url: '',
        urlStr:'',
        startTime: '',
        times:{
          days: '00',
          hours: '',
          mins: '',
          secs: ''
        },  // 助力计时
        award: '', // 奖金
        userImg: require('../../assets/active/moren.png'), // 用户头像
        userName: '', // 用户昵称
        fenxiangname: '', // 分享者昵称
        iszhuli: '',  // 记录分享者的openid，并根据这个判断是否为帮别人助力的
        complete_ttt: '', // 记录助力完成，根据人数显示不同标语
        peoplenum: '', // 已取现人数
        completezhuli: false, // 记录助力人的活动状态，是否已经帮助力过
        secondxianshi: false, // 记录是否助力完成，并确定是否显示
        isshouquan: false, // 记录用户是否授过权
        phoneNum: '',  // 记录用户电话号码
        QRcode: '',  // 记录用户验证码
        codeTime: 60, 
        codetime: '', // 验证码计时器
        endtime: '',  // 活动结束时间
        codejishi: true,
        tixianNum: 8.8, //可提现金额数
        haicharenshu: 5,  // 还有几人可以提现
        from: '', // 记录分享者来源
        // 记录帮助助力人信息
        userArr:[
          {
            img:require('../../assets/active/morentouxiang.png'),
            // img: 'https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132',
            name: '待邀请'
          },
          {
            img:require('../../assets/active/morentouxiang.png'),
            // img: 'https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132',
            name: '待邀请'
          },
          {
            img:require('../../assets/active/morentouxiang.png'),
            // img: 'https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132',
            name: '待邀请'
          },
          {
            img:require('../../assets/active/morentouxiang.png'),
            // img: 'https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132',
            name: '待邀请'
          },
          {
            img:require('../../assets/active/morentouxiang.png'),
            // img: 'https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132',
            name: '待邀请'
          }
        ],
        // 提现轮播图假数据
        tixianUser:[
          {
            img: require('../../assets/active/face_1.png'),
            name: 'AAA'
          },
          {
            img: require('../../assets/active/face_2.png'),
            name: 'Aimee'
          },{
            img: require('../../assets/active/face_3.png'),
            name: 'Mr. Ma'
          },{
            img: require('../../assets/active/face_4.png'),
            name: 'ohh'
          },{
            img: require('../../assets/active/face_5.png'),
            name: 'pong'
          },{
            img: require('../../assets/active/face_6.png'),
            name: 'Quan、'
          },{
            img: require('../../assets/active/face_7.png'),
            name: '阿甘'
          },{
            img: require('../../assets/active/face_8.png'),
            name: '毛小驴'
          },{
            img: require('../../assets/active/face_9.png'),
            name: '喵咪'
          },{
            img: require('../../assets/active/face_10.png'),
            name: '木公'
          },{
            img: require('../../assets/active/face_11.png'),
            name: '闹腾'
          },{
            img: require('../../assets/active/face_12.png'),
            name: '彭贵宝'
          },{
            img: require('../../assets/active/face_13.png'),
            name: '入魔、'
          },
        ],
        mob: '', // 用户手机号
        computetime: '', // 计时器
        SHOWText: '', // 控制首页显示养卡攻略或真实内容
        SHOW: true, // 控制首页显示养卡攻略或真实内容
        fenxiangImg : '', // 分享者的头像
        arrCode: [
          'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/qrcode.jpg'
        ],  // 点击图片在新窗口打开 所需数据
        jt_title: '交通提额攻略:',
        js_title: '建设提额攻略',
        gs_title: '工商通用攻略：',
        ny_title: '农业提额攻略',
        gd_title: '光大养卡技巧',
        gf_title: '广发养卡技巧',
        zg_title: '中国提额方法',
        xy_title: '兴业提额方法',
        ms_title: '民生提额方法',
        hx_title: '华夏提额方法',
        isLogin: true,
        isActive :false,
        appear:true,
        tips:true,
        phototUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1528106264550&di=635bd54844f92c9672485b5d5f6ba3cc&imgtype=0&src=http%3A%2F%2Fwww.xiazaiba.com%2Fuploadfiles%2Fsub_ico%2F2015%2F0417%2F2015041715312182286.png',
        cardUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1528122362532&di=a15d3f52f9a40864816db75d76e4930b&imgtype=0&src=http%3A%2F%2Fs4.sinaimg.cn%2Fmw690%2F006iRLaxzy73UJHuEO763%26690',
        hotBanks: [], //热门
        noviceCard: [], //
        bigQuota: [],  //
        fastApproval: [], //
        politeCard: [], //
        bannerData: [], //轮播图
        bannerDataTxt: [], //轮播文字
        //分页属性      
        showList:[], //
        cardTips:[], //
        credittips:[], //热门未处理
        searchCondition:{
          t: '',
          page: 0,
          token: '',
          creditid: '',
        },
        pageList: [],
        bottomAllLoaded: false, //是否可以上拉属性，false可以上拉，true为禁止上拉，就是不让往上划加载数据了
        wrapperHeight: 0,
        bottomText: '上拉加载更多',
        bottomDropText: '释放更新',
        showAll: false,　//标记数据是否需要完全显示的属性
        isLoading_hotBank: false,
        isLoading_theme: true,
        isLoading_banner: true,
        isLoading_hotCard: true,
        animate:false,
        translate: 0,
        scrollIcon:'',
        isScrollIcon:'',
        creditHref:'',
        isCredit:'',
        ReachBotton:true,
        regList:{
          mob:'', //手机号、
          chan:'', //渠道号、
          cid:'', //ID、
          cname:'', //名称、
        },
        urlList:{    //url拼接参数
          urlAll:'',             //所有参数
          urlUtm:'',             //通道
          urlCredit:'',          //取现
          urlType:'',            //下载
          urlMob:'',             //手机号
          urlKami:'',            //是否为kamiApp跳转标识符
        },
        onbehalfsource:0,          //0:页面跳转代还-立即查看非原生跳转
        isKami:'',          //1:App-页面-代还-一键导入-账单 0:非 秘App-页面-代还-一键导入-注册下载页
        operationList:{   //记录用户操作接口列表
            type:3,                 //点击(h5),
            mobile:'',                 //手机号、
            channelSign:'',         //渠道号、渠道标识(H5)
            typeId:'',              //相应操作数据id（对应数据的id不存在时可以不传）==>信用ID
            address:'',	            //链接地址（app不需要；H5需要）
        },
        backgroundI1:{
          background:"url("+require('../../assets/1@3x.png')+")",
        },
        back_img1: require('../../assets/1@3x.png'),
        back_img2: require('../../assets/2@3x.png'),
        back_img3: require('../../assets/3@3x.png'),
        showGD: false, // 控制更多和收起
        word1: '更多',
        word2: '收起',
        gengduo: require('../../assets/gengduo@2x.png'),
        shouqi: require('../../assets/shouqi@2x.png'),
        userInfo:{
          username: '',
          avatarUrl: '',
          gender: '',
          province:'',
          city: '',
          openid: '',
          encrydata: '',
          iv: ''
        }
      }
    },
    components: {
      vueTabBar,
      // tab:tab
    },   
    methods: {  
      // 新用户点击开奖获取用户信息，并跳到开奖页
      onGotUserInfo: function(e) {
        let that = this
        // console.log(e)
        // console.log(e.mp.detail.userInfo)    
        if(e.target.userInfo) {
          // console.log('用户已经授权');
          that.userInfo.username= e.mp.detail.userInfo.nickName,
          that.userInfo.avatarUrl= e.mp.detail.userInfo.avatarUrl,
          that.userInfo.gender= e.mp.detail.userInfo.gender,
          that.userInfo.province= e.mp.detail.userInfo.province,
          that.userInfo.city= e.mp.detail.userInfo.city
          that.userInfo.encrydata= e.mp.detail.encryptedData
          that.userInfo.iv= e.mp.detail.iv
          that.isshouquan = true
          wx.login({
            success (res) {       
              if (res.code) {
                //发起网络请求,获取用户openid           
                getUserOpenid(res.code).then(data => {  
                  console.log(data)
                  that.userInfo.openid = data.result.msg                   
                  wx.setStorage({
                    key: 'openID',
                    data: {
                      "openId":data.result.msg
                    }
                  })  
                  // 将用户信息传给后台
                  postUserInfo(that.userInfo).then(res=>{
                    // console.log('上传用户信息返回',res)
                    if(res.result.code == 10000){
                      // !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
                         
                    }else if(res.result.code == 99999){
                      wx.showModal({
                        title: '提示',
                        content: '网络错误，请稍后重试！',
                        showCancel: false,
                        confirmText: '好的',
                        success: function(res) {
                          if (res.confirm) {
                            // console.log('用户点击确定');
                          }
                        }
                      })
                    }
                  })
                  startTask({openid: that.userInfo.openid}).then(res=>{
                    if(res.result.code == 10000 ){
                      that.gettaskinfo()
                      that.showkaijiang = false
                      that.showaward = true
                    } 
                  })           
                })      
              } else {                         
                wx.showModal({
                  title: '提示',
                  content: '网络错误，请稍后重试！',
                  showCancel: false,
                  confirmText: '好的',
                  success: function(res) {
                    if (res.confirm) {
                      console.log('用户点击确定');
                    }
                  }
                })
              }
            }
          })  
        } else {
          console.log('用户拒绝授权');
          //用户拒绝授权
          wx.showModal({
            title: '提示',
            content: '只有授权后才能领红包哦！',
            showCancel: false,
            confirmText: '好的',
            success: function(res) {
              if (res.confirm) {
                console.log('用户点击确定');
              }
            }
          })
        }
      },
      // 已授权用户点击开奖，跳转到开奖页
      toaward(){
        let that = this
        this.showkaijiang = false
        this.showmengban = true
        this.showaward = true
        this.showshare= false
        this.showcomplete= false
        this.showhelphe= false
        this.showsuccess= false
        this.showtixian= false
        this.showphone= false
        this.showjiakefu= false
         wx.getStorage({
            key:'openID',
            success:function(res){ 
              getTaskInfo({openid: res.data.openId}).then(res=>{
              // console.log(res)
                that.award = res.data.coin
              })
          }
        })
        
      },
      // 跳转到分享好友页
      tofenxiang(){
        startTask({openid: this.userInfo.openid}).then(res=>{
          if(res.result.code == 10000 ){
            this.gettaskinfo()
            this.showkaijiang = false
            this.showaward = true
          } 
        })
        // // 用用户openid请求任务状态
        // getTaskInfo({openid:this.userInfo.openId}).then(res => {
        //   console.log('任务状态接口返回',res)
        // })
        clearInterval(this.computetime)
        this.showaward = false
        this.showshare = true
      },
      // 助力人获取用户信息，并跳转到助力完成页
      GotUserInfo(e) {
        let that = this   
        // console.log(e)
        // console.log(e.mp.detail.userInfo)    
        if(e.target.userInfo) {
          // console.log('用户已经授权');
          that.userInfo.username= e.mp.detail.userInfo.nickName,
          that.userInfo.avatarUrl= e.mp.detail.userInfo.avatarUrl,
          that.userInfo.gender= e.mp.detail.userInfo.gender,
          that.userInfo.province= e.mp.detail.userInfo.province,
          that.userInfo.city= e.mp.detail.userInfo.city
          that.userInfo.encrydata= e.mp.detail.encryptedData
          that.userInfo.iv= e.mp.detail.iv
          // that.isshouquan = true
          // console.log('that.userinfo',that.userInfo)
          // 将用户信息传给后台
          postUserInfo(that.userInfo).then(res=>{
            // console.log('上传用户信息返回',res)
            if(res.result.code == 10000){
              // this.showkaijiang = false
              // this.helpHe = true
              // this.showaward = true
              this.isshouquan = true

              // 用户已经上传过信息也会返回99999
            }else if(res.result.code == 99999){
              wx.showModal({
                title: '提示',
                content: '网络错误，请稍后重试！',
                showCancel: false,
                confirmText: '好的',
                success: function(res) {
                  if (res.confirm) {
                    console.log('用户点击确定');
                  }
                }
              })
            }
          })
          // let params = {
          //   tarid: that.iszhuli,
          //   curid: that.userInfo.openid
          // }
          // helpHe(params).then(res => {
          //   console.log(res)
          // })
          // 记录助力人的活动状态，是否已经帮忙助力过
          // this.isshouquan = true
          // this.completezhuli = true   
        } else {
          console.log('用户拒绝授权');
          //用户拒绝授权
          wx.showModal({
            title: '提示',
            content: '只有授权后才能帮好友助力哦！',
            showCancel: false,
            confirmText: '好的',
            success: function(res) {
              if (res.confirm) {
                console.log('用户点击确定');
              }
            }
          })
        }
      },
      // 已授权用户帮别人助力，跳转到助力完成页
      tosuccess(){   
        // console.log('主理人页面的用户信息',this.userInfo)
        // console.log('分享者的openid',this.iszhuli)    
        let that = this  
        wx.getStorage({
          key: 'openID',
          success:function(res){
            let params = {
              tarid: that.iszhuli,
              curid: res.data.openId
            }

            helpHe(params).then(res => {
              console.log('帮助好友助力接口返回',res)
              if(res.result.code == 10000) {
                // console.log('助力成功')
                wx.showToast({
                  title: '助力成功',
                  icon: 'success',
                  duration: 1000
                })
                that.completezhuli = true
                that.showsuccess = true
                that.showmengban = true 
                that.showkaijiang= false
                that.showaward= false
                that.showshare= false
                that.showcomplete= false
                that.showhelphe= false
                that.showtixian= false
                that.showphone= false
                that.showjiakefu= false     
                wx.setStorage({
                  key: that.iszhuli,
                  data: {
                    "openId":that.iszhuli
                  }
                }) 
              } else if(res.result.msg == '您已为好友助力过了'){
                console.log('帮助好友助力，返回99999，已助力过')
                wx.showToast({
                  title: '您已经为好友助力过了,自己也要加油哦！',
                  icon: 'none',
                  duration: 1500
                })
                that.completezhuli = true
                that.showmengban= false 
                that.showkaijiang= false
                that.showaward= false
                that.showshare= false
                that.showcomplete= false
                that.showhelphe= false
                that.showsuccess= false
                that.showtixian= false
                that.showphone= false
                that.showjiakefu= false
                wx.setStorage({
                  key: that.iszhuli,
                  data: {
                    "openId":that.iszhuli
                  }
                }) 
              } else if(res.result.code == 99998) {
                wx.showToast({
                  title: '不能给自己助力哦！',
                  icon: 'none',
                  duration: 1000
                })
                that.showmengban= false // 控制开奖页显隐
                that.showkaijiang= false
                that.showaward= false
                that.showshare= false
                that.showcomplete= false
                that.showhelphe= false
                that.showsuccess= false
                that.showtixian= false
                that.showphone= false
                that.showjiakefu= true  
              } else {
                wx.showModal({
                  title: '提示',
                  content: '网络错误，请稍后重试！',
                  showCancel: false,
                  confirmText: '好的',
                  success: function(res) {
                    if (res.confirm) {
                      console.log('用户点击确定');
                    }
                  }
                })
              }
            })
          }
        })
      },

      // 从助力完成页跳到开奖页
      tokaijiang(params){
        // if(params == 1) {
        //   this.isshouquan = true
        //   this.showmengban = false
        //   this.showkaijiang = false
        //   this.showcomplete = false
        //   this.showshare = false
        //   this.showhelphe = false  
        //   this.showaward = false
        //   this.showsuccess = false
        //   this.showtixian= false
        //   this.showphone= false
        //   this.showjiakefu= false
        //   this.gettaskinfo()
        // } else {
          this.showkaijiang = false
          // this.showmengban = true
          this.showcomplete = false
          this.showshare = false
          this.showhelphe = false  
          this.showaward = false
          this.showsuccess = false
          this.showtixian= false
          this.showphone= false
          this.showjiakefu= false
          
          this.getRWstatus(1)
        // }
      },
      // 获取任务信息
      gettaskinfo(open){
        if(open){
          getTaskInfo({openid: open}).then(res=>{
            // console.log('分享者的信息',res)
            this.fenxiangImg = res.data.headurl
            this.fenxiangname = decodeURI(res.data.usname)
            // console.log(this.fenxiangname)
          })
        } else {
          let timestamp = Date.parse(new Date()) + "0"
          let xianziatime = timestamp.substring(0,10)
          let that = this
          // console.log('现在时间',xianziatime)
          wx.getStorage({
            key:'openID',
            success:function(res){  
              getTaskInfo({openid: res.data.openId}).then(res=>{
                // console.log('活动信息',res)
                wx.getStorage({
                  key: 'lingqurenshu',
                  success:function(res){
                    that.peoplenum = res.data.num
                    let num1 = parseInt(res.data.num + 5) 
                    wx.setStorage({
                      key: 'lingqurenshu',
                      data: {
                        "num": num1
                      }
                    })
                  },
                  fail: function(res){
                    that.peoplenum = 54687
                    wx.setStorage({
                      key: 'lingqurenshu',
                      data: {
                        "num": that.peoplenum
                      }
                    })
                  },
                })
                that.award = res.data.coin
                that.startTime = res.data.stime
                that.userImg = res.data.headurl

                that.helpNum = res.data.peoples
                if(res.data.peoples == 5){
                  that.complete_ttt = '你的好友真给力!'
                } else if(5 <res.data.peoples <= 20) {
                  that.complete_ttt = '你的好友好多呀！'
                } else if(20 <res.data.peoples <= 50) {
                  that.complete_ttt = '哟，你真的很受欢迎！'
                } else if(50 <res.data.peoples <= 100) {
                  that.complete_ttt = '你的人气真让人嫉妒！'
                } else if(100 <res.data.peoples ) {
                  that.complete_ttt = '你的好友遍布天下！'
                } 
                that.userName = decodeURI(res.data.usname)
                that.tixianNum = res.data.coin / 100
                that.mob = res.data.mob
                if(res.data.peoplesinfo != ' '){
                  let json = JSON.parse(res.data.peoplesinfo)
                  // console.log("json",json)
                  for(let i = 0; i< json.length; i++){
                    if(json[i].fheadurl == null || json[i].fheadurl== ''){
                      that.userArr[i].img='https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132'
                    } else{
                      that.userArr[i].name = decodeURI(json[i].fname)
                      that.userArr[i].img = json[i].fheadurl
                    }
                    
                  }
                  // console.log('userArr',that.userArr)
                } 
                if(res.data.peoples >= 1){
                  that.haicharenshu = 0
                  that.showmengban = true
                  that.showcomplete = true
                  that.showaward = false
                  that.showkaijiang = false
                  that.showshare = false
                  that.showhelphe = false
                  that.showsuccess = false 
                  that.showtixian= false
                  that.showphone= false
                  that.showjiakefu= false
                  if(that.endtime==null ||that.endtime==''){
                    that.endtime = 1546271999
                  } 
                  
                  let times = that.endtime - xianziatime
                  that.times.secs = parseInt(times%60) 
                  that.times.mins = parseInt(times/60%60)
                  that.times.hours = parseInt(times/3600%24)
                  that.times.days = parseInt(times/86400)
                 
                  if(that.times.secs<10){
                    that.times.secs = "0" + that.times.secs
                  }
                  if(that.times.mins<10){
                    that.times.mins = "0" + that.times.mins
                  }
                  if(that.times.hours<10){
                    that.times.hours = "0" + that.times.hours
                  }

                  that.computetime = setInterval(()=>{
                    // this.times.secs += 1
                    that.times.secs = parseInt(that.times.secs) - 1
                    // console.log('secs',that.times.secs)

                    if(that.times.secs == 0){
                      // console.log('22222')
                      that.times.secs = 60
                      that.times.mins = parseInt(that.times.mins) - 1
                      if(that.times.mins == 0){
                        that.times.mins = 60
                        that.times.hours = parseInt(that.times.hours) - 1
                        if(that.times.hours = -1){
                          that.times.hours = 23
                          that.times.days = parseInt(that.times.days) - 1
                        } else if(that.times.hours<10){
                          that.times.hours = "0"+that.times.hours
                        }
                      } else if(that.times.mins<10){
                        that.times.mins = "0"+that.times.mins
                      }
                    } else if(that.times.secs<10){
                      that.times.secs = "0"+that.times.secs
                    }
                  },1000)
                } else {  
                  that.haicharenshu = 5 - res.data.peoples
                  that.showmengban = true
                  that.showshare = true
                  that.showaward = false
                  that.showkaijiang = false
                  that.showcomplete = false
                  that.showhelphe = false
                  that.showsuccess = false
                  that.showtixian= false
                  that.showphone= false
                  that.showjiakefu= false
                  if(that.endtime==null ||that.endtime==''){
                    that.endtime = 1546271999
                  } 
                    let times = that.endtime - xianziatime
                    that.times.secs = parseInt(times%60) 
                    that.times.mins = parseInt(times/60%60)
                    that.times.hours = parseInt(times/3600%24)
                    that.times.days = parseInt(times/86400)
                    // console.log('xianzai',xianziatime)
                    // console.log('times',times)
                    // console.log('secs',that.times.secs)
                    // console.log('mins',that.times.mins)
                    // console.log('hours',that.times.hours)
                    // console.log('days',that.times.days)
                    if(that.times.secs<10){
                      that.times.secs = "0" + that.times.secs
                    }
                    if(that.times.mins<10){
                      that.times.mins = "0" + that.times.mins
                    }
                    if(that.times.hours<10){
                      that.times.hours = "0" + that.times.hours
                    }
                    that.computetime = setInterval(()=>{
                    // this.times.secs += 1
                    that.times.secs = parseInt(that.times.secs) - 1
                    // console.log('secs',that.times.secs)

                    if(that.times.secs == 0){
                      // console.log('22222')
                      that.times.secs = 60
                      that.times.mins = parseInt(that.times.mins) - 1
                      if(that.times.mins == 0){
                        that.times.mins = 60
                        that.times.hours = parseInt(that.times.hours) - 1
                        if(that.times.hours = -1){
                          that.times.hours = 23
                          that.times.days = parseInt(that.times.days) - 1
                        } else if(that.times.hours<10){
                          that.times.hours = "0"+that.times.hours
                        }
                      } else if(that.times.mins<10){
                        that.times.mins = "0"+that.times.mins
                      }
                    } else if(that.times.secs<10){
                      that.times.secs = "0"+that.times.secs
                    }
                  },1000)
                }
              })
            }
          })
        }
      },
      // 获取任务状态
      getRWstatus(option){    
        let that = this 
        if(option){
          // 获取任务状态
          wx.getStorage({
            key:'openID',
            success:function(res){    
              // console.log(res)
              if(res.data.openId){
                let openID = res.data.openId
                // 获取任务状态
                getRWInfo({openid: res.data.openId}).then(res => {  
                  // console.log('任务状态',res) 
                  // 未授权状态
                  if(res.data.peoplestatus == 0){
                    // console.log('isshouquan',res.data.peoplestatus)
                    that.isshouquan = false
                    that.showmengban = true
                    that.showkaijiang = true
                    that.showaward = false
                    that.showshare = false
                    that.showcomplete = false
                    that.showhelphe = false
                    that.showsuccess = false
                    that.showjiakefu= false
                    that.showtixian= false
                    that.showphone= false
    
                  } else if(res.data.peoplestatus == 1){
                    that.isshouquan = true
                    // 若任务未激活
                    if(res.data.status == 0){
                      that.showmengban = true
                      that.showkaijiang = true
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                      // 任务已激活
                    } else if(res.data.status == 1){  
                      // console.log('aaa')
                      clearInterval(that.computetime) 
                        that.showmengban = false
                        that.showkaijiang = false
                        that.showaward = false
                        that.showshare = false
                        that.showcomplete = false
                        that.showhelphe = false
                        that.showsuccess = false
                        that.showjiakefu= false
                        that.showtixian= false
                        that.showphone= false
                        that.gettaskinfo()
                      // 任务已完成
                    } else if(res.data.status == 2){
                      that.showmengban = false
                      that.showkaijiang = false
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                      // 活动已结束
                    } else if(res.data.status == 3){
                      that.showmengban = false
                      that.showkaijiang = false
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                    } 
                  }     
                })
              }else{
            
              }
            },
          })
        } else {
          // 获取任务状态
          wx.getStorage({
            key:'openID',
            success:function(res){    
              // console.log('助力人的openid',res)
              if(res.data.openId){
                let openID = res.data.openId
                // 获取任务状态
                getRWInfo({openid: res.data.openId}).then(res => {  
                  // console.log('助力人任务状态',res) 
                  // 未授权状态
                  if(res.data.peoplestatus == 0){
                    // console.log('isshouquan',res.data.peoplestatus)
                    that.isshouquan = false
                    that.showmengban = true
                    that.showkaijiang = true
                    that.showaward = false
                    that.showshare = false
                    that.showcomplete = false
                    that.showhelphe = false
                    that.showsuccess = false
                    that.showjiakefu= false
                    that.showtixian= false
                    that.showphone= false

                  } else if(res.data.peoplestatus == 1){
                    // console.log('bbb')
                    that.isshouquan = true
                    // 若任务未激活
                    if(res.data.status == 0){
                      that.showmengban = true
                      that.showkaijiang = true
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                      // 任务已激活
                    } else if(res.data.status == 1){  
                      // clearInterval(that.computetime) 
                        that.showmengban = false
                        that.showkaijiang = false
                        that.showaward = false
                        that.showshare = false
                        that.showcomplete = false
                        that.showhelphe = false
                        that.showsuccess = false
                        that.showjiakefu= false
                        that.showtixian= false
                        that.showphone= false
                        // that.gettaskinfo()
                      // 任务已完成
                    } else if(res.data.status == 2){
                      that.showmengban = false
                      that.showkaijiang = false
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                      // 活动已结束
                    } else if(res.data.status == 3){
                      that.showmengban = false
                      that.showkaijiang = false
                      that.showaward = false
                      that.showshare = false
                      that.showcomplete = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone= false
                    } 
                  }     
                })
              }else{
    
              }
            },
          })
        } 
      },
      // 从浮窗进入活动页
      toactive(optiom){
        // console.log(this.computetime)
        clearInterval(this.computetime)
        // 助力人，走一波逻辑
        if(this.iszhuli){
          // 助力完成，显示它自己的任务状态
          if(this.completezhuli){
            // console.log('助力完成')
            clearInterval(this.computetime)
            // this.showmengban = true
            this.showkaijiang = false  
            this.showshare = false
            this.showhelphe = false
            this.showaward = false
            this.showcomplete = false
            this.showsuccess = false
            this.showjiakefu= false
            this.showtixian= false
            this.showphone= false
            this.getRWstatus(1)
          // 助力未完成，显示帮好友助力页面
          } else {
            this.showmengban = true
            this.showkaijiang = false  
            this.showshare = false
            this.showhelphe = true
            this.showkaijiang = false
            this.showaward = false
            this.showcomplete = false
            this.showsuccess = false
            this.showjiakefu= false
            this.showtixian= false
            this.showphone= false
          }
        // 非助力人，获取任务状态
        } else {
          // this.showkaijiang = true
          // this.showmengban = true
          // 获取任务状态
          this.getRWstatus(1)
          // this.gettaskinfo()
        }
      },
      
      // 去提现页面
      totixian(){
        this.showmengban= true, // 控制开奖页显隐
        this.showkaijiang= false,
        this.showaward= false,
        this.showshare= false,
        this.showcomplete= false,
        this.showhelphe= false,
        this.showsuccess= false
        this.showtixian = false
        this.showphone = false
        this.showjiakefu= false

        if(this.mob == ' '){
          this.showtixian= true
          this.showphone = false
        } else {
          this.showphone = true
          this.showtixian= false
        }
      },
      // 提现页验证码计时
      getcode(){
        // console.log(this.phoneNum)
        let reg=/^((1[3,5,6,8][0-9])|(14[5,7])|(17[0,6,7,8])|(19[7]))\d{8}$/;
        if(!reg.test(this.phoneNum)){
          wx.showToast({
            title: '手机号错误',
            icon: 'loading',
            duration: 500
          })
        } else{
          getCode({mob:this.phoneNum}).then(res => {
            console.log(res)
          })
          this.codejishi = false
          this.codetime = setInterval(()=>{
            // this.times.secs += 1
            this.codeTime = parseInt(this.codeTime) - 1
            
            if(this.codeTime<10){
              this.codeTime = "0"+ this.codeTime
            } 
            if (this.codeTime == "00"){
              this.codejishi = true
              this.codeTime = 60
              clearInterval(this.codetime)
            }
            // console.log(this.codeTime)
          },1000)
        }  
      },  
      // 绑定电话号码
      bindphone(){
        let that = this
        let params ={
          openid: '',
          mob: '',
          code: ''
        }
        params.openid = this.userInfo.openid
        params.mob = this.phoneNum
        params.code = this.QRcode
        // console.log(params)
        if(params.mob=='' ||params.code==''){
          wx.showToast({
            title: '手机号或验证码错误',
            icon: 'none',
            duration: 500
          })
        } else {
          bandPhone(params).then(res => {
            // console.log(res)
            if(res.result.code == 10000){
              wx.showToast({
                title: '绑定成功',
                icon: 'success',
                duration: 500
              })
              that.showmengban= true // 控制开奖页显隐
              that.showkaijiang= false
              that.showaward= false
              that.showshare= false
              that.showcomplete= false
              that.showhelphe= false
              that.showsuccess= false
              that.showtixian= false
              that.showphone= false
              that.showjiakefu= true
            } else {
              wx.showToast({
                title: '手机号或验证码错误',
                icon: 'none',
                duration: 500
              })
            }
          })
        } 
      },
      // 加客服页
      tojiakefu(){
        this.showkaijiang= false,
        this.showaward= false,
        this.showshare= false,
        this.showcomplete= false,
        this.showhelphe= false,
        this.showsuccess= false,
        this.showtixian= false,
        this.showphone= false,
        this.showjiakefu= true

        // wx.navigateTo({ 
        //   url: "/pages/jiakefu/main" 
        // });
      },
      // 取消活动页面的显示
      toquxiao(){
        this.showmengban= false 
        this.showkaijiang= false 
        this.showaward= false
        this.showshare= false
        this.showcomplete= false
        this.showhelphe= false
        this.showsuccess= false
        this.showtixian= false
        this.showphone= false
        this.showjiakefu= false
      },
      // 加客服页点击图片在新窗口打开
      previewImage: function (e) { 
        let that = this 
        let current=e.target.dataset.src;
        // console.log(current)
		    wx.previewImage({
          current: 'http://download.pcuion.com/app2_0/wxqcode.jpg', // 当前显示图片的http链接
          urls: this.arrCode // 需要预览的图片http链接列表
        })
        wx.getImageInfo({// 获取图片信息（此处可不要）
          src: 'http://download.pcuion.com/app2_0/wxqcode.jpg',
          success: function (res) {
            // console.log(res.width)
            // console.log(res.height)
          }
        })

      },
      // 跳转到新的研究玩卡页
      toyanjiuwanka(){
        wx.navigateTo({ 
          url: "/pages/yanjiuwanka/main" 
        });
      },
      toyongkajingyan(){
        wx.navigateTo({ 
          url: "/pages/yongkajingyan/main" 
        });
      },
      // 跳转到活动详情
      toactiveshuoming() {
        wx.navigateTo({ 
          url: "/pages/activeshuoming/main" 
        });
      },
      // 跳转到助力人详情页
      tozhulixiangqing(){
        wx.navigateTo({ 
          url: "/pages/zhulixiangqing/main" 
        });
      },
      // 跳转到代还页
      toOnbehalf() {
        wx.navigateTo({ 
          url: "/pages/onBehalf/main" + '?utm_source='
           + this.urlList.urlUtm + '&mob' + this.urlList.urlMob 
        });
      },
      // 跳转到进度查询页
      toprogresscheck() {
        wx.navigateTo({ 
          url: "/pages/progresscheck/main" 
        });
      },
      // 跳转到激活页
      toActivation() {
        wx.navigateTo({ 
          url: "/pages/activation/main" 
        });
      },
      // 跳转到 中心
      tofiltercard(){
        wx.navigateTo({ 
          url: "/pages/filtercard/main" 
        });
      },
      // 跳转到热门详情页
      toHotbank(item){
        wx.navigateTo({ 
          url: "/pages/hotDetails/main?utm_source=" + this.urlList.urlUtm + '&mob=' + this.urlList.urlMob + '&bankid=' + item.bankid + '&bankname=' + item.bankname + '&bankcontent=' + item.bankcontent + '&logo=' + item.banklogo   
        });
      },
      // 跳转到新手页
      toNovicecard(){
        wx.navigateTo({ 
          url: "/pages/noviceCard/main?utm_source=" + this.urlList.urlUtm + '&mob' + this.urlList.urlMob
        });
      },
      // 跳转到大额度页
      tolargemonute(){
        wx.navigateTo({ 
          url: "/pages/largemounte/main?utm_source=" + this.urlList.urlUtm + '&mob' + this.urlList.urlMob
        });
      },
      // 跳转到审批快页
      tofastproval(){
        wx.navigateTo({ 
          url: "/pages/fastapproval/main?utm_source=" + this.urlList.urlUtm + '&mob' + this.urlList.urlMob
        });
      },
      // 跳转到有礼页
      topolitecard(){
        wx.navigateTo({ 
          url: "/pages/politecard/main?utm_source=" + this.urlList.urlUtm + '&mob' + this.urlList.urlMob
        });
      },
      // 跳转到轮播图详细页
      toswiperdetails(url,index,title){
        switch(index)
        {
        case 0:
          wx.navigateTo({ 
            url: "/pages/activation/main"
          });
          break;
        case 1:
          let pages = getCurrentPages();
          let currPage = pages[pages.length - 1];   //当前页面
          let prevPage = pages[pages.length - 2];  //上一个页面
          currPage.setData({
            urlStr: url
          });
          wx.navigateTo({ 
              url: `/pages/link/main?title=${title}`
          });
          break;
        case 2:
        // console.log(tourl)
          wx.navigateTo({ 
            url: "/pages/cardraiders/main"
          });
          break;
        }
      },
      // 禁止小的轮播文字滑动
      stopTouchMove(){
        return false
      },
      // 切换showList的值
      toggleShowList(){
        this.showAll=!this.showAll
        this.showGD = !this.showGD
        if(this.showAll){
          this.showList = []
          this.showList = this.hotBanks
        }else{
          if(this.hotBanks.length > 6){
            this.showList = []
            for(let i = 0; i < 6; i++){
              this.showList.push(this.hotBanks[i]);
            }
          }else{
            this.showList = this.hotBanks;
          }
        }
      },
      // 页面加载时查询数据
      loadPageList(){
        this.searchCondition.t = (new Date()).valueOf();  //获取当前时间戳
        this.searchCondition.token = md5(md5((new Date()).valueOf() + '@kami2018'));  //生成token
        this.searchCondition.page = 1;
        getHotCard(this.searchCondition).then(data => {
          if(data.result.code == 10000){
            for(let j = 0; j< data.data.length; j++){
              this.pageList.push(data.data[j]);
            }
            // console.log(this.pageList)
            this.isLoading_hotCard = false;
            // 为的tips赋值
            for(let i=0;i<this.pageList.length;i++){
              this.credittips.push(data.data[i].credittips) 
              this.cardTips.push(this.credittips[i].split(','))
              // this.cardTips.push(this.pageList.credittips.split(',')) 
            }
          }else if(data.result.code == 99996) {
            this.bottomText = '没有更多了';
            this.bottomDropText = '没有更多了';
            this.ReachBotton=false
          }
         /* else {
            Toast({message:'正在加载中。。。',duration: 500});
          }*/
        }).catch(err => {
          console.log(err);
         /* Toast({message:'正在加载中。。。',duration: 500});*/
        });
      },
      //统计热点击量
      hotdetailsNum(index){
          this.regList.mob=this.urlList.urlMob;
          this.regList.chan=this.urlList.urlUtm;
          this.regList.cid=this.pageList[index].creditid;
          this.regList.cname=this.pageList[index].creditname;
          registerHref(this.regList);
          this.operationList.mobile=this.$route.query.mob;
          this.operationList.channelSign=this.$route.query.utm_source;
          this.operationList.typeId=this.pageList[index].creditid;
          this.operationList.address=window.location.href;
          userOperation(this.operationList);
      },
      // 跳转到中间页
      tokefu(title,url){
        let pages = getCurrentPages();
        let currPage = pages[pages.length - 1];   //当前页面
        let prevPage = pages[pages.length - 2];  //上一个页面
        currPage.setData({
          urlStr: url
        });
        wx.navigateTo({ 
            url: `/pages/link/main?title=${title}`
        });
      },  
      // 第一次加载数据
      getFirst(option){
        if(option){

        } else {
          this.pageList = [] 
          this.loadPageList();
        }
        this.showGD = false
        this.showAll = false
        this.showList = []
        // 页面展示时，清空热门 卡数据，并重新请求
        this.isLoading_hotCard = false
        this.word= '更多'
        this.isLoading_hotBank = true
        this.imgUrl= require('../../assets/gengduo@2x.png')
        // 获取热门所需数据
        getHotBankInfoList().then(data => {
          // console.log('执行',data)
          if(data.result.code == 10000){
            this.showList = []
            this.hotBanks = data.data;
            // 第一次请求页面，给热门6个值
            if(this.hotBanks.length > 6){
              for(let i = 0; i < 6; i++){
                this.showList.push(this.hotBanks[i]);
              }
            }else{
              this.showList = this.hotBanks;
            }
            this.isLoading_hotBank = false;
          }else {
            this.isLoading_hotBank = false;
            // Toast({message:'正在加载中。。。',duration: 500});
          }
        }).catch(err=>{
          console.log(err)
          this.isLoading_hotBank = false;
          // Toast({message:'正在加载中。。。',duration: 500});
        });
        // this.isLoading_hotBank = true

        //加载主题精选时所需数据
        getTopicSelect().then(data => {
          if(data.result.code == 10000){
            this.noviceCard = data.data[0];
            this.bigQuota = data.data[1];
            this.fastApproval = data.data[2];
            this.politeCard = data.data[3];
            this.isLoading_theme = false;
          }else {
            this.isLoading_theme = false;
            // Toast({message:'正在加载中。。。',duration: 500});
          }
        }).catch(err => {
          console.log(err);
          this.isLoading_theme = false;
          // Toast({message:'正在加载中。。。',duration: 500});
        })
        //加载轮播图时所需数据
        getBannerImg().then(data => {
          if(data.result.code == 10000){
            this.bannerData = data.data;
            // console.log(this.bannerData)
            this.isLoading_banner = false;
          }else {
            this.isLoading_banner = false;
            // Toast({message:'正在加载中。。。',duration: 500});
          }
        }).catch(err => {
          console.log(err);
          this.isLoading_banner = false;
          // Toast({message:'正在加载中。。。',duration: 500});
        })

        //加载轮播文字时所需数据
        getBannerTxt().then(data => {
          if(data.result.code == 10000){
            this.bannerDataTxt = data.data;

            this.isLoading_banner = false;
          }else {
            this.isLoading_banner = false;
            // Toast({message:'正在加载中。。。',duration: 500});
          }
        }).catch(err => {
          console.log(err);
          this.isLoading_banner = false;
          // Toast({message:'正在加载中。。。',duration: 500});
        }) 
      },
      // 设置已领取红包人数
      setlingqurenshu(){
        let that = this
        wx.getStorage({
          key: 'lingqurenshu',
          success:function(res){
            let num1 = parseInt(res.data.num + 5) 
            wx.setStorage({
              key: 'lingqurenshu',
              data: {
                "num": num1
              }
            })
          },
          fail:function(res){
            let num = Math.floor(Math.random()*50000) +50000
            // console.log('num',num)
            // console.log('获取时间失败',res)
            wx.setStorage({
              key: 'lingqurenshu',
              data: {
                "num": num
              }
            })
          }
        })
      },  
      // 判断是否超过两小时
      judgeTime(){
        let that = this
        let timestamp = Date.parse(new Date()) + "0"
        let xianziatime = timestamp.substring(0,10)
        // console.log('现在时间',xianziatime)
        wx.getStorage({
          key: 'time',
          success:function(res){
            // console.log('获取时间storage',res)
            if(xianziatime - res.data.time > 1200) {
              // console.log('超过二十分钟，重新请求')
              wx.setStorage({
                key: 'time',
                data: {
                  "time": xianziatime
                }
              })
              that.getcontent()
            } else {
              // console.log('未超过2小时')
            }
          },
          fail:function(res){
            // console.log('获取时间失败',res)
            that.getcontent()
            wx.setStorage({
              key: 'time',
              data: {
                "time": xianziatime
              }
            })
          }
        })
      },
      // 判断是否显示真正内容
      getcontent(){
        let that = this
        getContent().then(data => {
          // console.log('调用一次',data)
          this.endtime = data.end
          wx.setStorage({
            key: 'ENDTIME',
            data: {
              "time": this.endtime
            }
          })

          this.SHOWText = data.content  
          if(this.SHOWText === 'abcdefg'){
            wx.setStorage({
              key: 'SHOW',
              data: {
                "show": true
              }
            })
            this.SHOW = true
          } else {
            that.SHOW = false
            this.getFirst(1)
            wx.setStorage({
              key: 'SHOW',
              data: {
                "show": false
              }     
            }) 
            
          }
        })   
      },
      // 未显示的跳转到养卡攻略详情页
      tocardraidersdetails(titles,bankNum){
        // console.log(titles,bankNum)
        wx.navigateTo({ 
          url: "/pages/cardraidersdetails/main?title=" + titles + '&bankNo=' + bankNum
        });
      }, 
      // 未显示的跳转到攻略页
      toGonglue(){
        wx.navigateTo({ 
          url: "/pages/cardraiders/main"
        });
      }
    },
    onLoad(options) {  
      let that = this
      // console.log('option',options)
      if(options.scene){
        // let scene=decodeURIComponent(options.scene);
        this.iszhuli= options.scene
        //&是我们定义的参数链接方式
        // this.iszhuli=options.scene.split("&")[0];
        // let recommendId=options.scene.split('&')[1];
        //其他逻辑处理。。。。。
      } else {
        this.iszhuli = options.userId; 
        this.from = options.from
      }  
      this.secondxianshi = false 
      this.setlingqurenshu()
      this.judgeTime()
                
    },
    //页面设置转发功能
    onShareAppMessage: function (res) {
      return {
        title: `你的好友正在红包接龙，他已抢到${this.tixianNum}元，快来支援他！`,
        imageUrl: 'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/share_r.png',
        path: `/pages/index/main?userId=${this.userInfo.openid}&from=1`
      }
    },
    onShow(){ 
      this.showGD = false
      this.showAll = false
      this.showList = []
      // 页面展示时，清空热门 卡数据，并重新请求
      this.isLoading_hotCard = false
      this.pageList = []
      let that = this
        
      this.showmengban = false  
      this.showkaijiang = false
      this.showaward = false
      this.showshare = false
      this.showcomplete = false
      this.showhelphe = false
      this.showsuccess = false
      this.showjiakefu= false
      this.showtixian= false
      this.showphone = false
      
      // 是助力人
      if(this.iszhuli){   
        wx.login({
          success (res) {       
            if (res.code) {
              //发起网络请求,获取用户openid           
              getUserOpenid(res.code).then(data => {  
                // that.userInfo.openid = data.result.msg                   
                wx.setStorage({
                  key: 'openID',
                  data: {
                    "openId":data.result.msg
                  }
                }) 
                wx.getStorage({
                  key:'openID',
                  success:function(res){
                    // 助力人点击自己的分享
                    if(res.data.openId == that.iszhuli){
                      that.showmengban = false
                      that.showcomplete = false
                      that.showaward = false
                      that.showkaijiang = false
                      that.showshare = false
                      that.showhelphe = false
                      that.showsuccess = false
                      that.showjiakefu= false
                      that.showtixian= false
                      that.showphone = false
                      that.completezhuli = true
                    } else {
                      // 获取助力人的授权状态
                      getRWInfo({openid: res.data.openId}).then(res => { 
                        // console.log('主理人',res)
                        // 助力人未授权
                        if(res.data.peoplestatus == 0){
                          // console.log('isshouquan',res.data.peoplestatus)
                          that.isshouquan = false
                          that.showmengban = true
                          that.showkaijiang = false
                          that.showaward = false
                          that.showshare = false
                          that.showcomplete = false
                          that.showhelphe = true
                          that.showsuccess = false
                          that.showjiakefu= false
                          that.showtixian= false
                          that.showphone = false
                          that.gettaskinfo(that.iszhuli)
                          // 助力人已授权
                        } else if(res.data.peoplestatus == 1){
                          that.isshouquan = true
                          console.log('secondxianshi',that.secondxianshi)   
                          if(that.secondxianshi == true){
                            that.showmengban = false
                            that.showkaijiang = false
                            that.showaward = false
                            that.showshare = false
                            that.showcomplete = false
                            that.showhelphe = false
                            that.showsuccess = false
                            that.showjiakefu= false
                            that.showtixian= false
                            that.showphone = false
                          } else {               
                            wx.getStorage({ 
                              key: that.iszhuli,
                              // 找到了 说明已经帮他授权过
                              success:function(res){
                                console.log('onload助力')
                                wx.showToast({
                                  title: '您已经为好友助力过了,自己也要加油哦！',
                                  icon: 'none',
                                  duration: 1500
                                })
                                that.isshouquan = true
                                that.showmengban = false
                                that.showshare = false
                                that.showhelphe = false
                                that.showaward = false
                                that.showkaijiang = false
                                that.showsuccess = false
                                that.showjiakefu= false
                                that.showtixian= false
                                that.showphone = false
                                that.completezhuli = true
                                that.secondxianshi = true  
                                // console.log('',that.secondxianshi)
                              },
                              // 没找到，说明未帮人助力过，或缓存被清空
                              fail:function(res){
                                that.isshouquan = true
                                that.showmengban = true
                                that.showshare = false
                                that.showhelphe = true
                                that.showaward = false
                                that.showkaijiang = false
                                that.showshare = false
                                that.showsuccess = false
                                that.showjiakefu= false
                                that.showtixian= false
                                that.showphone = false
                                // console.log('助力人的openid',that.iszhuli)
                                that.gettaskinfo(that.iszhuli)

                              } 
                            })  
                          }
                        }
                        
                      })
                    }
                  }
                })  
              })      
            } else {            
              console.log('助力人openid获取失败')
            }   
          }   
        })
      // 不是助力人
      } else {
        wx.login({
          success (res) {       
            if (res.code) {
              //发起网络请求,获取新用户openid           
              getUserOpenid(res.code).then(data => {  
                that.userInfo.openid = data.result.msg                   
                wx.setStorage({
                  key: 'openID',
                  data: {
                    "openId":data.result.msg
                  }
                }) 
                that.getRWstatus()
              })      
            } else {               
            }
          }
        })
      }  
      wx.getStorage({ 
        key: 'SHOW',
        success:function(res){
          that.SHOW = res.data.show
          if(!that.SHOW){
            that.getFirst()
          }
        },
        fail:function(res){
        }
      })
      
      // 用于tabbar判断
      this.selectNavIndex = 0
    }, 
    // 触底刷新
    onReachBottom() {
        if(this.isLoading_hotCard){
          this.loadPageList()
          return false
        }else{  
          this.searchCondition.page = parseInt(this.searchCondition.page + 1);
        }   
      //查询数据
        this.searchCondition.t = (new Date()).valueOf();  //获取当前时间戳
        this.searchCondition.token = md5(md5((new Date()).valueOf() + '@kami2018')); 
        // 获取热门  卡的信息
        getHotCard(this.searchCondition).then(data => {    
          if(data.result.code == 10000){
            for(let j = 0; j< data.data.length; j++){
              this.pageList.push(data.data[j]);
              this.credittips.push(data.data[j].credittips)
            }
            // console.log('111',this.pageList)
            // 为 卡的tips赋值
            for(let i=0;i<this.pageList.length;i++){
              this.cardTips.push(this.credittips[i].split(','))
              // this.cardTips.push(this.pageList.credittips.split(',')) 
            }
            this.isLoading_hotCard = false;
            // console.log(this.credittips)
            // console.log(this.cardTips)
          }else if(data.result.code == 99996) {
            this.bottomText = '没有更多了';
            this.bottomDropText = '没有更多了';
            this.ReachBotton=false
          }
          else if(data.result.code == 99999){
            // this.loadPageList()
          }
        }).catch(err => {
          console.log(err);
         /* Toast({message:'正在加载中。。。',duration: 500});*/
        });    
    },   
  } 
</script>

<style lang='scss' scoped>

.card {
  overflow: auto;
  background: #fff;
  -webkit-overflow-scrolling: touch;
  padding: 0;
  margin-bottom: 100rpx;
  .active_fuchuang{
    position: fixed;
    right: 20rpx;
    bottom: 15%;
    width: 176rpx;
    height: 186rpx;
    z-index: 8;
    img{
      width: 100%;
      height: 100%;
    }
  }
  .kaijiang{
    z-index: 10;
    // max-width: 600rpx;
    width: 750rpx;
    height: 953rpx;
    position: fixed;
    // left: 75rpx;
    top: 24rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 102%;
      top: -12rpx;
      left: -8rpx;
    }
    
    .kaijiang_btn {
      width: 256rpx;
      height: 268rpx;
      position: absolute;
      top: 354rpx;
      // bottom: 0;
      left: 248rpx;
      // right: 0;
      z-index: 11;
      button{
        z-index: 12;
        width: 100%;
        height: 100%;
        padding: 0;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      .kaijiang_button {
        width: 100%;
      }
    }
    .kaijiang_title1{
      position: absolute;
      width: 350rpx;
      height: 40rpx;
      left: 202rpx;
      top: 630rpx;
      p{
        color: #FCD514;
        font-size: 21px;
      }
    }
    .kaijiang_title2{
      position: absolute;
      width: 226rpx;
      height: 51rpx;
      left: 264rpx;
      top: 694rpx;
      p{
        color: #FCD514;
        font-family:PingFangSC-Semibold;
        font-weight:500;
        font-size: 26px;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .award{
    z-index: 10;
    width: 613rpx;
    height: 971rpx;
    position: fixed;
    left: 66rpx;
    top: 41rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .award_title{
      position: absolute;
      width: 452rpx;
      top: 570rpx;
      left: 93rpx;
      // right: 93rpx;
      
      p:nth-of-type(1){
        font-size: 29px;
        color: #FCD514;
      }
      p:nth-of-type(2){
        margin-top: 10rpx;
        font-size: 11px;
        color: #FCD514;
      }
    }
    .award_rule{
      position: absolute;
      top: 299rpx;
      left: 506rpx;
      width: 104rpx;
      height: 61rpx;
      img{
        width: 100%;
      }
    }
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    .award_btn {
      width: 434rpx;
      height: 76rpx;
      position: absolute;
      top: 724rpx;
      left: 98rpx;
      z-index: 11;
      .award_button{
        width: 100%;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .share{
    z-index: 10;
    width: 604rpx;
    height: 1003rpx;
    position: fixed;
    left: 79rpx;
    top: 5rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center; 
    .share_swiper{
      position: absolute;
      font-size: 10px;
      color: #F22216;
      top: 80rpx;
      left: 60rpx;
      width: 350rpx;
      height: 42rpx;
      z-index: 12;
      text-align: left;
      float: left;    
      swiper-item{
        height: 42rpx;
      }
      img{
        border-radius: 50%;
        display: inline-block;
        vertical-align: top;
        width: 30rpx;
        height: 30rpx;
        margin-right: 8rpx;
      }
    }
    .to_share_right{
      position: absolute;
      top: 62rpx;
      right: 30rpx;
      width: 106rpx;
      height: 70rpx;
      z-index: 12;
      .share_button{
        z-index: 12;
        position: absolute;
        top: 0;
        right: 0; 
        height: 60rpx;
        width: 100rpx; 
        opacity: 0;    
        padding: 0;    
      }
      .share_right{
        width: 100%;
        position: absolute;
        top: 0;
        right: -1rpx;
      }
    }
    .share_userInfo{
      position: absolute;
      width: 350rpx;
      height: 260rpx;
      left: 140rpx;
      top: 128rpx;
      .user_img{
        width: 126rpx;
        height: 126rpx;
        border-radius: 50%;
        margin-bottom: 20rpx;
      }
      p{
        font-size: 24px;
        color: #F22216;
        font-weight: 600;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      p:nth-of-type(1){
        margin-top: -15rpx;
        font-size: 24px;
        color: #F22216;
        margin-bottom: 8rpx;
      }
      p:nth-of-type(2){
        // margin-top: -5rpx;
        font-size: 24px;
        color: #F22216;
      }
    }
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    .share_main{
      text-align: center;
      width: 400rpx;
      height: 120rpx;
      left: 76rpx;
      top: 532rpx;
      z-index: 12;
      position: absolute;
      p:nth-of-type(1){
        font-size: 12px;
        color: #9C0202;
        .time{
          box-sizing: border-box;
          display: inline-block;
          font-size: 11px;
          width: 44rpx;
          height: 44rpx;
          line-height: 44rpx;
          color: #D71206;
          background-image: url(../../assets/active/timebg.png);
          background-size: 44rpx;
        }  
      }
      p:nth-of-type(2){
        text-align: center;
        padding-left: 36rpx;
        margin-top: 20rpx; 
        color: #9C0202;
        font-size: 11px;
      }
      // .user_img{
      //   border-radius: 50%;
      //   width: 112rpx;
      //   height: 112rpx;
      //   margin: 30rpx 0 25rpx;
      // }
      // p:nth-of-type(2){
      //   color: #333;
      //   font-size: 11px;
      //   .time{
      //     padding: 5rpx 0;
      //     box-sizing: border-box;
      //     margin: 0rpx 10rpx;
      //     display: inline-block;
      //     width: 34rpx;
      //     height: 34rpx;
      //     color: #fff;
      //     background-image: url(../../assets/active/3_1_timebg.png);
      //     // background-size: 20rpx;
      //   }
      // }
      // p:nth-of-type(3){
      //   font-size: 11px;
      //   margin-top: 10rpx;
      //   color: #a9a9a9;
        
      // }
    }
    
    .share_user{
      position: absolute;
      z-index: 8;
      top: 645rpx;
      left: 76rpx;
      width: 452rpx;
      height: 80rpx;
      li:nth-of-type(1){
        margin: 0; 
      }
      li:nth-of-type(5){
        // margin: 0; 
      }
      li{
        float: left;
        margin-left: 12rpx;
        width: 80rpx;
        height: 80rpx;
        img{
          display: block;
          width: 80rpx;
          border-radius: 50%;
        }
        // span{
        //   display: inline-block;
        //   font-size: 11px;
        //   color: #a9a9a9;
        //   width: 66rpx;
        //   overflow: hidden;
        //   white-space: nowrap;
        //   text-overflow: ellipsis;
        // }
      }
    }
    .share_btn {
      width: 469rpx;
      height: 101rpx;
      position: absolute;
      top: 757rpx;
      left: 65rpx;
      z-index: 11;
      button{
        padding: 0;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      .share_button{     
        width: 100%;
        height: 100%;
      }
    }
    .share_tips{
      position: absolute;
      bottom: 50rpx;
      left: 75rpx;
      width: 450rpx;
      height: 55rpx;
      text-align: left;
      p{
        line-height: 1.5;
        font-size: 11px;
        color:#FCD514;
      }
    }
    .quxiao{
      position: absolute;
      bottom: -8%;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .complete{
    z-index: 10;
    width: 626rpx;
    height: 1007rpx;
    position: fixed;
    left: 53rpx;
    top: 4rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    .share_swiper{
      position: absolute;
      font-size: 10px;
      color: #F22216;
      top: 80rpx;
      left: 78rpx;
      width: 350rpx;
      height: 42rpx;
      z-index: 12;
      text-align: left;
      float: left;    
      swiper-item{
        height: 42rpx;
      }
      img{
        border-radius: 50%;
        display: inline-block;
        vertical-align: top;
        width: 30rpx;
        height: 30rpx;
        margin-right: 8rpx;
      }
    }
    .to_share_right{
      position: absolute;
      top: 62rpx;
      right: 30rpx;
      width: 106rpx;
      height: 70rpx;
      z-index: 12;
      .share_button{
        z-index: 12;
        position: absolute;
        top: 0;
        right: 0; 
        height: 60rpx;
        width: 100rpx; 
        opacity: 0;    
        padding: 0;    
      }
      .share_right{
        width: 100%;
        position: absolute;
        top: 0;
        right: -1rpx;
      }
    }
    .share_main{
      text-align: center;
      width: 400rpx;
      height: 50rpx;
      left: 118rpx;
      top: 522rpx;
      z-index: 12;
      position: absolute;
      p:nth-of-type(1){
        font-size: 12px;
        color: #9C0202;
        .time{
          box-sizing: border-box;
          display: inline-block;
          font-size: 11px;
          width: 44rpx;
          height: 44rpx;
          line-height: 44rpx;
          color: #D71206;
          background-image: url(../../assets/active/timebg.png);
          background-size: 44rpx;
        }  
      }
      p:nth-of-type(2){
        margin-top: 20rpx;
        color: #9C0202;
        font-size: 11px;
      }
      // .user_img{
      //   border-radius: 50%;
      //   width: 112rpx;
      //   height: 112rpx;
      //   margin: 30rpx 0 25rpx;
      // }
      // p:nth-of-type(2){
      //   color: #333;
      //   font-size: 11px;
      //   .time{
      //     padding: 5rpx 0;
      //     box-sizing: border-box;
      //     margin: 0rpx 10rpx;
      //     display: inline-block;
      //     width: 34rpx;
      //     height: 34rpx;
      //     color: #fff;
      //     background-image: url(../../assets/active/3_1_timebg.png);
      //     // background-size: 20rpx;
      //   }
      // }
      // p:nth-of-type(3){
      //   font-size: 11px;
      //   margin-top: 10rpx;
      //   color: #a9a9a9;
        
      // }
    }
    
    .share_user{
      position: absolute;
      top: 600rpx;
      left: 96rpx;
      width: 453rpx;
      height: 80rpx;
      li:nth-of-type(1){
        margin: 0; 
      }
      li:nth-of-type(5){
        // margin: 0; 
      }
      li{
        float: left;
        margin-left: 12rpx;
        width: 80rpx;
        height: 80rpx;
        img{
          display: block;
          width: 80rpx;
          border-radius: 50%;
        }
        // span{
        //   display: inline-block;
        //   font-size: 11px;
        //   color: #a9a9a9;
        //   width: 66rpx;
        //   overflow: hidden;
        //   white-space: nowrap;
        //   text-overflow: ellipsis;
        // }
      }
    }
    .complete_more{
      position: absolute;
      top: 634rpx;
      left: 96rpx;
      width: 453rpx;
      height: 146rpx;
      p:nth-of-type(1){
        display: block;
        position: absolute;
        top: 79rpx;
        left: 0rpx;
        width: 100%;
        font-weight: 500;
        height: 20rpx;
        color: #9C0202;
        font-size: 13px;
        // font-weight: 700;
      }
      p:nth-of-type(2){
        font-weight: 700;
        position: absolute;
        width: 100%;
        text-align: center;
        top: 118rpx;
        // left: 147rpx;
        font-size: 14px;
        color:#FDCD00;
      }
    }
    .complete_btn{
      position: absolute;
      width: 472rpx;
      height: 101rpx;
      top: 824rpx;
      left: 87rpx;
      button{
        padding: 0;
        width: 220rpx;
        height: 100%;
        position: absolute;
        top: 0;
        right: 0;
        opacity: 0;
      }
      .complete_button{
        width: 220rpx;
        margin-left: 32rpx;
      }
      .totixian_button{
        width: 220rpx;
       
      }
    }
    .complete_title{
      position: absolute;
      width: 100%;
      top: 172rpx;
      // left: 65rpx;
      p:nth-of-type(1){
        color: #F22216;
        font-weight: 600;
        padding-left: 40rpx;
        font-size: 22px;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      p:nth-of-type(2){
        margin-top: 14rpx;
        color: #F22216;
        font-weight: 400;
        font-size: 11px;
        span{
          display: inline-block;
          margin-bottom: -4rpx;
          margin-left: -4rpx;
          // letter-spacing:-2rpx
        }
      }
    }
    .complete_main{
      position: relative;
      margin-top: 40rpx;
      p:nth-of-type(1){
        font-weight: 600;
        margin-top: 10rpx;
      }
      p:nth-of-type(2){
        margin-top: 10rpx;
      }
    }
    .complete_zhuli{
      position: relative;
      margin-top: 15rpx;
      height: 160rpx;
      width: 100%;
      text-align: center;
      li:nth-of-type(1){
        margin-left:30rpx; 
      }
      li:nth-of-type(5){
        margin-right:30rpx; 
      }
      li{
        float: left;
        margin-left: 10rpx;
        width: 80rpx;
        height: 80rpx;
        img{
          display: block;
          width: 100%;
          height: 100%;
          border-radius: 50%;
        }
        span{
          display: inline-block;
          font-size: 11px;
          color: #a9a9a9;
          width: 66rpx;
          overflow: hidden;
          white-space: nowrap;
          text-overflow: ellipsis;
        }
      }
      .howpeople{
        position: absolute;
        width: 100%;
        bottom: 0;
        // text-align: center;
        p{
          width: 100%;
          text-align: center;
          font-size: 11px;
          color: #F3392A;
        }
      }
    }
    
    .complete_tips{
      position: absolute;
      text-align: center;
      width: 100%;
      top: 928rpx;
      font-weight: 600;
      color: #9C0202;
      font-size: 15px;
      // .complete_left{
      //   position: absolute;
      //   left: 0;
      //   bottom: -60rpx;
      //   height: 80rpx;
      //   width: 120rpx;
      //   z-index: 9;
      //   opacity: 0;
      // }
      .complete_right{
        position: absolute;
        left: 440rpx;
        bottom: -77rpx;
        height: 80rpx;
        width: 160rpx;
        z-index: 9;
        opacity: 0;
      }
      span:nth-of-type(1){
        position: absolute;
        display: inline-block;
        left: 103rpx;
        bottom: -67rpx;
        height: 40rpx;
        width: 120rpx;
        z-index: 9;
      }
      span:nth-of-type(2){
        position: absolute;
        display: inline-block;
        left: 440rpx;
        bottom: -67rpx;
        height: 40rpx;
        width: 160rpx;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .helphe{
    z-index: 10;
    width: 614rpx;
    height: 1076rpx;
    position: fixed;
    left: 81rpx;
    top: 17rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    .helphe_title{  
      position: absolute;
      z-index: 12;
      width: 428rpx;
      height: 56rpx;   
      top: 113rpx;
      left: 83rpx; 
      img{
        width: 100%;
      }
      // position: absolute;
      // width: 428rpx;
      // height: 56rpx;
      // top: 113rpx;
      // left: 83rpx;
      // z-index: 12;
      // font-size: 28px;
      // font-weight: 700;
      // color: #F3392A;
    }
    .helphe_user{
      position: absolute;
      text-align: center;
      width: 100%;
      height: 168rpx;
      top: 209rpx;
      // left: 176rpx;
      z-index: 12;
      .helphe_userimg{
        width: 118rpx;
        height: 118rpx;
        border-radius: 50%;
        margin-bottom: 10rpx;
      }
      .helphe_username{
        position: absolute;
        top: 124rpx;
        left: 196rpx;
        width: 212rpx;
        height: 45rpx;
        line-height: 45rpx;
        z-index: 14;
        color:#FFFFFF;
        font-size: 11px;
        background-image: url(../../assets/active/help_username.png);
        background-size: 212rpx 45rpx;
        // align-items: center;
        // margin-bottom: 20rpx;
      }
      p:nth-of-type(2){
        position: absolute;
        width: 100%;
        top: 172rpx;
        // left: 176rpx;
        font-weight: 600;
        color: #F22216;
        font-size: 15px;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      p:nth-of-type(3){
        position: absolute;
        width: 100%;
        top: 206rpx;
        // left: 176rpx;
        font-weight: 600;
        color: #F22216;
        font-size: 15px;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
    }
    .helphe_btn {
      width: 468rpx;
      height: 216rpx;
      position: absolute;
      top: 678rpx;
      left: 61rpx;
      z-index: 11;
      .helphe_button1 {
        width: 100%;
      }
      .helphe_button2 {
        margin-top: 16rpx;
        width: 100%;
      }
      .helphe_btn1{
        width: 100%;
        height: 100rpx;
        padding: 0;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      .helphe_btn2{
        width: 100%;
        height: 100rpx;
        padding: 0;
        position: absolute;
        bottom: 0;
        left: 0;
        opacity: 0;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .success{
    z-index: 10;
    width: 614rpx;
    height: 1076rpx;
    position: fixed;
    left: 81rpx;
    top: 17rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 614rpx;
      // height: 1334rpx;
      top: 0rpx;
      left: 0rpx;
      // z-index: 998;
    }
    .success_title{
      position: absolute;
      top: 246rpx;
      left: 103rpx;
      width: 400rpx;
      height: 76rpx;
      font-weight: 700;
      p{
        font-size: 36px;
        font-weight: 700;
        color: #F22216;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      
    }
    .success_tips{
      position: absolute;
      width: 100%;
      height: 120rpx;
      // left: 60rpx;
      text-align: center;
      top: 350rpx;    
      img{
        position: absolute;
        width: 443rpx;
        // height: 1334rpx;
        top: -0rpx;
        left: 84rpx;
      }
      p{
        margin-top: 20rpx;
        position: absolute;
        font-weight: 600;
        width: 100%;
        font-size: 15px;
        color:#F22216;
      }
      // background-size: 1976rpx;
    }
    .success_btn {
      width: 468rpx;
      height: 100rpx;
      position: absolute;
      top: 777rpx;
      left: 60rpx;
      z-index: 11;
      button{
        width: 100%;
        height: 100%;
        padding: 0;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      img{
        width: 468rpx;
        height: 100rpx;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .tixian{
    z-index: 10;
    width: 616rpx;
    height: 998rpx;
    position: fixed;
    left: 53rpx;
    top: 13rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    .share_swiper{
      position: absolute;
      font-size: 10px;
      color: #F22216;
      top: 80rpx;
      left: 78rpx;
      width: 350rpx;
      height: 42rpx;
      z-index: 12;
      text-align: left;
      float: left;    
      swiper-item{
        height: 42rpx;
      }
      img{
        border-radius: 50%;
        display: inline-block;
        vertical-align: top;
        width: 30rpx;
        height: 30rpx;
        margin-right: 8rpx;
      }
    }
    .to_share_right{
      position: absolute;
      top: 62rpx;
      right: 23rpx;
      width: 106rpx;
      height: 70rpx;
      z-index: 12;
      .share_button{
        z-index: 12;
        position: absolute;
        top: 0;
        right: 0; 
        height: 60rpx;
        width: 100rpx; 
        opacity: 0;    
        padding: 0;    
      }
      .share_right{
        width: 100%;
        position: absolute;
        top: 0;
        right: -1rpx;
      }
    }
    .tixian_title{
      position: absolute;
      top: 163rpx;
      left: 189rpx;
      z-index: 9;
      p:nth-of-type(1){
        font-size: 29px;
        color:#F22216;
        font-weight: 600;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      p:nth-of-type(2){
        margin-top: 20rpx;
        font-size: 35px;
        font-weight: 600;
        color: #F22216;
        margin-bottom: 30rpx;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
    }
    .tixian_input{
      position: absolute;
      top: 553rpx;
      left: 107rpx;
      z-index: 9;
      width: 426rpx;
      .tixian_input_code{
        position: relative;
        .getcode{
          position: absolute;
          z-index: 9;
          height: 100rpx;
          right: 22rpx;
          bottom: -50rpx;
          color: #666;
          font-size: 13px;
        }
      }
      input{
        text-align: left;
        width: 100%;
        height: 77rpx;
        line-height: 80rpx;
        padding-left: 20rpx;
        box-sizing: border-box;
        font-size: 14px;
        background: #fff;
        color: #999;
        // padding-left: 10rpx;
        border-radius: 5px;
        // border: 2px solid #ccc;
        margin-top: 20rpx;
        // margin-left: 10%;
      }
    }
    .tixian_tips{
      width: 440rpx;    
      text-align: center;
      position: absolute;
      z-index: 9;
      box-sizing: border-box;
      // height: 200rpx;
      top: 886rpx;
      left: 101rpx;
      // padding: 0 40rpx;
      p:nth-of-type(1){
        font-size: 10px;
        line-height: 1.8;
        color: #E9C011;
      }
      p:nth-of-type(2){
        font-size: 12px;
        line-height: 1.8;
        font-weight: 700;
        color: #E9C011;
      }
    }
    .tixian_btn {
      width: 297rpx;
      height: 89rpx;
      position: absolute;
      top: 774rpx;
      left: 174rpx;
      z-index: 11;
      button{
        padding: 0;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      .tixian_button{
        width: 100%;
        height: 100%;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .phone{
    z-index: 10;
    width: 616rpx;
    height: 998rpx;
    position: fixed;
    left: 53rpx;
    top: 13rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
     .share_swiper{
      position: absolute;
      font-size: 10px;
      color: #F22216;
      top: 80rpx;
      left: 78rpx;
      width: 350rpx;
      height: 42rpx;
      z-index: 12;
      text-align: left;
      float: left;    
      swiper-item{
        height: 42rpx;
      }
      img{
        border-radius: 50%;
        display: inline-block;
        vertical-align: top;
        width: 30rpx;
        height: 30rpx;
        margin-right: 8rpx;
      }
    }
    .to_share_right{
      position: absolute;
      top: 62rpx;
      right: 23rpx;
      width: 106rpx;
      height: 70rpx;
      z-index: 12;
      .share_button{
        z-index: 12;
        position: absolute;
        top: 0;
        right: 0; 
        height: 60rpx;
        width: 100rpx; 
        opacity: 0;    
        padding: 0;    
      }
      .share_right{
        width: 100%;
        position: absolute;
        top: 0;
        right: -1rpx;
      }
    }
    .tixian_title{
      position: absolute;
      top: 163rpx;
      left: 189rpx;
      z-index: 9;
      p:nth-of-type(1){
        font-size: 29px;
        color:#F22216;
        font-weight: 600;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
      p:nth-of-type(2){
        margin-top: 20rpx;
        font-size: 35px;
        font-weight: 600;
        color: #F22216;
        margin-bottom: 30rpx;
        text-shadow:0px 3px 5px rgba(187,122,122,0.8);
      }
    }
    .phone_num{
      position: absolute;
      width: 190rpx;
      left: 233rpx;
      top: 525rpx;
      img{
        width: 139rpx;
        height: 106rpx;
      }
      p:nth-of-type(1){
        margin-top: 16rpx;
        font-size: 15px;
        color: #FFCE00;
      }
      p:nth-of-type(2){ 
        font-size: 15px;
        margin-top: 4rpx;
        color: #FFCE00;
      }
    }
    .phone_title{
      position: relative;
      padding-top: 80rpx;
      z-index: 9;
      p:nth-of-type(1){
        font-size: 12px;
        font-weight: 600;
      }
      p:nth-of-type(2){
        margin-top: 20rpx;
        font-size: 26px;
        font-weight: 600;
        color: #F3392A;
      }
    }
   
    .tixian_tips{
      width: 440rpx;    
      text-align: center;
      position: absolute;
      z-index: 9;
      box-sizing: border-box;
      // height: 200rpx;
      top: 886rpx;
      left: 101rpx;
      // padding: 0 40rpx;
      p:nth-of-type(1){
        font-size: 10px;
        line-height: 1.8;
        color: #E9C011;
      }
      p:nth-of-type(2){
        font-size: 12px;
        line-height: 1.8;
        color: #E9C011;
        font-weight: 700;
      }
    }
    .phone_btn {
      width: 297rpx;
      height: 89rpx;
      position: absolute;
      top: 750rpx;
      left: 174rpx;
      z-index: 11;
      button{
        padding: 0;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
      }
      .phone_button{
        width: 100%;
        height: 100%;
      }
    }
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .jiakefu{
    z-index: 10;
    width: 610rpx;
    height: 1009rpx;
    position: fixed;
    left: 69rpx;
    top: 4rpx;
    overflow: hidden;
    display: block;
    clear: both;
    text-align: center;
    .jiakefu_title{
      position: absolute;
      width: 314rpx;
      height: 29rpx;
      font-size: 14px;
      color: #F22216;
      top: 100rpx;
      left: 144rpx;
      font-weight: 600;
      font-family: PingFangSC-Semibold;
    }
    .jiakefu_erweima{
      position: absolute;
      top: 145rpx;
      left: 144rpx;
      width: 336rpx;
      height: 318rpx;
      img{
        display: block;
        width: 100%;
      }
    }
    .jiakefu_methods{
      position: absolute;
      top: 692rpx;
      left: 226rpx;
      width: 152rpx;
      height: 35rpx;
      p {
        font-size: 18px;
        color:#FFFFFF;
        font-weight: 600;
      }
    }
    .jiakefu_tips{
      position: absolute;
      top: 763rpx;
      left: 110rpx;
      width: 405rpx;
      height: 67rpx;
      text-align: left;
      li{
        margin-bottom: 20rpx;
        img{
          float: left;
          width: 19rpx;
          display: inline-block;
          height: 19rpx;
          vertical-align: middle;
          margin-top: 5rpx;
          margin-right: 4rpx;
        }
      }
      p:nth-of-type(1){
        font-size: 12px;
        width: 400rpx;
        margin-left: 26rpx;
        color: #fefefe;
        line-height: 1.5;
      }
      p:nth-of-type(2){
        font-size: 12px;
        color: #fefefe;
        line-height: 1.5;
      }
    }
    .main_img{
      position: absolute;
      width: 100%;
      top: 0;
      left: 0;
    }
    
    .quxiao{
      position: absolute;
      bottom: 0;
      left: 40%;
      width: 20%;
      height: 16%;
    }
  }
  .splitLine{
    width: 100%;
    height: 16rpx;
    background-color: #F6F6F6;
    margin: 40rpx 0;
  }
  .splitLine2{
    width: 100%;
    height: 16rpx;
    background-color: #F6F6F6;
    margin-bottom: 40rpx;
  }
  .funList{
    display: flex;
    flex-wrap: nowrap;
    padding: 0 60rpx;
    text-align: center;
    color: #999;
    margin: 40rpx 0;
    div{
      width: 100%;
    } 
    img{
      width: 100rpx;
      height: 100rpx;
      margin-bottom: 16rpx;
    }    
    .funListMiddle{
      position: relative;
      .hotGif {
        width: 74rpx;
        height: 48rpx;
        margin: 0;
        position: absolute;
        top: -10rpx;
        right: 4rpx;
      }
    } 
  }
  .hotBanks{
    width: 100%;
    .hotBanks_header{
      display: flex;
      justify-content: space-between;
      height: 134rpx;
      line-height: 134rpx;
      padding: 0 30rpx;
      .theme_p{
        /*font-weight bold*/
      } 
      .leftBorder{
        display: inline-block;
        position: relative;
        top: 4rpx;
        height: 30rpx;
        border-left: 6rpx solid #7370FF;
        margin-right: 20rpx;
      }
    }    
    .hotBanks_content{
      /*margin-top 20rpx*/
      width: 100%;
      text-align: center;
      /*padding-bottom 20rpx*/
      ul{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        /*height 580rpx*/
        overflow: hidden;
        clear: both;
        li{
          width: 33.333%;
          text-align: center;
          margin-bottom: 30rpx;
          position: relative;
          .tips{
            position: absolute;
            top: -12rpx;
            left: 120rpx;
            font-size: 40rpx;
            /*background-color #F43C2A*/
            background: linear-gradient(to right, #FE743C , #F3392A); /* 标准的语法 */
            border-radius: 44rpx;
            padding: 4rpx 6%;
            border: 2rpx solid #fff;
            color: #fff;
            box-shadow: 0 0 40rpx rgba(243, 57, 42, 0.1);
            -webkit-transform: scale(0.5);
          }  
          img{
            width: 90rpx;
            height: 90rpx;
            border-radius: 100rpx;
          }
           
          p:nth-of-type(1){
            /*font-weight*/
            color: #333;
            /*font-family pingFangSC-Medium
            font-weight normal*/
            font-size: 28rpx;
            margin: 20rpx 0 10rpx;
          }
           
          p:nth-of-type(2){
            /*font-family pingFangSC-Regular*/
            font-size: 12px;
            margin: 10rpx 0; 
          }   
        }     
      }
        
      .moreItem{
        width: 100%;
        margin-top: 10rpx;
        font-size: 14px;
        color: #6c6c6c;
        /*font-family pingFangSC-Medium*/   
      }   
    }    
  }
  .theme{
    /*width 100%*/
    .theme_p{
      /*font-weight bold*/
      /*position relative*/
      padding: 50rpx 30rpx;
      margin-top: -40rpx;
      .leftBorder{
        display: inline-block;
        position: relative;
        top: 4rpx;
        height: 30rpx;
        border-left: 6rpx solid #7370FF;
        margin-right: 20rpx;
      }   
    } 
    .theme_content{
      margin: 0 4%;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 0 30rpx rgba(209,209,209,0.22);
      border-radius: 10rpx;

      /*text-align center*/
      .theme_div{
        // display: inline-block;
        width: 44%;
        padding: 0 16rpx;
        margin: 32rpx 0;
        text-align: left;
        p{
          margin: 10rpx 0;
        }
        p:nth-of-type(1){
          /*font-weight bold*/
          font-size: 26rpx;
          color: #363636;
          /*font-family pingFangSC-Medium
          font-weight normal*/
          /*margin-top 20rpx*/
        }
         
        p:nth-of-type(2){
          font-size: 22rpx;
          /*font-family pingFangSC-Regular*/
        }
        img{
          width: 90rpx;
          height: 90rpx;
          float: right;
          margin-right: 10rpx;
        }    
      }
        
    }
      /*padding 0 30rpx*/
  }
  .banner{
    width: 100%;
    /*height 250rpx*/
    margin-top: 30rpx;
    div:nth-of-type(3){
      display: flex;
      justify-content: flex-start;
      /*margin-top 15px*/
    }
    .banneritem{
      position: relative;
      
    }
   

    .todayTitle{
      text-align: center;
      margin-left: 20rpx;
      width: 20%;
      display: inline-block;
      /*padding 0 5px*/
      color: #fff;
      font-size: 24rpx;
      font-style: italic;
      font-weight: bold;
      background: linear-gradient(to right, #FF6D3B , #FFB152); /* 标准的语法 */
      height: 36rpx;
      line-height: 36rpx;
      border-radius: 36rpx;
    }
    img{
      width: 100%;
      height: 100%;
    }  
  }
  .hotCard {
    padding-bottom: 50rpx;
    .hotCard_p{
      padding: 50rpx 30rpx;
      margin-top: -40rpx;
      .leftBorder{
        display: inline-block;
        position: relative;
        top: 4rpx;
        height: 30rpx;
        border-left: 6rpx solid #7370FF;
        margin-right: 20rpx;
      }  
    }   
    .hotCard_content{
       ul{
          text-align: center;          
          li{
            display: inline-block;
            border-radius: 10rpx;
            box-shadow: 0px 6rpx 20rpx #eee;
            margin-top: 20rpx;
            margin-bottom: 10rpx;
            padding: 20rpx;
            position: relative;
            width: 85%;
            .imgBox{
              position: absolute;
              right: 0;
              top: 0;
              
              img{
                width: 94rpx;
                height: 94rpx;
              }
            }
            a{
              display: flex;
              justify-content: flex-start;
              align-items: center;
            }             
            img{
              /*position absolute*/
              /*left 10px*/
              // vertical-align: -30%;
              width: 37%;
              // height: 144rpx;
              border-radius: 10rpx;
              margin-right: 30rpx;
            }
            .bankContent{
              line-height: 56rpx;
              width: 100%;
              display: inline-block;
              text-align: left;
              position: relative;
              /*margin-left 10px*/
              .cardNum {
                position: absolute;
                right: 0;
                bottom: -4%;
                font-size: 11px;
                color: #666;
              }
              p:nth-of-type(1){
                 /*font-family  pingFangSC-Medium
                font-weight normal*/
                color: #363636;
                font-size: 15px;
                max-width: 350rpx;
                overflow: hidden;
                white-space: nowrap;
                text-overflow: ellipsis;
                /*font-weight bold*/
              }
               
              p:nth-of-type(2){
                /*font-family pingFangSC-Medium*/
                font-size: 13px;
                color: #9a9a9a;
                margin-top: -8rpx;
                max-width: 350rpx;
                overflow: hidden;
                white-space: nowrap;
                text-overflow: ellipsis;
              }   
            }     
          }    
       }   
    }    
  }    
}
#kamiTitlePic{
    width: 137rpx;
    height: 64rpx;
    margin-top: -10rpx;
    margin-left: 20rpx;
}
#theme-swiper1{
  width: 750rpx;
}
#box{
  height: 40rpx;
  line-height: 40rpx;
  overflow: hidden;
  transition: all 2s;
}
.anim{
  transition: all 1s;
}
#box li{
    /*line-height: 20px;*/
    /*padding-left:5px;*/
    font-size:12px;
}
.theme_transverseline{
    width: 45%;
    height: 2rpx;
    background: url(../../assets/hengxian.png) no-repeat;
    transform: scaley(0.6);
}
.theme_verticalline{
    width: 2rpx;
    height: 100rpx;
    background: url(../../assets/shuxian.png) no-repeat;
    margin-top: 10rpx;
    transform: scalex(0.6);
}
.itemTipsCss{
    max-width: 150rpx;
    height: 30rpx;
    line-height: 30rpx;
    padding: 2rpx 2rpx;
    margin-right: 6rpx;
    margin-top: 4rpx;
    font-size: 11px;
    overflow: hidden;
    white-space: nowrap;
    border: 1px solid #bdbdbd;
    border-radius: 6px;
    text-overflow: ellipsis;
    float:left;
    color: #9a9a9a;
    /*-webkit-transform: scale(0.5)*/
    /*transform: scale(0.5);*/
}
.itemTipsCss::after{
    content: "";
    width: 195%;
    height: 30rpx;
    line-height: 30rpx;
    padding: 4rpx;
    // margin-top: -40rpx;
    // margin-left: -57%;
    font-size: 11px;
    border: 2rpx solid #bdbdbd;
    border-radius: 8px;
    float: left;
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
}
.loading{
    margin-bottom: 200rpx;
    display: flex;
    justify-content: center;
    img{
      width: 50rpx;
      height: 50rpx;
    }
}
.noMore{
  text-align: center;
  p{
    font-size: 13px;
    line-height: 2;
    color:#666;
  }
} 
.navTitle{
  width:100%;    
  height: 86rpx;
  line-height: 86rpx;
  text-align: center;
  font-size: 18px;
  color: #363636;
  border-bottom: 2rpx solid #C9C9C9;
  background:#fff;
}
.navTitle img{
  width: 24rpx;
  position: absolute;
  top: 20rpx;
  left: 5%;
}
.cardraiders{
  background: #F6F6F6;
  // padding-bottom: 100rpx;
  .funList{
    background: #fff;
    display: flex;
    flex-wrap: nowrap;
    padding: 40rpx 60rpx 40rpx 0 ;
    text-align: center;
    color: #999;
    margin:  0 0 0rpx 0;
    div{
      width: 100%;
      
    } 
    img{
      width: 100rpx;
      height: 100rpx;
      margin-bottom: 16rpx;
    }    
    .funListMiddle{
      position: relative;
      .hotGif {
        width: 74rpx;
        height: 48rpx;
        margin: 0;
        position: absolute;
        top: -10rpx;
        right: 4rpx;
      }
    } 
  }
  .hotBanks_chaxun{
    display: flex;
    justify-content: space-between;
    width: 95%;
    margin-left: 2.5%;
    border-radius: 8px;
    box-shadow: 2px 2px 2px rgba(0,0,0,0.1);
    height: 200rpx;
    // line-height: 160rpx;
    box-sizing: border-box;
    padding: 30rpx 0;
    // margin-left: 20rpx;
    .funListMiddle{
      flex: 1;
      width: 20%;
      justify-content: space-between;
      text-align: center;
      img{
        width: 100rpx;
        height: 100rpx;
      }
      p{
        widows: 100rpx;
        height: 40rpx;
        line-height: 40rpx;
      }
    }
  }
  .hotBanks_header{
      display: flex;
      justify-content: space-between;
      height: 110rpx;
      line-height: 110rpx;
      padding: 0 30rpx;
      .theme_p{
        /*font-weight bold*/
      } 
      .leftBorder{
        display: inline-block;
        position: relative;
        top: 4rpx;
        height: 30rpx;
        border-left: 6rpx solid #7370FF;
        margin-right: 20rpx;
      }
    }  
  .header{
    text-align: center;
    padding: 20rpx;
    img{
        width: 100%;
    }  
  }
    
  .articleList{
    a:visited{
      color: #363636;
    }   
    .content{
      border:-2rpx(rgb(232, 232, 232));
      display: flex;
      justify-content: space-between;
      padding: 50rpx;
      background: #fff;
      .content_left{
        width: 100%;
        p:nth-of-type(1){
          color: #363636;
          font-size: 16px;
          /*font-family pingFangSC-Medium*/
        }
        
        p:nth-of-type(2){
          width: 100%;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
          font-size: 14px;
          color: #9a9a9a;
          margin: 20rpx 0;
          /*font-family pingFangSC-Medium*/
        }
          
        span{
          color: #9a9a9a;
          font-size: 12px;
          /*font-family pingFangSC-Medium*/
        }
          
        span:nth-of-type(2){
          float: right;
            margin-right: 30rpx;
          /*font-family pingFangSC-Medium*/
        }
          
      }   
      .content_right{
        width: 30%;
        img{
          width: 64%;
          margin-left: 40rpx;
        }      
      }    
    }     
  }    
 }    
.mengban{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  background: #760A00 ;
  z-index: 8;
  .toquxiao{
    position: absolute;
    top: 1015rpx;
    left: 326rpx;
    width: 100rpx;
    height: 100rpx;
    opacity: 0;
    z-index: 16;
  }
  img{
    position: absolute;
    top: 1040rpx;
    left: 351rpx;
    width: 48rpx;
    height: 48rpx;
  }
}

</style>
