def mo(arry, search, low, high):
    while low <= high:
        mid = (low + high) // 2

        if arry[mid] == search:
            return mid
        elif arry[mid] < search:
            low = mid + 1
        else:
            high = mid - 1

    return -1

filee1txt = ["hello python", "hello world", "hello everyone ", "elfalaky"]
filee2txt = ["mohamed elfalaky", "python programming", "good morning", "good evening"]

search = input("enter the word to search: ")

arry = filee1txt + filee2txt
arry.sort()  

result = mo(arry, search, 0, len(arry)-1)
for i in arry:
    if search in i.lower():
        print("Word found in sentence:", i)
    else:        print("Word not found in sentence")
