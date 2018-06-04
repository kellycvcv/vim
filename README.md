# vim
 cat    ID_card.table  | awk -F"," '{print $4 $6,$9}'

awk 'NR==FNR{a[$3]=$0;next}NR>FNR{if($3 in a)print $0"\n"a[$1]}' number.txt table.txt

 awk 'NR==FNR{a[$3]=$3;next}NR>FNR{if($3 in a)print $2" "$1 a[$1]}' number.txt table.txt


awk 'NR==FNR{a[$3]=$3;next}NR>FNR{if($3 in a)print $2{-F"." '{print $1}'}a[$1]}' number.txt table.txt 

 awk 'NR==FNR{a[$3]=$3;next}NR>FNR{if($3 in a)print $2| awk -F"," '{print $1}'" "$1 a[$1]}' number.txt table.txt

cat name_train_list.txt | awk '{print $1"\t"$2}' > name_train_list.txt.1


awk 'NR==FNR {a[$1]=$2; next}  a[$1]' data.txt ID_third90.txt | head

cat ocr_name_data.txt |awk -F "_" '{print $NF}' |awk -F "." '{print $1}'
awk 'NR==FNR{a[NR]=$0;nr=NR;}NR>FNR{print a[NR-nr]"\t"$0}' ocr_name_data.txt ocr_name_data.txt2 >ttt.txt



ssh 01338029@shterm.sf-express.com


ls -l |grep "^-"|wc -l
ls -lR|grep "^d"|wc -l

Vim 删除不包含指定字符串的行：

    :g/xxx/d，删除包含xxx的行

    :v/xxx/d，删除不含xxx的行

:%s/xxx//gn，统计xxx个数，n表示只报告匹配的个数而不进行实际的替换。 

:g/吖/d
剔除字符库没有的字：蝈、逯、囡，谌，吖，咩，哚，啵，蝌，蚪，烊，　霈，庹，洵，唰，嫒，芤


docker ps -a | grep "Exited" | awk '{print $1 }'|xargs docker stop
docker ps -a | grep "Exited" | awk '{print $1 }'|xargs docker rm
sudo docker ps -a | grep Exited | awk '{print $1}' | xargs -i sudo docker rm -f {}
 sudo docker images|grep none|awk '{print $3}'| sudo xargs docker rmi

