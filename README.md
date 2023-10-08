# Candies
def find_candies_to_eat(N, K, A):
    A.sort(reverse=True)  
    ans = 0
    for i in range(N):
        if A[i] >= K:
            ans += 1
        else:
            break  
    return ans
T = int(input())
for _ in range(T):
    N, K = map(int, input().split())
    A = list(map(int, input().split()))
    print(find_candies_to_eat(N, K, A))
