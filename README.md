# JigsawProteinPuzzleThing

####EDIT

def findOverlaps(seq):
    from lineArray import lineArray
    array=lineArray(seq)
    overlaps=[]
    i=1
    j=1
    part=''
    bool=True
    while j<15:
        part=array[0]
        part=part[j:15]
        while i<len(array):
            if bool and part in array[i]:
                print array[i]
                bool=False
            i+=1
    return

findOverlaps('testSeq.txt')



def lineArray(filename):
    array=[]
    with open(filename, 'r') as file:
        while True:
            line=file.readline().rstrip()
            if not line: break
            array.append(line)
#    for line in array:
#        print line
    return array

lineArray('testSeq.txt')

#edit
