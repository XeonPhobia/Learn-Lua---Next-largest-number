local function Iterator(a, lastNumber)
  b = 1
  if lastNumber == 0 then
    local n = 1
    local temporaryValue = ""
    while n <= #a do
      temporaryValue = temporaryValue .. a[n] 
      n = n + 1
    end
    table.insert(resultsArray, temporaryValue)   

  else
    for i=1,lastNumber do
      -- put the i-th element as the last one
      a[lastNumber], a[i] = a[i], a[lastNumber]

      --generate all permutations of the other elements
      Iterator(a,lastNumber-1)

      -- restore i-th element
      a[lastNumber], a[i] = a[i], a[lastNumber]
    end
  end
end

number = 234765

resultsArray = {}
arrayNumber = {}
for i=1, string.len(number) do
  arrayNumber[i] = string.sub(number,i,i)
end
Iterator(arrayNumber, string.len(number))

printableResultNumber = 1
i  =1; while resultsArray[i] do 
  if tonumber(resultsArray[i]) > number and tonumber(resultsArray[i]) < tonumber(resultsArray[printableResultNumber]) then 
    printableResultNumber = i 
  end
i = i + 1 end

print("Length of table resultsArray:", #resultsArray)
print("The Result is:", resultsArray[printableResultNumber])
