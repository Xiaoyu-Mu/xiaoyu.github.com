## Welcome to Xiaoyu's Pages

<table border="0">
  <tr>
    <td width="75%">
      <h1> Xiaoyu Mu</h1>
      <p><b>- 👋Hi, I’m Xiaoyu Mu, a postgraduate of University of Leeds.</b></p>
      <p><b>- 👀 I’m interested in watching films, programming, running, sharing my life...</b></p>
      <p><b>- 💞️ I’m looking to a good job.</b></p>
      <p><b>- 🌱 I’m currently learning Advanced Computer Science.</b></p>
      <p><b>- 📫 How to reach me:  xiaoyu_fish@outlook.com</b></p>
    </td>
    <td width="25%">
      <img src="XiaoyuMu.png">      
    </td>
  </tr>
</table>


### Education
09/2021-09/2022   MSc in Advanced Computer Science, University of Leeds


09/2017-07/2021   BSc in Computer Science, Yantai University

### Skills

- C++
- Python 
- Tableau
- SQL
- C
- Linux
- Opencv
 
### Awards

- Excellent bachelor’s degree thesis of College (top 2%), Yantai University, 2021
- School-level outstanding graduate awards (top 2%), Yantai University, 2021
- The Outstanding Student Scholarship (top 8%), Yantai University, 2020
- The Xinde Enterprise Encouragement Scholarship (top 2%), Yantai University, 2019
- The National Second Prize of ASC International Student CS Challenge, China, 2019
- The Third Prize of Blue Bridge Cup Coding Competition, Shandong, China, 2019
- The Third Prize of Provincial Mathematics Competition, Shandong, China, 2018
- The Golden Dragon Enterprise Scholarship (top 4%), Yantai University, 2018

### Projects
11/2021-12/2021  Group Project - Data Analysis with Python, University of Leeds
- Skills in Python, Matplotlib Method to draw different graphs.
- Analyse and visualise data in the CSV files, and explain the cause and result of the problem according to data features and trends.
```
def pltcorrCO2GDP(co2,gdp,area):

    plt.plot(co2.keys(), co2.values())

    # Label the axes
    plt.xlabel('Year')
    plt.ylabel(co2data['Indicator Name'].iloc[0])

    #label the figure
    plt.title('CO2 Emissions and GDP per capita in '+area)

    #set x axis ticker
    ax = plt.gca()
    ax.xaxis.set_major_locator(ticker.MultipleLocator(base=8))

    #plot gdp data
    ax1=ax.twinx()
    ax1.plot(gdp.keys(),gdp.values(),'r')
    ax1.set_ylabel(gdpdata['Indicator Name'].iloc[0])
    ax1.xaxis.set_major_locator(ticker.MultipleLocator(base=8))

    plt.show()
```
![Image](P4DS1.png)

11/2021-12/2021  Group Project - Analysis Case Study, University of Leeds
- Skills in Tableau, visualise data using Tableau.
- Analyse data about NHS Dental Statistics for England for 12 months.
![Image](Tableau2.png)
![Image](Tableau1.png)
![Image](Tableau3.png)
11/2020-06/2021  Final Year Project - Recognition Circular Pattern Plane Target Based on Graph Algorithm, Yantai University
- Skills in C++, Clustering, Graph Theory, Calibrate Camera, Convex Algorithms,Homography Matrix Algorithms, Shortest Distance Algorithms.
- Take pictures of the target, identify the circles, and calculate the center of thecircles. Finally, select and order the circles. This technique is ised to calibratecamera in computer vision.

```
//image processing
cvtColor(src, gray_src, COLOR_BGRA2GRAY); 
threshold(gray_src, gray_src, 0, 255, THRESH_OTSU | THRESH_BINARY); 
Mat kernel = getStructuringElement(MORPH_RECT, Size(5, 5), Point(-1, -1)); 
morphologyEx(gray_src, dst, MORPH_CLOSE, kernel, Point(-1, -1)); 
kernel = getStructuringElement(MORPH_RECT, Size(5, 5), Point(-1, -1)); 
morphologyEx(dst, dst, MORPH_OPEN, kernel, Point(-1, -1)); 
imshow("open image", dst); 
vector <vector<Point> > contours; 
vector<Vec4i> hireachy; 
findContours(dst, contours, hireachy, RETR_TREE, CHAIN_APPROX_SIMPLE, Point());

//get Homography Matrix 
Mat h = findHomography(tubaodian, tubaodian1);//opencv function
Mat q= Mat(3, 1, CV_32FC1);
```

![Image](Finalyearproject.png)


05/2020-06/2020  Group Project - Developing a Web Application, Yantai University
- Skills in HTML and CSS, and MySQL.
- Developed a web application for the Intelligent Home System.

``` 
//初始化本机socket信息
$this->_init($address, $port);
//将socket加入到连接池中
$this->sockets[] = $this->master;
//监听和数据处理
while(true){
//得到连接池
$sockets = $this->sockets;
var_dump($sockets);
var_dump($this->clients);
//IO复用完成多客户端，$sockets为引用型参数，最后得到的为有主机连接或者有数据接收的socket集合
$symbol = socket_select($sockets, $this->write, $this->except, NULL);
if($symbol == false){
echo"socket_select() failed,reason:".socket_strerror(socket_last_error())."\n";
die();
}
//遍历socket进行接收收据
foreach($sockets as $socket){
//有主机要连接数据
if($socket == $this->master){
//绑定客户端
$client = socket_accept($this->master);
if($client){
//表示接收到客户端
//加入socket连接池和用户池
$this->sockets[] = $client;
$this->clients[] = array('familyNo'  => null,//家庭号
'is_user'	=> false,	//表明是否为用户
'socket' => $client,//握手信息
'handshake' => false
);
}else{
echo "socket_accept() failed";
continue;	//处理其它socket
}
}else{
//接收数据
$bytes = @socket_recv($socket, $buffer, 2048 ,0);
$index = $this->_getUserIndex($socket);	//输出用户信息
if($index == -1){continue;}
//得到用户下标
if($bytes == 0){
//断开服务器与客户端的连接
$this->_disConnect($socket);
//将用户去掉
$this->_deleteUser($index);
continue;
}
if(!$this->clients[$index]['handshake']){
//握手
if($this->_doHandShake($socket, $buffer, $index)){
echo "handshake success!\n";
$msg = array(
'infoNo'=>'0',
'info'	=>"握手成功"	//加密问题
);	//ok
$this->_send($socket, json_encode($msg));
}else{
//得到家庭号
echo "send message\n";
//得到数据部分并进行json解密
$info = json_decode($this->_decode($buffer));

```

![Image](homesystem.png)
