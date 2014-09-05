12306REST
=========

12306接口解析


请求车票详情

url:
    https://kyfw.12306.cn/otn/leftTicket/queryT
params:
    leftTicketDTO.train_date    出发时间
        =2014-09-05&
    leftTicketDTO.from_station  始发站
        =BJP&
    leftTicketDTO.to_station    目的站
        =WHN&
    purpose_codes=              票类型
        ADULT   成人
        0X00    学生票

response:
    {
        "validateMessagesShowId": "_validatorMessage",
        "status": true,
        "httpstatus": 200,
        "data": [
            {
                "queryLeftNewDTO": { // 数组为每一个车次的数据
                    "train_no": "240000G52502", // 车次编号
                    "station_train_code": "G525",   // 车次
                    "start_station_telecode": "BXP",// 车次英文编号
                    "start_station_name": "北京西",    //始发站
                    "end_station_telecode": "HKN",
                    "end_station_name": "汉口",
                    "from_station_telecode": "BXP",
                    "from_station_name": "北京西",
                    "to_station_telecode": "HKN",
                    "to_station_name": "汉口",
                    "start_time": "17:14",
                    "arrive_time": "22:54",
                    "day_difference": "0",
                    "train_class_name": "",         // 分类，用不上
                    "lishi": "05:40",
                    "canWebBuy": "N",
                    "lishiValue": "340",
                    "yp_info": "O000000000M0000000009000000000",
                    "control_train_day": "20201231",
                    "start_train_date": "20140905",
                    "seat_feature": "O3M393",
                    "yp_ex": "O0M090",
                    "train_seat_feature": "3",
                    "seat_types": "OM9",
                    "location_code": "P2",
                    "from_station_no": "01",
                    "to_station_no": "13",
                    "control_day": 29,
                    "sale_time": "1400",
                    "is_support_card": "0",
                    ----------------------座位类型只需要解析我注释的11种，其他的类型都已经不存在，或者是以后才会用到的
                    "yz_num": "--",     //硬座 余票
                    "rz_num": "--",     //软座
                    "yw_num": "--",     //硬卧
                    "rw_num": "--",     //软卧
                    "gr_num": "--",     //高级软卧
                    "zy_num": "无",     //一等座
                    "ze_num": "无",      // 二等座
                    "tz_num": "--",     //特等座
                    "wz_num": "--",     //无座
                    "qt_num": "--",     // 其他
                    "swz_num": "无"      //商务座
                },
                "secretStr": "",
                "buttonTextInfo": "预订"
            },
            {
            }.....
        ]
    }
