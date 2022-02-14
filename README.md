- 👋 Hi, I’m @furupon2008
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
furupon2008/furupon2008 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

# coding: utf-8
# Your code here!
# coding: utf-8
# 自分の得意な言語で
# Let's チャレンジ！！
h,w,k = [int(i) for i in input().split()]
#print(h,w,k)
a=[input() for i in range(h) ]
a1=[[0]*w for i in range(h)]
#print(a)
#print(a1)
for i in range(h):
    for j in range(w):
        if a[i][j]=="N":
            i1=i
            j1=j
#print(i1,j1)
d=[[1,0],[0,1],[-1,0],[0,-1]] #d,r,u,l
#print(d[1][0])
que=[[i1,j1]]
ans=[]
i0=i1
j0=j1
ds=abs(i0-i1)+abs(j0-j1)
dm=0
#print(ds)
for i in que:
    y=i[0]
    x=i[1]
    if a[y][x]=="#" or a[y][x]=="N":
      a1[y][x]=1
    else:
      a1[y][x]=1
      if dm==0:
        dm=abs(i0-y)+abs(j0-x)
      if dm==abs(i0-y)+abs(j0-x):
        ans.append(int(a[y][x]))
        #print(dm,ans)
      else:
        break
    #if len(ans)!=0:
    #  break
    for j in range(4):
        y1=y+d[j][0]
        if y1<0 or y1>h-1:
          continue
        x1=x+d[j][1]
        if x1<0 or x1>w-1:
          continue
        if a1[y1][x1]==1:
          continue
        que.append([y1,x1])
        a1[y1][x1]=1
        #print(ans,y1,x1,a1)
ans.sort()
#print(ans)
print(len(ans))
for i in ans:
  print(i)
