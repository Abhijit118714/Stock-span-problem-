for i in range(int(input())):
    s=[]
    v=[]
    n=int(input())
    a=[int(i) for i in input().split()]
    for i in range(len(a)):
        if(s==[]):
            v.append(-1)
            s.append([a[i],i])
        else:
            if(s[-1][0]>a[i]):
                v.append(s[-1][1])
                s.append([a[i],i])
            else:
                while(s!=[] and s[-1][0]<=a[i]):
                    s.pop()
                if(s==[]):
                    v.append(-1)
                    s.append([a[i],i])
                else:
                    v.append(s[-1][1])
                    s.append([a[i],i])
            
    for i in range(len(v)):
        print(i-v[i],end=' ')
    print()
        
