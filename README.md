1.  
c=a+b, вывод a+b, это строка, чтобы указать переменную нужно использовать $.  
d=$a+$b, вывод 1+2, переменные a,b указаны неявно, поэтому их значения это строки, происходит сложение строк.  
e=$(($a+$b)), вывод 3, значения преобразуются в целочисленные, поэтому их можно сложить.    

2.    
while ((1==1))  
do  
curl https://localhost:4757  
if (($? != 0))  
then  
date >> curl.log  
else  
break  
fi  
done  

3.  
array=(192.168.0.1 173.194.222.113 87.250.250.242)  
array_count=(0 1 2 3 4)  

for i in ${array[@]}  
do  
	for j in ${array_count[@]}  
	do  
	telnet $i 80 >> telnet.log  
	done  
done  

4.  
array=(192.168.0.1 173.194.222.113 87.250.250.242)  
array_count=(0 1 2 3 4)  

for i in ${array[@]}  
do  
	for j in ${array_count[@]}  
	do  
	telnet $i 80 >> telnet.log  
	done	  
	if (($? != 0))  
	then  
	echo $i >> error.log  
	break  
	fi  
	
done  
