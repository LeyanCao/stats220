# My Index Page
***
## *Meme that I created using R code*
![My meme](my_meme.png "My meme")


***
## *R code I used to create this meme*
```r
library(magick)

morning <- image_annotate(image_scale(image_read("ass1pic/1.jpg"), 400),
                          text = "Morning",color = "#FFFFFF",size = 55, font = "Comic Sans",gravity = "Northwest")

midday <- image_annotate(image_scale(image_read("ass1pic/2.jpg"), 400),
                         text = "Midday",color = "#FFFFFF",size = 55, font = "Comic Sans",gravity = "Northwest")

afternoon <- image_annotate(image_scale(image_read("ass1pic/3.jpg"), 400),
                            text = "Afternoon",color = "#FFFFFF",size = 55, font = "Comic Sans",gravity = "Northwest")

evening <- image_annotate(image_scale(image_read("ass1pic/4.jpg"), 400),
                          text = "Evening",color = "#FFFFFF",size = 55, font = "Comic Sans",gravity = "Northwest")

morning_text <- image_blank(width = 400, 
                          height = 300, 
                          color = "#000000") %>%
  image_annotate(text = "Just a wheat\ncracker is enough",
                color = "#FFFFFF",
                size = 50,
                font = "Impact",
                gravity = "center")

midday_text <- image_blank(width = 400, 
                            height = 300, 
                            color = "#FFFFFF") %>%
  image_annotate(text = "Just a few bites of\nsalad, I can do it",
                color = "#000000",
                size = 50,
                font = "Impact",
                gravity = "center")

afternoon_text <- image_blank(width = 400, 
                               height = 300, 
                               color = "#000000") %>%
  image_annotate(text = "You eat, I just\ndrink water",
                color = "#FFFFFF",
                size = 50,
                font = "Impact",
                gravity = "center")

evening_text <- image_blank(width = 400, 
                             height = 300, 
                             color = "#FFFFFF") %>%
  image_annotate(text = "I haven't eaten\nfor a day, I'm\nso hungry",
                 color = "#000000",
                 size = 50,
                 font = "Impact",
                 gravity = "center")

header <- image_blank(width = 800, 
                       height = 200, 
                       color = "#FFFFFF") %>%
  image_annotate(text = "Me trying to lose weight",
                color = "#000000",
                size = 80,
                font = "Impact",
                gravity = "center")

first_row <- c(morning, morning_text) %>%
  image_append()

second_row <- c(midday, midday_text) %>%
  image_append()

third_row <- c(afternoon, afternoon_text) %>%
  image_append()

fourth_row <- c(evening, evening_text) %>%
  image_append()

meme <- c(header, first_row, second_row, third_row, fourth_row) %>%
  image_append(stack = TRUE)

image_write(meme, "ass1pic/my_meme.png")
```

***
## *Reasons why I made this meme*
1. I love The Simpsons.
2. I want to satirize my previous weight loss experience. I saw a similar picture on the Internet before, and it explained very well why my previous attempts to weight loss    failed, so I decided to make a similar meme of it.

