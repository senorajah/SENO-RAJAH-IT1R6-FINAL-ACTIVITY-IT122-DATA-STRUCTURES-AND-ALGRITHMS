# SENO-RAJAH-IT1R6-FINAL-ACTIVITY-IT122-DATA-STRUCTURES-AND-ALGRITHMS
chapter 9
A graph is a data structure made up of a limited number of nodes (or vertices) and the edges that connect them. An edge is a pair of vertices (x,y) that conveys that the x vertex links to the y vertex.It's also a graphical depiction of a group of items, with some pairs of items linked together by connections. The points that connect the interconnected objects are called vertices, and the links that connect the vertices are called edges.

chapter 10
The binary search algorithm, also known as half-interval search, logarithmic search, or binary chop, discovers the position of a target value inside a sorted array. The target value is compared to the array's middle element in a binary search.By splitting the search interval in half repeatedly, a sorted array may be created. Begin by creating an interval that spans the whole array. If the search key's value is less than the item in the interval's midpoint, the interval should be narrowed to the bottom half. Otherwise, limit it to the upper half

chapter 11
The simplest sorting algorithm is Bubble Sort, which operates by periodically exchanging nearby components if they are in the wrong order.In computing, this is one of the most basic types of sorting. Bubble sort algorithms run through a set of data (usually numbers) and rearrange them one by one into ascending or descending order. To do this, the algorithm compares number X to the adjacent number Y.

chapter 12
Quicksort is a sorting algorithm that employs a divide-and-conquer strategy. A pivot element is used to split an array into subarrays.which is a term often used in the field of computer science. Quick Sort employs a divide-and-conquer strategy. It makes two empty arrays to contain elements less than the pivot value and items more than the pivot value, and then sorts the subarrays recursively.

chapter 13
Insertion sort is a straightforward sorting algorithm that works similarly to how you arrange cards in your hands.The lowest half of an array is kept in order to sort it. An element that has to be 'inserted' into this sorted sub-list must first locate its proper location before being inserted. As a result, the term "insertion sort" was coined.

chapter 14
Merge Sort, like QuickSort, is a Divide and Conquer algorithm. It splits the input array into two half, as seen below.Merge sort is an example. To sort and combine the two adjacent lists, first partition the list into the smallest unit (1 element), then compare each element with the adjacent list. After that, all of the components are sorted and combined.

chapter 15
Shell sort is a sorting algorithm that is based on the insertion sort method and is very efficient. When the smaller value is on the far right and must be pushed to the far left, this technique avoids huge shifts as in insertion sort.The “diminishing increment sort,” as it is often known, improves on the insertion sort by dividing the original list into smaller sublists, each of which is sorted using an insertion sort.

chapter 16
A basic sorting algorithm is selection sort. This sorting method is based on in-place comparison and divides the list into two parts: the sorted part on the left end and the unsorted part on the right. The sorted section is initially empty, but the unsorted section contains the complete list.Basically, it's a selection of an element's starting location in relation to the rest of the elements. According to the condition, elements are compared and swapped, and the selection point is transferred to the next position till it reaches the finish.

chapter 17
Recursion is the capacity of a function or procedure to solve a problem by invoking itself. Recursion is the technique of addressing a problem by breaking it down into smaller versions of itself. The procedure by which a function calls itself can take place both directly and indirectly.The data structure is partially made up of smaller or simpler versions of the same data structure. A tree, for example, is made up of smaller trees (subtrees) and leaf nodes, whereas a list might contain other lists as components.

 def get_num(self):
        return self.num
 def get_den(self):
        return self.den
        
  def __add__(self, other):
        new_num = (self.num * other.den) + (self.den * other.num)
        new_den = self.den * other.den
        return Fraction(new_num, new_den)
   def __radd__(self, other):
        if other == 0:
            return self
        else:
            other = Fraction(other, 1)
            return self.__add__(other)
         
    def __str__(self):
        return str(self.num) + "/" + str(self.den)
      def __repr__(self):
        return '%s(%r)' % (self.__class__, self.__str__())

    def show(self):
        print (self.num, "/", self.den)
        
   
   
   
   
   
   class Card:
    SUITS = ('Clubs', 'Diamonds', 'Hearts', 'Spades')
    RANKS = ('narf', 'Ace', '2', '3', '4', '5', '6', '7',
             '8', '9', '10', 'Jack', 'Queen', 'King']

    def __init__(self, suit=0, rank=0):
        self.suit = suit
        self.rank = rank

    def __str__(self):
        """
          >>> print(Card(2, 11))
          Queen of Hearts
        """
        return '{0} of {1}'.format(Card.RANKS[self.rank],
                                   Card.SUITS[self.suit])


if __name__ == '__main__':
    import doctest
    doctest.testmod()
    
    
    def __cmp__(self, other):
    # check the suits
    if self.suit > other.suit: return 1
    if self.suit < other.suit: return -1
    # suits are the same... check ranks
    if self.rank > other.rank: return 1
    if self.rank < other.rank: return -1
    # ranks are the same... it's a tie
    return 0
    
    class Deck:
    def __init__(self):
        self.cards = []
        for suit in range(4):
            for rank in range(1, 14):
                self.cards.append(Card(suit, rank))
      class Deck:
    ...
    def print_deck(self):
        for card in self.cards:
            print(card)
     class Deck:
    ...
    def __str__(self):
        s = ""
        for i in range(len(self.cards)):
            s += " " * i + str(self.cards[i]) + "\n"
        return s
    >>> deck = Deck()
>>> print(deck)
Ace of Clubs
 2 of Clubs
  3 of Clubs
   4 of Clubs
     5 of Clubs
       6 of Clubs
        7 of Clubs
         8 of Clubs
          9 of Clubs
           10 of Clubs
            Jack of Clubs
             Queen of Clubs
              King of Clubs
               Ace of Diamonds
    random.randrange(0, len(self.cards))
    
  
  
  
  
  
Enqueue and Dequeue tend to be operations on a queue, a data structure that does exactly what it sounds like it does.
You enqueue items at one end and dequeue at the other, just like a line of people queuing up for tickets

import random

def enqueue(lst, itm):
    lst.append(itm)       
    return lst             
def dequeue(lst):
    itm = lst[0]          
    lst = lst[1:]         
    return (itm, lst)     
myList = []

for _ in range(15):
    if random.randint(0, 9) == 0 and len(myList) > 0:
        (itm, myList) = dequeue(myList)
        print(f"Dequeued {itm} to give {myList}")
    else:
        itm = 10 * random.randint(1, 9)
        myList = enqueue(myList, itm)
        print(f"Enqueued {itm} to give {myList}"

print("========")
while len(myList) > 0:
    (itm, myList) = dequeue(myList)
    print(f"Dequeued {itm} to give {myList}")
        
        
        
        
  class Queue(object):
    def __init__(self):
        self.items = []

    def isEmpty(self):
        return self.items == []

    def enqueue(self, item):
        self.items.insert(0, item)

    def dequeue(self):
        return self.items.pop()

    def size(self):
        return len(self.items)



# Radix Sorting Machine
def radixSorting(base, num):
    main = Queue()
    sub_bins = [Queue() for i in range(base)]
    int_str = ''
    while num > 0:
        n = num % base
        sub_bins[n].enqueue(n)
        num = num // 10
    for q in sub_bins:
        while q.size() > 0:
            int_str = int_str + str(q.dequeue())
    return int_str

#print radixSorting(10, 9342354)        



# Airplanes landing simulation

# New plane arrives in airspace on average every 10 minutes
# It takes 7 minutes to land the plane before another plance can land
# Planes must wait their turn to land


import random

class Plane(object):
    def __init__(self, num, current_time):
        self.arrive_time = current_time
        self.num = num

    def getArriveTime(self):
        return self.arrive_time

    def getPlaneNum(self):
        return self.num


class Airport(object):
    def __init__(self):
        self.arrivals = Queue()
        self.wait_times = []
        self.plane_count = 1
        self.busy = False
        self.runwayTimer = 1

    def addPlane(self, current_time):
        self.arrivals.enqueue(Plane(self.plane_count, current_time))
        self.plane_count += 1

    def landPlane(self, current_time):
        p = self.arrivals.dequeue()
        self.addWaitTime(current_time, p.getArriveTime())
        self.busy = True

    def addWaitTime(self, current_time, arrive_time):
        self.wait_times.append(current_time - arrive_time)

    def isRunwayBusy(self):
        return self.busy

    def clearRunway(self):
        if self.runwayTimer == 7:
            self.busy = False
            self.runwayTimer = 1
        self.runwayTimer += 1

    def waitingToLand(self):
        return self.arrivals.size()


def randomArrival(arrival_num):
    chance = random.randrange(1,arrival_num+1)
    return chance == 10
        

def airport_simulation(time):
    a = Airport()
    current_time = 0
    while current_time < time:
        current_time += 1
        if randomArrival(10):
            a.addPlane(current_time)
        if a.waitingToLand() > 0:
            if not a.isRunwayBusy():
                a.landPlane(current_time)
            else:
                a.clearRunway()
    return a.wait_times, a.waitingToLand()


def average(num_list):
    return float(sum(num_list)) / len(num_list)

#wait_times, planes_remaining = airport_simulation(10000)
#i = 0
#for time in wait_times:
#    i += 1
#    print "Wait time %d: %d minutes" % (i, time)

#print "%d total planes landed" % len(wait_times)
#print "%d planes remaining" % planes_remaining
#print "Average wait time: %d minutes" % average(wait_times)
    


# Deque Class Implementation
class Deque(object):
    def __init__(self):
        self.items = []

    def size(self):
        return len(self.items)

    def isEmpty(self):
        return self.items == []

    # Add item to left side of list
    def addFront(self, item):
        self.items.append(item)

    # Add item to RIGHT side of list
    def addRear(self, item):
        self.items = self.items.insert(0,item)

    # Remove and return item on the RIGHT side of list
    def removeFront(self):
        return self.items.pop()

    # Remove and return item on the LEFT side of list
    def removeRear(self):
        return self.items.pop(0)


html_doc = """
<html>
   <head>
      <title>
         Example
      </title>
   </head>
   <body>
      <h1>Hello, world</h1>
   </body>
</html>
"""

# Returns True if string is valid HTML 
def validHTML(html):
    d = Deque()
    i = 0
    # < == 'o'
    # > == 'c'
    # </ == 'e'
    # Add bracket elements to Deque
    while i < len(html):
        if html[i:i+2] == '</':
            print "adding close tag"
            d.addFront('e')
            i += 2
        elif html[i] == '<':
            d.addFront('o')
            i += 1
        elif html[i] == '>':
            d.addFront('c')
            i += 1
        else:
            i += 1

    # Analyze Deque brackets
    open_count = 0
    close_count = 0
    while d.size() > 1:
        next_str = d.removeRear() + d.removeRear()
        print next_str
        if close_count > open_count:
            print "close count greater than open count"
            return False
        elif next_str not in ['oc','ec']:
            print "bracket not valid HTML"
            return False
        elif next_str == 'oc':
            open_count += 1
        elif next_str == 'ec':
            close_count += 1
    print open_count
    print close_count
    return open_count == close_count


#print validHTML(html_doc)



# Returns deque filled with HTML brackets
def extractBrackets(html):
    d = Deque()
    # < == 'o'
    # > == 'c'
    # </ == 'e'
    # Add bracket elements to Deque    
    i = 0
    while i < len(html):
        print i
        if html[i:i+2] == '</':
            d.addRear('e')
            i += 2
        elif html[i] == '<':
            d.addRear('o')
            i += 1
        elif html[i] == '>':
            d.addFront('c')
            i += 1
        else:
            i += 1
    return d

#tmp = extractBrackets(html_doc)
#while tmp.size() > 1:
#    print tmp.removeRear()
#    print tmp.removeFront()

#def validHTML2(html):
#    d = extractBrackets(html)

from lists import Node, LinkedList



class Stack:
    def __init__(self):
        self.items = LinkedList()

    def getItems(self):
        return self.items

    def size(self):
        return self.items.size()

    def push(self, item):
        self.items.append(item)

    def pop(self):
        return self.items.pop()

    def isEmpty(self):
        return self.items.isEmpty()
    


'''
s1 = Stack()
print s1.size()
print s1.push('hey')
print s1.pop()
print s1.push(3)
print s1.push(2)
print s1.getItems()
print s1.size()
print s1.isEmpty()
'''

class Queue(object):
    def __init__(self):
        self.items = []
        # Store the index of the last item for constant time push and pop
        self.last = -1

    def isEmpty(self):
        return self.items == []

    def enqueue(self, item):
        self.last += 1
        self.items.insert(0, item)

    def dequeue(self):
        self.last -= 1
        return self.items.pop()
        
    def size(self):
        return len(self.items)
        
        
  struct QNode {
    int data;
    QNode* next;
    QNode(int d)
    {
        data = d;
        next = NULL;
    }
};
  
struct Queue {
    QNode *front, *rear;
    Queue()
    {
        front = rear = NULL;
    }
  
    void enQueue(int x)
    {
  
        // Create a new LL node
        QNode* temp = new QNode(x);
  
        // If queue is empty, then
        // new node is front and rear both
        if (rear == NULL) {
            front = rear = temp;
            return;
        }
  
        // Add the new node at
        // the end of queue and change rear
        rear->next = temp;
        rear = temp;
    }
  
    // Function to remove
    // a key from given queue q
    void deQueue()
    {
        // If queue is empty, return NULL.
        if (front == NULL)
            return;
  
        // Store previous front and
        // move front one node ahead
        QNode* temp = front;
        front = front->next;
  
        // If front becomes NULL, then
        // change rear also as NULL
        if (front == NULL)
            rear = NULL;
  
        delete (temp);
    }
};
  
// Driven Program
int main()
{
  
    Queue q;
    q.enQueue(10);
    q.enQueue(20);
    q.deQueue();
    q.deQueue();
    q.enQueue(30);
    q.enQueue(40);
    q.enQueue(50);
    q.deQueue();
    cout << "Queue Front : " << (q.front)->data << endl;
    cout << "Queue Rear : " << (q.rear)->data;
    
    





def recur_factorial(n):
   if n == 1:
       return n
   else:
       return n*recur_factorial(n-1)

num = 7


if num < 0:
   print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
   print("The factorial of 0 is 1")
else:
   print("The factorial of", num, "is", recur_factorial(num))
   
   
   
   
   
   
  In [ ]:
def sequentialSearch(alist, item):
    pos = 0
    found = False
    
    while pos < len(alist) and not found:
        if alist[pos] == item:
            found =  True
        else:
            pos = pos+1
            
    return pos

testlist = [1, 2, 32, 8, 17, 19, 42, 13, 0]
item = 2
k = sequentialSearch(testlist, item)
if k <= len(testlist)-1:
    print('The item t= %s was found at testlist[%s]') %(item, k)
else:
    print('The item t= %s was not found.' %item)
    
    
    
    
    
    
    
    
    
    
    
  class StolenItem:
	def __init__(self, theID, theValue, theWeight):
		self.ID = theID
		self.value = theValue
		self.weight = theWeight

def dpMaxProfit (itemList, knapWeight, maxProfits, weightsUsed):
	maxProfit = 0

	for knapWeights in range (knapWeight + 1):
		print "KNAPWEIGHT:", knapWeights - 1, " ", maxProfits
		newItem = itemList[0]

		for item in [x for x in itemList if x.weight <= knapWeights]:
			if maxProfits[knapWeights - item.weight] + item.value > maxProfit: 
				maxProfit = maxProfits[knapWeights - item.weight] + item.value
				newItem = item
		maxProfits[knapWeights] = maxProfit
		weightsUsed[knapWeights] = newItem.weight

	return(maxProfits[knapWeight])
	
def reMaxProfit(itemList, knapWeight):
	if knapWeight < 1:
		return 0 

	l1 = [x for x in itemList if x.weight <= knapWeight]	
	profitList = [(item.value + reMaxProfit(itemList, knapWeight-item.weight)) for item in l1]

	if len(profitList) > 0:
		return max(profitList)
	else:
		return 0 
		
def _weightsUsed(weightList, knapWeight):
	weight = knapWeight
	while weight > 0:
		print(weightList[weight])
		weight -= weightList[weight]
recurse = True
if recurse:
	maxProfits = [0] * (knapWeight + 1)
	weightsUsed = [0] * (knapWeight + 1)

def main():
	itemList = [StolenItem(1,3,2), StolenItem(2,4,3), StolenItem(3,8,4), StolenItem(4,8,5), StolenItem(5,10,9)]
	knapWeight = 20
	if !recurse:
		maxProfits = [0] * (knapWeight + 1)
		weightsUsed = [0] * (knapWeight + 1)
		print(dpMaxProfit(itemList, knapWeight, maxProfits, weightsUsed))
		print _weightsUsed(weightsUsed, knapWeight)
	else:	
		print (reMaxProfit(itemList, knapWeight))

if __name__ == "__main__":
	main()
  
  
  
  
  
