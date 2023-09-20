import csv
from scipy.stats import pearsonr
from typing import List
def generatePercentages():
    #countIndex=0
    foundItem2=False
    uniqueValues=[]
    uniqueValues3=[]
    #races:List[str]=[]
    xx=0
    y=0
    #counts2=[]
    #counts3=[]
    #arrayLimits=[]
    target=""
    for column in range(0,len(freqColumns)):
        
        #uniqueValues.append(target)
        counts2=[]
        counts2.append(1.0)
        
        y=0
        #arrayLimits=[]
        uniqueValues=[]
        
        #uniqueValues.append(data[y][column])
        uniqueValues.append(data[column][y])
        nUniqueValues=1
        y+=1
        #print(f'len data={len(data[column])}')
        while (y<len(data[column])):
            target=data[column][y]
            #print(f'target={target}')
            foundItem2=False
            
            xx=0
            for u in uniqueValues:
                
                if target==u:
                    foundItem2=True
                    countIndex=xx
                    #counts2[countIndex]+=1.0
                    #print("FoundItem*** u=\(u) target=\(target) xx=\(xx)")
                #end foundItem
                xx+=1
            #end u
            
            if foundItem2:
                counts2[countIndex]+=1.0
            
            else:
                
                uniqueValues.append(target)
                nUniqueValues+=1
                #print("uniqueValues=\(uniqueValues) xx=\(xx)")
                counts2.append(1.0)
                #countIndex+=1
            
            
            
            y+=1
        #end while
        counts3.append(counts2)
        arrayLimits.append(nUniqueValues)
        uniqueValues3.append(uniqueValues)
    #end for columns
    """        
    for c in 0...counts.count-1 {
      //  counts[c]=counts[c]*100.0/nCases
    //}
    //print(counts2)
    //xArray=[]
    //print(counts2)
    """
    return uniqueValues3
def toFloat(str0:str):
    str2=str0.strip()
    nDecimals=0
    neg=False
    if str0=="":
        return 0.0
    if str2[0]=='-':
        neg=True
    str3=''
    for i in str2:
        if (i.isnumeric() or i=='.'):
            if i==".":
                nDecimals+=1
            str3+=i
    if (str3=="") or (str3==".") or (nDecimals>1):
        return 0.0
    #print(str3)
    if neg:
        return float(str3)*(-1.0)
    return float(str3)
#activeColumns=[0,1,2,3,4,5,6,7] for tsla_split_adjusted
#freqColumns=[8] for tsla
#activeColumns=[3,6,9,11,15,18,19,21,27,30,31,32] #for porsche_911
#activeColumns=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22] #for smoking driking dataset
#activeColumns=[1,2,5,6,7,9] #titanic
#freqColumns=[1,2,4,6,7,11]  #titanic
#activeColumns=[0,1,2,3,4,5,8,9,10,11,12,13,14,15,16,17,18,19,20,21] #crimes
#freqColumns=[6] #crimes
#activeColumns=[1,12] #fatal police shootings
#freqColumns=[2,3,4,7,13,14,16,17] #fatal police shootings
#activeColumns=[1,3,4,5,6,9,10,13,14,15,16,17,18,19,21,22,23,26,27,30,31,32] #world-data-2023
#freqColumns=[24] #world-data-2023
#activeColumns=[1,9,10,11,12,13,14,15,16,17,18] #kaggle income
#freqColumns=[2,10] #kaggle income
#activeColumns=[1,3,4,5,6,7] #deciles
#freqColumns=[0] #deciles
#activeColumns=[2,3,4,5,6,7,8] #exercise
#freqColumns=[1] #exercise
#activeColumns=[2,3,4,5,7,8,9] #exercise2
#freqColumns=[6] #exercise2
#activeColumns=[0,1,2,3,4,5,6,7,8,9,10,11,12,13] #heart
#freqColumns=[1] #heart
#activeColumns=[2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46] #demographic
#freqColumns=[3] #demographic
#freqColumns=[3,4,5,6,7,14,15,17] #car price
#activeColumns=[0,1,3,4,5] #student performance
#freqColumns=[2] #student performance
#activeColumns=[0,1,2,4] #50 Startups
#freqColumns=[3] #50 Startups
#activeColumns=[1,2,3,4,5,6] #fish
#freqColumns=[0] #fish
#activeColumns=[1,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21] #Life Expectancy
#freqColumns=[2] #Life Expectancy
#activeColumns=[0,1,2,3,4,5,6,7,8] #concrete
#freqColumns=[] #concrete
#activeColumns=[0,1,2,3] #Salary
#freqColumns=[] #Salary
#activeColumns=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] #housing
#freqColumns=[] #housing
#activeColumns=[1,2,3,4,5,6,7,8,10,11,12,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33] #cancer
#freqColumns=[] #cancer
#activeColumns=[1,2,3,4] #advertising
#freqColumns=[] #advertising
#activeColumns=[0,1,2,3,4,5] #wind
#freqColumns=[] #wind
#activeColumns=[0,5,6,7,8,9,10,11] #olympic
#freqColumns=[] #olympic
#activeColumns=[2,3,4,5,6,7,8,9] #mental health
#freqColumns=[] #mental health
#activeColumns=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30] #food
#freqColumns=[] #food
#activeColumns=[1,3,10,27,28,29,30] #music
#freqColumns=[31] #music
#activeColumns=[0,1,2,3,4,5,6] #engine
#freqColumns=[] #engine
#activeColumns=[1,3,4,5,6,7,8,9,10,11,12,13,14] #gun
#freqColumns=[] #gun
#activeColumns=[4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19] #deprivation
#freqColumns=[] #deprivation
#activeColumns=[3,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,32,33,34,35,36] #bank customers
#freqColumns=[4,5] #bank customers
#activeColumns=[3,4,5,6,7,8,9,10,11,12,13,14,15] #activity fitbit
#freqColumns=[2] #activity fitbit
#activeColumns=[1,4,5,6] #james bond
#freqColumns=[2] #james bond
activeColumns=[0,4,5,6,7,8,9]
freqColumns=[1,2,3]
limitLines=60000
minimumr=0.3
columnLabels=[]
#with open('gpa_study_hours.csv') as csv_file:
data=[]
counts=[]
counts2=[]
counts3=[]

arrayLimits=[]
#fileName="porsche_911.csv"
#fileName="tsla_split_adjusted.csv"
#fileName='titanic.csv'
#fileName='crimes.dataset.csv'
#fileName='fatal-police-shootings-data.csv'
#fileName='world-data-2023.csv'
#fileName='kaggle_income.csv'
#fileName='Final_32_region_deciles_1958-2015.csv'
#fileName='exercise-train.csv'
#fileName='exercise_dataset-2.csv'
#fileName='heart.csv'
#fileName='demographic.csv'
#fileName='CarPrice_Assignment.csv'
#fileName='Student_Performance.csv'
#fileName='50_Startups.csv'
#fileName='Fish.csv'
#fileName='Life Expectancy Data.csv'
#fileName='concrete_data.csv'
#fileName='Salary.csv'
#fileName='housinghuge.csv'
#fileName='cancer_reg.csv'
#fileName='Advertising.csv'
#fileName='wind_vs_price.csv'
#fileName='winter_olympic_study.csv'
#fileName='prevalence-by-mental-and-substance-use-disorder.csv' #mental health
#fileName='Food_Supply_Quantity_kg_Data.csv'
#fileName='mxmh_survey_results.csv'
#fileName='engine_data.csv'
#fileName='dataset_gun.csv'
#fileName='File_2_ID_2015_Domains_of_deprivation.csv'
#fileName='Bank_Customers.csv'
#fileName='Daily_Activity_2022_27_02.csv'
#fileName='jamesbond.csv'
fileName='diamonds.csv'
for column in range(0,len(activeColumns)):
    #print(f'len activeColumns={len(activeColumns)} Column={column}')
    #with open('gpa_iq.csv') as csv_file:
    #with open('diamonds.csv') as csv_file:
    #with open('world_university_rank.csv') as csv_file:
    #with open('smoking_driking_dataset_Ver01.csv') as csv_file:
    with open(fileName) as csv_file:
        csv_reader = csv.reader(csv_file, delimiter=',')
        line_count = 0
        
        a=[]
        #b=[]
        #c=[]
        #data=[]
        for row in csv_reader:
            if line_count == 0:
                #print(f'Column names are {", ".join(row)}')
                #print(row[0]," ",row[1]," ",row[2])
                if column==0:
                    for i in row:
                        #print(i)
                        columnLabels.append(i)
                line_count += 1
            else:
                #print(line_count, row[0])
                #print(row," ",column)
                #if (line_count<=3):
                #print(f'\t{row[1]} gpa, {row[2]} iq, {row[3]} gender')
                #a.append(float(row[activeColumns[column]]))
                a.append(toFloat(row[activeColumns[column]]))
                #target.append(row[calculateColumns[cc]])
                #b.append(float(row[2]))
                #c.append(float(row[3]))
                line_count += 1
                if (line_count>=limitLines):
                    break
    data.append(a)
    #data.append(b)
    #data.append(c)
#print(data)
# Specify the file name and mode (in this case, 'w' for write)
file_name = "outputFile.txt"

# Open the file in write mode
# This will create the file if it doesn't exist, or overwrite it if it does
with open(file_name, 'w') as file:
    # Write content to the file
    #file.write("This is some text written to a text file.\n")
    #file.write("You can write multiple lines like this.\n")

# The file is automatically closed when you exit the 'with' block

    for column in range(0,len(activeColumns)):
        pairColumn=column+1
        while (pairColumn<len(activeColumns)):
            corr, _ = pearsonr(data[column], data[pairColumn])
            if (abs(corr)>=minimumr):
                print(f'correlation between {columnLabels[activeColumns[column]]} and {columnLabels[activeColumns[pairColumn]]}')
                print('Pearsons correlation: %.3f' % corr)
                file.write(f'correlation between {columnLabels[activeColumns[column]]} and {columnLabels[activeColumns[pairColumn]]}\n')
                file.write('Pearsons correlation: %.3f \n' % corr)
            pairColumn+=1
        
    print(f'\nProcessed {line_count} lines.')
#print(columnLabels)
    data=[]
    for column in range(0,len(freqColumns)):
    #print(f'len activeColumns={len(activeColumns)} Column={column}')
    #with open('gpa_iq.csv') as csv_file:
    #with open('diamonds.csv') as csv_file:
    #with open('world_university_rank.csv') as csv_file:
    #with open('smoking_driking_dataset_Ver01.csv') as csv_file:
        with open(fileName) as csv_file:
            csv_reader = csv.reader(csv_file, delimiter=',')
            line_count = 0
        
            a=[]
        #b=[]
        #c=[]
        #data=[]
            for row in csv_reader:
                if line_count == 0:
                #print(f'Column names are {", ".join(row)}')
                #print(row[0]," ",row[1]," ",row[2])
                    if column==0:
                        for i in row:
                        #print(i)
                            columnLabels.append(i)
                    line_count += 1
                else:
                #if (line_count<=3):
                #print(f'\t{row[1]} gpa, {row[2]} iq, {row[3]} gender')
                #a.append(float(row[activeColumns[column]]))
                    a.append(row[freqColumns[column]])
                #target.append(row[calculateColumns[cc]])
                #b.append(float(row[2]))
                #c.append(float(row[3]))
                    line_count += 1
                    if (line_count>=limitLines):
                        break
        data.append(a)
    #data.append(b)
    #data.append(c)
#print(data)
    if (len(freqColumns) != 0):
        unique=generatePercentages()
    #print(unique)
    for j in range(0,len(unique)):
        print(f'\n{columnLabels[freqColumns[j]]}')
        file.write(f'\n{columnLabels[freqColumns[j]]}\n')
        #print(f'unique values={unique[j]}')
        for k in range(0,len(unique[j])):
            pc=counts3[j][k]*100.0/(line_count-1)
        #print('Pearsons correlation: %.3f' % corr)
        #print(f'{unique[j][k]} = {counts3[j][k]*100.0/(line_count-1)}')
            print(unique[j][k],'= %.3f'%pc,'%')
            file.write(f'{unique[j][k]} = %.3f'%pc)
            file.write('% \n')
