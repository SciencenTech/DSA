# DSA

getwd()	
d=read.csv2(".csv")
dim(d)
nrow(d)
head(d)

c is combine
d is orginal dataset



Subset
subset1<-d[c('x','y','z')]
write.csv(subset1,"name of file.csv")
sub1=subset(subset1,x>50)


Merge 
dataA=read.csv2(".csv")
dataB=read.csv2(".csv")
NewAB=rbind(dataA,dataB)

Sort
x=sub[order(-d$colname),] //"-" is for descending,dont apply - for ascending

Transpose
tran=t(subset1)

Melting
melt(data=subset1,id.vars="colname")
sudo apt-get install r-cran-plyr
library(reshape)//for melting,casting
melt(data = subset1,id.vars = "x")

casting
library(reshape)
sub=d[c('X.a','X.b')]
cast(sub,X.a ~ X.b,mean,value = 'Paid')

PieChart
runs=c(21,45,98,11)
players=c("A","B","C","D")
png(file="scorecard.png")
pie(runs,players)
dev.off()	//to save

barplot(runs)	//for bargraph


head(name)
input=mtcars[,c('mpg','cyl')]
print(head(input))
png(file="boxplot.png")
boxplot(mpg~cyl,data = mtcars,xlab="No. of cylinders",ylab="Miles per gallons",main="MileageDta")
dev.off()


DataCleaning
mean(airquality$Ozone)
mean(airquality$Ozone,na.rm = TRUE)
max(airquality$Solar.R)
max(airquality$Solar.R,na.rm = TRUE )
summary(airquality)
air = airquality
air$Ozone=ifelse(is.na(air$Ozone),median(air$Ozone,na.rm = TRUE,air$Ozone))
summarry(air)

ErrorCorrection

air$Solar.R=ifelse(is.na(air$Solar.R),median(air$Solar.R,na.rm =TRUE),air$Solar.R)
summary(air)

Data Transformation
air$Solar.X=air$Solar.R>100			X named column created where >100 values are inserted
head(air)

brks=c(0,50,100,150,200,250,300,350)
air$Solar.R=cut(air,break = brks,include.lowestc= TRUE)  //For Range
# DSA
