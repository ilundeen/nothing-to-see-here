library(curl)
f <- read.csv(curl("https://raw.githubusercontent.com/ilundeen/nothing-to-see-here/master/just.nothing.at.all.csv"), header=TRUE)
library(ggplot2)

p<-ggplot(f, aes(x=x, y=y))+ 
  geom_point(aes(color=f$X, size=3))+
          theme_classic()+
  theme(legend.position="none")
p
p<-p + theme(
  axis.text.x = element_blank(),
  axis.text.y = element_blank(),
  axis.ticks = element_blank())+
  scale_x_discrete(name =" ")+
  scale_y_discrete(name=" ")
p
