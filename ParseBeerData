str = "Kentucky Brunch Brand StoutToppling Goliath Brewing CompanyAmerican Double / Imperial Stout / 12.00% ABV"


#create empty dict of beerinfo
beerinfo = {
    "Name": [],
    "Brewery" : [],
    "Type" : [],
    "Type2" : [],
    "ABV" : [],
}
#create empty array to hold indicies of "delim" where a lowercase character is right before an Uppercase character
delim = []

#iterate through string to find cases where lower meets uppercase, append to delim array
for i in range(1,len(str)-1):
    if(str[i].islower() and str[i+1].isupper()):
        delim.append(i)
    else:
        continue
#assign string[0:delim1] to "Name", delim1:delim2 to "Brewery" etc       
beerinfo["Name"] = str[0:delim[0]+1]
beerinfo["Brewery"] =str[(delim[0]+1):delim[1]+1]
beerinfo["Description"] =str[delim[1]+1:(len(str))]       

#split Description into types and descriptions
slash = "/"
typestart = str.find(slash)
beerinfo["Type"] = str[delim[1]+1:typestart-1]

#check for multiple descriptions and split 
if str.count("/") >= 2:
    typestart2 = (str[typestart + 1:len(str)].find(slash)) + typestart
    beerinfo["Type2"] = str[typestart+2:typestart2]


#find "%" to locate are of ABV, then strip whitespace and assign to beerinfo["ABV"]
abvloc = str.find("%")
beerinfo["ABV"] = str[abvloc-5:abvloc].strip()
