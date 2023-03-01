n = int(input())
t = [int(i) for i in input().split()]

def custom_sort(x, y):
    if int(str(x) + str(y)) > int(str(y) + str(x)):
        return -1
    else:
        return 1

sorted_t = sorted(t, key=functools.cmp_to_key(custom_sort))
print(''.join([str(i) for i in sorted_t]))
