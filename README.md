# Prediction-using-unsuprevided-ml
> library(ggplot2)
> df1<-iris
> head(iris)
> summary(iris)
> g<-ggplot(df1, aes(Petal.Length, Petal.Width)) + geom_point(aes(col=Species))
> print(g)
> set.seed(132)
> irisCluster1 <-kmeans(df1[,1:4], center=3, nstart=20)
> irisCluster1
> table(irisCluster1$cluster, df1$Species)
> library(cluster)
> clusplot(iris, irisCluster1$cluster, color=T, shade=T, labels=0, lines=0)
>  
