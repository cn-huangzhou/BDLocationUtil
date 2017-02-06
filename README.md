# BDLocationUtil
百度地图定位工具类

使用方法
LocationUtil.init(MainActivity.this);
        LocationUtil.getLocation(new LocationUtil.LocationListener() {
            @Override
            public void onGetLocationStart() {
                LogUtils.d("----------定位开始---------------");
            }
            @Override
            public void onReceiveLocation(BDLocation location) {
                LogUtils.d("============定位成功=================\n"+location.getAddrStr()+"--->"+location.getCity());
            }
            @Override
            public void onGetLocationTimeOut() {
                LogUtils.d("----------定位超时----------------");
            }
        },3500,true,false);
