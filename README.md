# first
python programme
# -*- coding: utf-8 -*-
"""
Created on Thu Mar  1 19:36:06 2018

@author: mamme
"""

def ReturnMax(input):
	tempo=input[0]
	for i in input:
		if i>tempo:
			tempo=i
	return tempo

def DoubleTheValue(input,n):
	tempo=[]
	for i in input:
		tempo.append(i*n)
	return tempo
	
def DisplayList(lst,interval):
	return lst[::interval]
		
def Divisible(input):
	global multiplier
	if(input%multiplier==0):
		isdiv=1
	else:
		isdiv=0
	return isdiv
		
def AcquireTuples(l):	# accepts a list l and returns a pair
	sm=[]
	index,tempo=0,0
	while index<len(l):
		if index==0:
			sm.append(0)
		else:
			sm.append(sum(l[0:index]))
		index=tempo+1
		tempo=index
	return zip(l,sm)
#####################################################################
	
#####################################################################
global multiplier
list=eval(raw_input("Enter set of integers (separated by comma): "))
multiplier=int(raw_input("Enter a multiplier: "))
print (list)
print ("The maximum number in the list is : ",ReturnMax(list))
print ("multiplying it by n is: ",DoubleTheValue(list,multiplier))
print ("the list divisible by ", multiplier," is:")
print (filter(Divisible, list))
ls=eval(raw_input("Enter list of integers: "))
print (ls)
print ("the list with the associated cummulative sum pair is : ")
print (AcquireTuples(ls))
step=int(raw_input("enter the display step size: "))
print ("the list at interval...")
print (DisplayList(ls,step))
