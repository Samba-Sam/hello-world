# hello-world-2.0

#Experiment 5

import random

print("1 = Rock , 2 = Paper , 3 = Sisscor")

x = int(input(" Input R(1),P(2),S(3) : "))
print(x)


y = random.randint(1,3)
print( y )

if x ==y:
 print("Tie")
elif( x == 1 and y == 3):
  print("You Wins")
elif( x == 2 and y == 1):
  print("You Wins")
elif( x == 3 and y == 2):
  print("You Wins")
else:
  print("Bot Wins")


 #Experiment 6

class Person:
  def __init__(self , name , is_man):
   self.name = name
   self.is_man = is_man

sid = Person("Sid",True)
water = Person("Water",False)

def test(person):
  return person.is_man 
  

print(test(sid))

print(test(water))

#Exp 3: 
from collections import deque

graph = {
'A' :['B','C'],
'B' : ['A','D','E'],
'C' : ['F','A'],
'D' : ['B'],
'E' : ['F','B'],
'F' : ['C','E']
}

def bfs(graph, start_node):
 visited = set()         # Keep track of visited nodes
 queue = deque([start_node])
 visited.add(start_node)

 while queue:

  current = queue.popleft()
  print(current, " ")

        # Check all neighbors
  for neighbor in graph[current]:
    if neighbor not in visited:
      visited.add(neighbor)
      queue.append(neighbor)

bfs(graph,'B') # Corrected: 'A' should be a string





from collections import deque

graph = {

'A' : ['B','C'],
'B' : ['A'],
'C' : ['A']
}

def bfs(graph , start_node):
 v = set()
 queue = deque([start_node])
 v.add(start_node)
 
 while queue:

  now = queue.popleft()
  print(now)

  for i in graph[now]:
    if i not in v :
      v.add(i)
      queue.append(i)

bfs(graph , 'A')
