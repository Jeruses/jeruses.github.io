<!DOCTYPE html><html lang="zh"><head><meta charset="utf-8"><meta http-equiv="X-UA-Compatible" content="IE=edge"><meta name="viewport" content="width=device-width,initial-scale=1"><meta name="renderer" content="webkit"><link rel="icon" href=""><title></title><script src="https://res.wx.qq.com/open/js/jweixin-1.2.0.js"></script><script src="https://open.work.weixin.qq.com/wwopen/js/jwxwork-1.0.0.js"></script><script charset="utf-8" src="https://map.qq.com/api/js?v=2.exp&key=YK6BZ-ODI6W-QOORM-R2ANJ-W65ZJ-5YBJB"></script><script src="https://3gimg.qq.com/lightmap/components/geolocation/geolocation.min.js"></script><script src="https://pv.sohu.com/cityjson?ie=utf-8"></script><script src="/md5.js"></script><script src="/paramsHandler.js"></script><script>let Ip = returnCitySN['cip'];
      localStorage.setItem('Ip', Ip);
      // localStorage.setItem('cityname', cityname)  // 之前的数据
      // 新增的获取定位的数据
      let geolocation = new qq.maps.Geolocation(
        'YK6BZ-ODI6W-QOORM-R2ANJ-W65ZJ-5YBJB',
        'myapp'
      );
      geolocation.getLocation(
        (position) => {
          let cityname = position.province + position.city;
          localStorage.setItem('cityname', cityname);
        },
        (errCallback) => {
          let cityname = returnCitySN['cname'];
          localStorage.setItem('cityname', cityname);
        }
      );</script><script>var _hmt = _hmt || [];
      (function() {
        var hm = document.createElement("script");
        hm.src = "https://hm.baidu.com/hm.js?c2375d4c9286a79fbb49dff493fccb72";
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(hm, s);
      })();

      /**
       * KA产品差异化配置
       */
      window['WeShineProductSettings'] = {
        fileStorage: 'cos',
        fastDfsImageUrlPrefix: '',
        customizeVersion: '1015'
      };</script><script src="/module-loader.js?v=1686139388716"></script></head><body><noscript><strong>We're sorry but vue-admin-template doesn't work properly without JavaScript enabled. Please enable it to continue.</strong></noscript><div id="app"></div><script>moduleLoaderInit({
        NODE_ENV: 'production'
      });</script></body></html>
