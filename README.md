# RandomResults
Using random data, we can create a random-picking machine, with the ability to showcase the results we get graphically using Matplotlib. 
import matplotlib.pyplot as plt
import numpy as np

products = np.array([['Apple','Orange'],
                     ['Beef','Chicken'],
                     ['Candy','Chocolate'],
                     ['Fish','Bread'],
                     ['Eggs','Bacon']])

random = np.random.randint(2, size=5)
choices = []
counter = 0
for product in products:
    choices.append(product[random[counter]])
    counter += 1

print(choices)


percentages = []

for i in range(4):
    percentages.append(np.random.randint(25))
percentages.append(100 - np.sum(percentages))

print(percentages)

plt.pie(percentages, labels=choices)
plt.legend(loc='lower right', ncol=1)

plt.show()
