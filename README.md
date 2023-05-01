# Example-of-README.md
#Data mtcars

?mtcars
head(mtcars)
library(rpart)
library(rattle)
library(rpart.plot)
dat=mtcars[,1:11]
pmatrix=scale(dat)
d=dist(pmatrix)
#tree hclust
c=hclust(d,method="ward.D2")
plot(c)
#ξεχωρίζω σε τρείς μεγάλες ομάδες το δένδρο με τα data mtcars 
rect.hclust(c,k=3)
groups<-cutree(c,k=3)
