# lottos-best-and-worst
# python
# If I bought 6 lottery numbers, the 1st place got all 6, the 2nd place got 5, and the 6th place got 1 or not all the numbers in this order. What will be my best lottery ranking and lowest lottery ranking? 로또번호를 6개 샀는데 1등은 6개 다 맞추고 2등은 5개를 맞추고 이런순으로 6등은 1개변호를 맞추거나 다 맞추지 못한다고 할때, 거기서 0은 내가 어떤 번호를 샀는지 기억이 나지 않는다면 나의 최고로또 순위와 최저로또순위는 어떻게 될까?
def solution(lottos, win_nums):
    answer=[]
    count=0
    nosee=lottos.count(0)
    rank=[6,6,5,4,3,2,1]
    for i in range(len(lottos)):
        if win_nums[i] in lottos:
            count+=1
    answer.append(rank[count+nosee])
    answer.append(rank[count])
    return answer
lottos=[44,1,0,0,31,25]
win_nums=[31,10,45,1,6,19]
a=solution(lottos,win_nums)
print(a)
#result--> [3,5] 왼쪽은 최고순위, 오른쪽은 최저순위
