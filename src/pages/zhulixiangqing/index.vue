<template>
  <div class="wrap">
    <canvas id="canvas" canvas-id='canvas' style="width:750rpx; height:1208rpx;"></canvas> 
    <div class="main">
        <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/more_bg.jpg" class="main_img" alt="">
        <div class="toshare">
            <button class="toshare_btn" open-type='share'></button>
            <img src="https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/more_share.png" mode="widthFix" alt="">
        </div>
        <div class="todownload" @click="xiazai">
            <button class="todownload_btn" @click="xiazai"></button>
            <img src="../../assets/active/more_down.png" mode="widthFix" alt="">
        </div>
        <div class="more">
            <div class="zhulixiangqing">
                <img mode="widthFix" :src="img" alt="">
                <p>{{nickName}}</p>
            </div>
            <div class="zhuli_title">
                <p><span>{{tixiannum}}</span></p>
                <p>{{pm}}</p>
            </div>
            <div class="zhuli_main">
                <p>{{zhulinum}}</p>
                <div class="first">
                    <li style="float:left;" v-for="(item,index) in userArrOne" :key="index">
                        <img mode="widthFix" :src="item" alt="">
                    </li>
                </div>
                <div class="second">
                    <li style="float:right;" v-for="(item,index) in userArrTow" :key="index">
                        <img mode="widthFix" :src="item" alt="">
                    </li>
                </div>
                <div class="third">
                    <li style="float:left;" v-for="(item,index) in userArrThree" :key="index">
                        <img mode="widthFix" :src="item" alt="">
                    </li>
                </div>
                <div class="four">
                    <li style="float:right;" v-for="(item,index) in userArrFour" :key="index">
                        <img mode="widthFix" :src="item" alt="">
                    </li>
                </div>
            </div>
            <div class="zhuli_erweima">
                <img :src="QrCodeImgUrl" alt="" mode="widthFix">
                <p>查看我的财气榜</p>
            </div>
        </div>
    </div>
   
  </div>
</template>

<script>
import {getTaskInfo, getMore, getQRcode} from '../../requestAPI/requestAPI';
  export default {
    data () {
      return {
        windowW: '',  // 设备宽度
        windowH: '',  // 设备高度
        zhulinum: '', // 帮助用户助力的人数
        coin: '',  // 用户累计金币数
        tixiannum: '', // 可提现金额数
        pm: '',  // 当前用户排名
        img: require('../../assets/active/morentouxiang.png'),
        userArrOne: [],
        userArrTow: [],
        userArrThree: [],
        userArrFour: [],
        userName: '',
        openid: '',

        userimg: ['https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png'],
        // 画图相关
        avatarUrl: '',
        nickName: '',
        fengniaoID: '',
        QrCodeImgUrl: '', // 用户二维码地址
        color1: '',
        color2: '',
        color3: '',
        color4: '',
        color5: '',
        urlDuck: '',  //鸭子图片
        saveUrlDuck: '',
        typeDuck: '',  //鸭子类型
        introDuck: '',  //鸭子简介
        parseDuck: '',  //鸭子详情
        matchImg: '',
        inviteImg: '',
        prurl: '',
      }
    },
    onLoad(){
      let that = this   
      wx.showLoading({
        title: '正在努力生成中...',
        mask: true,
      });  
      wx.getStorage({
        key:'openID',
        success:function(res){  
            that.openid = res.data.openId
            let openid = res.data.openId
            getTaskInfo({openid: res.data.openId}).then(res=>{
                // console.log('详情页活动信息',res)
                that.tixiannum = res.data.coin/100
                that.img = res.data.headurl
                that.zhulinum = res.data.peoples
                that.nickName = decodeURI(res.data.usname)
                // console.log(decodeURI("%E5%BD%AD%E8%B4%B5%E5%AE%9D"))
            })
            getMore({openid: res.data.openId}).then(res => {      
                console.log('more',res)
                if(res.result.code == 10000){
                    that.userArrOne= []
                    that.userArrTow= []
                    that.userArrThree= []
                    that.userArrFour= []
                    that.userimg = []
                    that.pm = res.data.pm
                    if(res.data.peopleinfo == null || res.data.peopleinfo == '')
                    {
                        that.userimg = ['https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        'https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png',
                        ]
                        
                    } else {
                        if(res.data.peopleinfo.length <22){
                            for(let i = 0; i<res.data.peopleinfo.length; i++){
                                let url = res.data.peopleinfo[i].fheadurl
                                let name = res.data.peopleinfo[i].fname
                                if(url==null || url == ''){
                                    url = "https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132"
                                    that.userimg.push(url)
                                } else {
                                    that.userimg.push(url)
                                } 
                                if(name == 'null' || name == '') {
                                    that.nickName = '大神玩卡';
                                }else {
                                    // this.nickName = option.nickName;
                                }
                            }
                            for(let j=res.data.peopleinfo.length; j<22; j++ ){
                                that.userimg.push('https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/app2_0/moren.png')
                            }
                        } else {
                            for(let k = 0; k<22; k++){
                                let url = res.data.peopleinfo[k].fheadurl
                                if(url==null){
                                    url = "https://wx.qlogo.cn/mmopen/vi_32/jLqE4FVxYElZoggLrVZWicKy7LibD4zdiaZZ0QTSuUMySvM35lYYkvleEFiaO1TnKicTGNX0FAkf7DdM9nQADzGAXXQ/132"
                                    that.userimg.push(url)
                                } else {
                                    that.userimg.push(url)
                                }   
                            }
                        }
                    }
    
                    // console.log(that.userimg)
                    that.userArrOne = that.userimg.slice(0,5);
                    that.userArrTow = that.userimg.slice(5,11);
                    that.userArrThree = that.userimg.slice(11,17);
                    that.userArrFour = that.userimg.slice(17,22);
                    console.log("openid",openid)
                    getQRcode({openid:openid,chnl:'dashen'}).then(res => {
                        console.log(res)
                        if(res.result.code == 10000){
                            that.QrCodeImgUrl = res.result.msg
                            // console.log('that.userimg',that.userimg)
                            // 用户二维码
                            let promise1 = new Promise(function (resolve, reject) {
                                // console.log(that.QrCodeImgUrl)
                                wx.getImageInfo({
                                    src: that.QrCodeImgUrl,
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res1', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            // 用户头像
                            let promise2 = new Promise(function (resolve, reject) {
                                // console.log('头像',that.img)
                                wx.getImageInfo({
                                    src: that.img,
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res2', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise3 = new Promise(function (resolve, reject) {
                                // console.log(that.userimg)
                                wx.getImageInfo({
                                    src: that.userimg[0],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res3', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise4 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[1],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res4', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise5 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[2],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res5', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise6 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[3],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res6', res);
                                    },
                                    fail: function (err) {
                                        // console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise7 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[4],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res7', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise8 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[5],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res8', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise9 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[6],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res9', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise10 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[7],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res10', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise11 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[8],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res11', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise12 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[9],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res12', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise13 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[10],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res13', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise14 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[11],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res14', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise15 = new Promise(function (resolve, reject) { 
                                
                                wx.getImageInfo({
                                    src: that.userimg[12],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res15', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                               
                                
                            });
                            let promise16 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[13],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res16', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise17 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[14],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res17', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise18 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[15],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res18', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise19 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[16],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res19', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise20 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[17],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res20', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise21 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[18],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res21', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise22 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[19],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res22', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise23 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[20],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res23', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise24 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: that.userimg[21],
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res24', res);
                                    },
                                    fail: function (err) {
                                        console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                            let promise25 = new Promise(function (resolve, reject) {
                                wx.getImageInfo({
                                    src: "https://ioskamidownload.oss-cn-qingdao.aliyuncs.com/miniprogram/more_bg.png",
                                    success: function (res) {
                                        resolve(res);
                                        // console.log('res24', res);
                                    },
                                    fail: function (err) {
                                        // console.log(err);
                                        wx.hideLoading();
                                        wx.showToast({
                                            title: '生成失败，请稍后重试',
                                            icon: 'none',
                                            duration: 1000
                                        });
                                    }
                                })
                            });
                      
                            Promise.all([promise1,
                                promise2,promise3,promise4,promise5,promise6,promise7,promise8,promise9,promise10,promise11,promise12,promise13,promise14,promise15,promise16,promise17,promise18,promise19,promise20,promise21,promise22,promise23,promise24,promise25
                            ]).then(res => {
                                // console.log('res',res)
                                const ctx = wx.createCanvasContext('canvas');
                                // 画用户头像
                               
                               // 背景图
                               ctx.drawImage(res[24].path, 0, 0, 375, 604);
                
                                ctx.setFillStyle('#C18A37');
                                ctx.font = '14px 思源黑体';
                                ctx.fillText(that.nickName, 157, 98);
                               
                                
                                ctx.setFillStyle('#C1160F');
                                ctx.font = '45px 思源黑体';
                                ctx.fillText(that.tixiannum, 141, 165);
 
                                ctx.setFillStyle('#CD3F06');
                                ctx.font = '18px 思源黑体';
                                ctx.fillText(that.pm, 212, 194);
  
                                ctx.setFillStyle('#C18A37');
                                ctx.font = '13px 思源黑体';
                                ctx.fillText(that.zhulinum, 172, 268);

                                // // 画二维码
                                ctx.drawImage(res[0].path, 131, 475,100, 100);
                                ctx.restore()
                                ctx.setStrokeStyle('#fff');

                                // 画用户头像
                                ctx.save()
                                ctx.arc(188, 53, 28, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[1].path, 160, 25, 55, 55);
                                ctx.restore()
                                
                                // 第一行
                                ctx.save()
                                ctx.moveTo(130, 277)
                                ctx.arc(142, 289, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[2].path, 130, 277, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(158, 277)
                                ctx.arc(170, 289, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[3].path, 158, 277, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(186, 277)
                                ctx.arc(198,289, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[4].path, 186, 277, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(211, 277)
                                ctx.arc(223,289, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[5].path, 211, 277, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(236, 291)
                                ctx.arc(248,303, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[6].path, 236, 291, 24, 24);
                                ctx.restore()

                                // 第二行
                                ctx.save()
                                ctx.moveTo(226, 317)
                                ctx.arc(238,329, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[7].path, 226, 317, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(198, 317)
                                ctx.arc(210,329, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[8].path, 198, 317, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(170, 317)
                                ctx.arc(182,329, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[9].path, 170, 317, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(142, 317)
                                ctx.arc(154,329, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[10].path, 142, 317, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(114, 317)
                                ctx.arc(126,329, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[11].path, 114, 317, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(98, 340)
                                ctx.arc(110,352, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[12].path, 98, 340, 24, 24);
                                ctx.restore()

                                // 第三行
                                ctx.save()
                                ctx.moveTo(111, 368)
                                ctx.arc(123,380, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[13].path, 111, 368, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo( 139, 368)
                                ctx.arc(151,380, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[14].path, 139, 368, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(166, 368)
                                ctx.arc(179,380, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[15].path, 166, 368, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(194, 368)
                                ctx.arc(207,380, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[16].path, 194, 368, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(222, 368)
                                ctx.arc(235,380, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[17].path, 222, 368, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(238, 390)
                                ctx.arc(250,402, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[18].path, 238, 390, 24, 24);
                                ctx.restore()
                                
                                // 第四行
                                ctx.save()
                                ctx.moveTo(223, 413)
                                ctx.arc(235,425, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[19].path, 223, 413, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(195, 413)
                                ctx.arc(207,425, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[20].path, 195, 413, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(167, 413)
                                ctx.arc(179,425, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[21].path, 167, 413, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(139, 413)
                                ctx.arc(151,425, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[22].path, 139, 413, 24, 24);
                                ctx.restore()

                                ctx.save()
                                ctx.moveTo(194, 368)
                                ctx.arc(123,425, 12, 0, Math.PI * 2, false);
                                ctx.clip();
                                ctx.drawImage(res[23].path, 111, 413, 24, 24);
                                ctx.restore()
                                // console.log('生成即将结束')
                                ctx.draw()
                                // console.log('生成结束');
                                wx.hideLoading();
                            })

                        }
                    })
                    
                }
            })  
        }
      }) 
    },
    onShow(){
        
     
    },
    onShareAppMessage: function (res) {
      return {
        title: `我正在抢红包，已经获得￥${this.tixiannum}，全国排名${this.pm}，快来支援我~`,
        // imageUrl: 'http://download.pcuion.com/app2_0/songxianj.png',
        path: `/pages/index/main?userId=${this.openid}`
      }
    },
    methods: {
      xiazai() {
        let that = this;
        wx.showLoading({
          title: '努力生成中...'
        });
        wx.canvasToTempFilePath({
          x: 0,
          y: 0,
          width: 750,
          height: 1208,
          destWidth: 750,
          destHeight: 1208,
          canvasId: 'canvas',
          success: function (res) {
            that.prurl = res.tempFilePath;
            wx.hideLoading();

            //生产环境时 记得这里要加入获取相册授权的代码
            wx.saveImageToPhotosAlbum({
              filePath: that.prurl,
              success(res) {
                wx.showToast({
                  title: '图片已保存到相册',
                  icon: 'none',
                  duration: 1500
                });
              }
            })

          },
          fail: function (res) {
            // console.log(res)
          }
        });

      }
    }
  }
</script>

<style lang='scss' scoped>
.wrap{
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  width: 100%;
  text-align: center;
  // height: 100%;
  // height: 1800rpx;
  background: #c03830;
  text-align: center;
  .main{
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
  }
  .main_img{
      position: fixed;
      top: 0;
    //   left: -30rpx;
      bottom: 0;
      right: 0;  
      width: 750rpx;
      height: 1208rpx;           
  }
  .toshare_btn{
    position: absolute;
    top: -22rpx;
    // left: 103rpx;
    right:-16rpx;
    // bottom:0;
    width: 150rpx;
    height: 110rpx;
    opacity: 0;
    z-index: 20;
  }
  .todownload_btn{
    position: absolute;
    top: -22rpx;
    left: -16rpx;
    width: 150rpx;
    height: 110rpx;
    opacity: 0;
    z-index: 20;
  }
  .toshare{
      position: absolute;
      top: 111rpx;
      right: 103rpx;
      width: 110rpx;
      height: 64rpx;

      img{
          width: 100%;
      }
  }
  .todownload{
        position: absolute;
      top: 111rpx;
      left: 104rpx;
      width: 110rpx;
      height: 64rpx;
      img{
          width: 100%;
      }
  }
  .more{
      position: absolute;
      top: 27rpx;
      left: 0;
      width: 750rpx;
      height: 1061rpx;
      .zhulixiangqing{
        position: absolute;
        top: 24rpx;
        left: 285rpx;
        width: 220rpx;
        // margin-top: 60rpx;
        margin-bottom: 20rpx;
        img{
        width: 110rpx;
        border-radius: 50%;
        //   border: 2px solid #fff;
        margin-bottom: 10rpx;
        }
        p{
        color: #C18A37;
        font-size: 14px;
        }
    }
    .zhuli_title{
        position: absolute;
        top: 211rpx;
        left: 158rpx;
        width: 443rpx;
        height: 160rpx;
        text-align: center;
        // margin-bottom: 40rpx;
        p:nth-of-type(1){
            font-weight: 500;
            font-size: 19px;
            color: #C18A37;
            // margin-bottom: 10rpx;
            span {
                font-size: 45px;
                color: #C1160F;
            }
        }  
        p:nth-of-type(2){
            position: absolute;
            z-index: 10;
            top: 119rpx;
            left: 267rpx;
            font-weight: 500;
            font-size: 19px;
            color: #C18A37;
            // margin-bottom: 10rpx;
            span {
                font-size: 45px;
                color: #C1160F;
            }
        }
        img{
            position: absolute;
            top: 108rpx;
            left: 0rpx;
            width: 443rpx;
            height: 79rpx;
        }
    }
    .zhuli_main {
        position: relative;
        top: 500rpx;
        width: 535rpx;
        height: 550rpx;
        // height: 50%;
        margin-left: 107rpx;
        .main_bg{
            position: absolute;
            left: 33rpx;
            top: -22rpx;
            width: 369rpx;
            height: 390rpx;
        }
        p{  
            text-align: center;
            position: absolute;
            width: 100rpx;
            left: 209rpx;
            top: -15rpx;
            font-size: 14px;
            color:goldenrod;
        }
        div{
            clear: both;
            display: block;
            overflow: hidden;
            width: 400rpx;
            height: 100rpx;
            li:nth-of-type(1){
            // margin: 0;
            }
            li {
                margin-left: 8rpx;
                // margin-top: 8rpx;
            }
            img{
            width: 49rpx;
            height: 49rpx;
            // height: 84rpx;
            border-radius: 50%;
            // border: 2px solid #fff;
            }
        }
        
        // 奇数行
        div:nth-child(odd){ 
            display: block;
            overflow: hidden;
            clear: both;
            box-sizing: border-box;
            padding-left: 80rpx;
            margin-top: -28rpx;
            // li:last-of-type{
            //     // background: #000;
            //     margin-top: 43rpx;
            //     margin-left: -13rpx;
            // }
        }
        // 偶数行
        div:nth-child(even){ 
            display: block;
            overflow: hidden;
            clear: both;
            margin-top: -28rpx;
            box-sizing: border-box;
            padding-right: 80rpx;
            // li:last-of-type{
            //     // background: #000;
            //     margin-top: 43rpx;
            //     margin-right: -13rpx;
            // }
        }
        .first{
            position: absolute;
            width: 400rpx;
            left: 153rpx;
            top: 58rpx;
            li:last-of-type{
                // background: #000;
                margin-top: 35rpx;
                margin-left: -2rpx;
            }
        }
        .second{
            position: absolute;
            width: 400rpx;
            left: -4rpx;
            top: 145rpx;
            li:last-of-type{
                // background: #000;
                margin-top: 47rpx;
                margin-right: -23rpx;
            }
        }
        .third {
            position: absolute;
            width: 400rpx;
            left: 112rpx;
            top: 245rpx;
            li:last-of-type{
                // background: #000;
                margin-top: 39rpx;
                margin-left: -13rpx;
            }
        }
        .four {
            position: absolute;
            width: 400rpx;
            left: -1rpx;
            top: 329rpx;
            li:last-of-type{
                // background: #000;
                margin-top: 0rpx;
                margin-left: 0rpx;
            }
        }
    }
    .zhuli_erweima {
        position: absolute;
        bottom: -84rpx;
        left: 295rpx;
        width: 154rpx;
        height: 154rpx;
        border: 1px solid gold;
        img{
            width: 100%;
        }
        p{
            position: absolute;
            width:160rpx;
            height:24rpx;
            font-size:11px;
            font-family:PingFangSC-Semibold;
            font-weight:600;
            color:rgba(227,194,101,1);
            // line-height:56px;
        }
    }

  }
  
}
#canvas{
    position: absolute;
    left: -750rpx;
    top: 0;
    // background: #c03830;
}

</style>
