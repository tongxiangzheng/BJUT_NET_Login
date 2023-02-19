$user="21000000" #填入账号
$pwd="password" #填入密码

#后面的不用动
$res=curl -uri "http://10.21.221.98:801/eportal/?c=Portal&a=login&login_method=1&user_account=$user%40campus&user_password=$pwd"
$req=curl -uri "http://lgn6.bjut.edu.cn/V6?https://lgn.bjut.edu.cn" -Method Post -Body "DDDDD=$user&upass=$pwd&v46s=0&v6ip=&f4serip=172.30.201.10&0MKKey=" -UseBasicParsing
$ipv6=($req.Content -split "name='v6ip' value='")[1]
$ipv6=($ipv6 -split "'>")[0]
$res=curl -uri "https://lgn.bjut.edu.cn/" -Method Post -Body "DDDDD=$user&upass=$pwd&0MKKey=Login&v6ip=$ipv6"
