Practical 2:-

Q3) Create the matrics and perform ooperations
A<-matrix(c(1,2,3,2,0,1,3,-1,5),nrow=3,ncol=3)
print(A)
B<-matrix(c(2,-1,7,4,1,2,1,2,9), nrow=3,ncol=3)
print(B)
#Addition
print(A+B)
#Subtraction
print(A-B)
#Multiplication
print (A%*%B)
#Determinant
print(det (A))
print(det (B))
#Transpose
print(t(A))
print(t(B))
Q4)Createthe matrix using names:
A<-matrix(c(35,25,33,27), nrow=2,ncol=2)
dimnames (A) <- list(c("FYCS-1", "FYCS-2"), C("BOYS", "GIRLS"))
print(A)
Q5)Create the following dataset
Roll<-c(9001,9002,9003,9004,9006,9007,9009,9010)
gpa-c(6.9,0,9.3,0,0,0,8,7.8)
grade<-c("B", "F", "A+", "F","F","F","A", "B+")
x-data.frame(roll,gpa, grade)
print(x)

Practical 3:-
Q)claculate mean, median,mode of the given data set
cat("\014")
print('Data Set: 34,47,1,1,57,24,34,19,19,50,28,1,34')
A<-c(34,47,1,1,57,24,34,19,19,50,28,1,34)
x<-mean(A)
print('Mean=')
print(x)
#median
x-median(A)
print('Median-')
print(x)
#mode
B<-table(A)
x<-names (B)
x<-as.numeric(x)
y<-as.numeric(B)
z<-rbind(x,y)
max_val<-max(y)
#print(z)
d<-dim(z)
print('Mode: ')
for (i in 1:d[2]) {
if(z[2,i]==max_val)
print(paste(z[1,i]))
}
#range
x<-range (A)
print('Range: ')
print(x)
#quartiles
q<-quantile (A)
print('Quantiles of A: ')
print(q)
#interquartile range
i<-IQR(A)
print('Interquartile Range of A =')
print(i)
#Histogram of A
hist (A)

Practical 4:-

Q)TO execute statistical functions on the data imported from .CSV file
cat("\014")
data<-read.csv("result.csv")
print('..............................');
print(data)
print('.............................................');
p<-data$Physics
c<-data$Chemistry
m<-data$Maths
d<-data$Biology
mp<-mean (p)
print(paste('Mean of Physics marks:',mp))
mdc<-median(c)
print(paste("Median of Chemistry marks:",mdc))
#Mode of Biology sarks
B<-table(b)
x<-names (B)
x<-as.numeric(x)
y<-as.numeric(B)
z<-rbind(x,y)
max_val<-max(y)
d<-dia(z)
print('Mode of Biology marks: ')
for ( i in 1:d[2]){
if(z[2,i] ==max_val)
print(paste (z[1,i]))
}
print('Quartiles of Physics marks :')
qp<-quantile(p)
print(qp)
print('Range of Maths marks :')
rm<-range(m)
print(rm)
iqrc<-IQR(c)
print(paste('Interquartile range of Chemistry marks: ', iqrc))
Biology_Marks=b
hist (Biology_Marks)

Practical 5:-
cat("\014")
x<-c(rep(6.2), rep (10,3), rep (12,4), rep (14,5), rep(24,4))
print("Data Set: ")
print(x)
#Standard Deviation
nr<-sum((x-mean(x))^2)
dr<-(length(x)-1)
sd_x<-sqrt(nr/dr)
print(paste("Standard Deviation of the given data set is: ",round((sd_x),4)))
print("-..................");
#Variance
nr<-sum((x-mean(x))^2)
dr<-(length(x)-1)
var_x<-nr/dr
print(paste("Variance of the given data set is: ",round((var_x),4)))
print("........................")
#Covariance
x<-c(2,8,18,20,28,30)
y<-c(5,12,18,23,45,50)
print("x")
print(x)
print("y")
print(y)
cov_xy<-sum((x-mean(x))*(y-mean(y)))/(length(x)-1) 
print(paste("Covariance of the given data set is", round((cov_xy),4)))
data<-read.csv("result.csv")
print('........................');
print(data)
print('.....................');
q1<-data$QUIZ1
q2<-data$QUIZ2
sdc<-sd(q1) 
print (paste('standard deviation of Quiz-I marks', round(sdc,4)))
sdc<-sd(q2)
print (paste('Standard Deviation of Quiz-2 marks', round(sdc,4)))
var_a<-var (q1)
print (paste("Variance of Quiz1 marks:", round (var_a, 4)))
var_b<-var (q2)
print (paste("Variance of Quiz2 marks: ", round (var_b,4)))
covpm<-cov(q1,q2) 
print (paste("Covariance of Quiz-1 and Quiz-2 marks:", round(covpm,4)))


Practical 6:-
Q)Calculate skewness of the data imported from thhe .CSV file
library(e1071)
cat('\014')
data<-read.csv("skewdata.csv")
print('--................');
print(data)
print('.....................')
x<-data$Class_Mark
f<-data$Frequency
x<- c(rep (x,f))
sk<-skewness (x)
sk<-round(sk,4)
print(paste("Skewness=",sk))


Practical 7:-
Q1)Chi  squared method
cat ('\014')
data<-read.csv('chi.csv')
print('Chi Squared Test')
print('-------')
print(data)
print(".............................")
x<-data$Observed_Frequency
a<-chisq.test(x)
print(a)
Q2)Yates correction table
cat('\014')
data<-read.csv('chi_yt.csv')
print('Contigency Table')
print('--................')
print(data)
print('---------')
cl<-data Recover
c2<-data$Do_Not_Recover
m<-as.table (cbind(c1.c2))
print('without Yates Correction :')
x<-chisq.test(m,correct=FALSE)
print(x)
print('...............')
print('with Yates Correction :')
x<-chisq.test(m)
print(x)


Practical 8:-
cat('\014')
print('Example 1 : Binomial Distribution')
print('n=6, p=0.5 , P[X=2]=?')
n=6
D=0.5
x=2
ans=dbinom(x,n,p)
print(paste ("P[X=2]=", round(ans,4)))
print('-...................');
print('Example 2 : Binomial Distribution')
print c("n=6 p=0.5 , P[X>=4]=? ")
n=6
D=0.5
x=3
ans=1-pbinom(x,n,p)
print (paste('P[X>=4]=', round(ans,4)))
print('....................');
print('Example 3 : Binomial Distribution')
print "n=5 p=0.4 , P[X<=2]=? ')
n=5
D=0.4
x=2
ans=pbinom(x,n,p)
print(paste('P[X>=4]=', round(ans,4)))
print('-............... ')
print('Example 4 : Normal Distribution')
print c("mu=20.5. sigma-5.5, P[X<25]=?")
ans=pnorm(25,mean=20.5,sd=5.5)
print(paste('P[X<25]=', round(ans,4)))
print("mu=20.5, sigma=5.5, P[X>30]=? ")
ans=1-pnorm(30,mean=20.5,sd=5.5)
print(paste("P[X<25]=", round(ans,4)))
