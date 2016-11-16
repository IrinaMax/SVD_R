# SVD_R Sigular Value Decomposition
# for Expedia destination set 
# loading data
     dest <- read.csv("~/Desktop/Expedia/destinations.csv", header = T, sep=",", stringsAsFactors = F)

#To represent SVD i will took little random sample for easy emplementation
     set.seed(12345678)
     mysam1  <- dest

# SVD
     svd1<-svd(mysam1[,-5])

     u<-as.matrix(svd1$u[,1:2])
     v<-as.matrix(svd1$v[,1:2])
     d<-as.matrix(diag(svd1$d)[1:2, 1:2])

     s2<-u%*%d%*%t(v)
     s2
     plot(s2) 
 #SVD_plot_Expedia_.png    
![svd_plot_expedia_](https://cloud.githubusercontent.com/assets/16123495/20338498/4f47b11a-ab8c-11e6-8228-856dd47f753b.png)

