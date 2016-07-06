# CarManager_QT
QT课程设计内容，汽车销售管理软件  

##开发环境  
QT:4.8.5  
QtCreater:2.8.0  

##预览  
![](https://github.com/XINCGer/CarManager_QT/blob/master/Preview1.png)  
![](https://github.com/XINCGer/CarManager_QT/blob/master/Preview2.png)  
![](https://github.com/XINCGer/CarManager_QT/blob/master/Preview3.png)  

##开发文档  
> 1.菜单设计  
```C++  
    QMenu *manageMenu; //销售管理主菜单  
    QMenu *passwordMenu; //修改密码菜单   
    void on_manageMenu_clicked(); //实现品牌车管理子菜单功能函数  
    void on_chartMenu_clicked(); //实现销售统计子菜单功能函数  
    void on_quitMenu_clicked(); //实现退出子菜单功能函数  
    void createMenuBar(); //用于生成菜单栏的函数  
```

> 2.销售管理   
>* 车辆的数据信息保存在数据库中。创建了两张表，一张厂家表(Factory)，一张品牌表(Brand)。  
厂家表中存放这三家汽车生产商，在品牌表中保存了所有品牌汽车所属的厂家、总量、销售量  
和库存量等数据。销售车辆实际上就是操作品牌表，对其中的销售量和库存量数据进行更新。  
>* 汽车的销售记录使用XML保存，ListWidget中只显示当日的销售记录。XML中按日期和时间  
存储了所销售汽车的数量和金额等信息。  
每完成一次交易就把信息写到XML文件中，然后更新显示。

