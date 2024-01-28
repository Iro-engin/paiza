gyou,retu = map(int,input().split())

bannmenn_list = [list(map(str,input())) for i in range(gyou)]

y,x = map(int,input().split())

command=[[1,0],[-1,0],[0,1],[0,-1],[1,1],[1,-1],[-1,1],[-1,-1]]

#飛車＆角
for k in range(max(gyou,retu)):
    for i in range(8):
        if 0 <= y-k*command[i][0] < gyou and 0 <= x-k*command[i][1] < retu: 
            if bannmenn_list[y-k*command[i][0]][x-k*command[i][1]] == "#":
                bannmenn_list[y-k*command[i][0]][x-k*command[i][1]] = "."
            else:
                bannmenn_list[y-k*command[i][0]][x-k*command[i][1]] = "#"
                
                
#本体
if bannmenn_list[y][x]=="#":
   bannmenn_list[y][x]="."
   
else:
    bannmenn_list[y][x]="#"
    
for i in range(gyou):
    p=""
    for j in range(retu):
        p=p+bannmenn_list[i][j]
    print(p)
