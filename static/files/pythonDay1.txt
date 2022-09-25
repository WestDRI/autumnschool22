x = 5
if x > 0:
    if x < 5:
        print(x)
    else:
        print("no")


grade = 85
if grade <= 70:
    print('grade is D')
elif grade <= 80:
    print('grade is C')
elif grade <= 90:
    print('grade is B')
else:
    print('grade is A')


grade = 85
if grade >= 90:
    print('grade is A')
elif grade >= 80:
    print('grade is B')
elif grade >= 70:
    print('grade is A')
else:
    print('grade is D')


for letter in word:
    b = letter + b
    print(b)


a = list(word)
a.reverse()
''.join(a)


"computer"[::-1]


a = [1, 2, 3, 4]
b = [1, 2, 5]
for i in a:
    if i not in b:
        print(i, "is not in b")
for i in b:
    if i not in a:
        print(i, "is not in a")


a = [77, 9, 23, 67, 73, 21, 23, 9]
for i in a:
    print(i, "is seen", a.count(i))


for i in set(a):
    print(i, "is seen", a.count(i))


import collections
collections.Counter(a)


while 1==1:
    print("Ok")


sum([x**2 for x in range(1,101)])


def printDate(year, month, day):
  joined = str(year) + '-' + str(month) + '-' + str(day)
  print(joined)


def printDate(year, month, day):
  joined = str(year) + '-' + str(month) + '-' + str(day)
  return(joined)


def celsius(f):
    return (f-32)*5./9.
