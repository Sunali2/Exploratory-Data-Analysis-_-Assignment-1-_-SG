# Exploratory-Data-Analysis-_-Assignment-1-_-SG
# The R code used for Plots 1-4 are given below.
# R Code for Data Download
> library(readxl)
> PowerData <- read_excel("C:/Users/sunal/OneDrive/Documents/datasciencecoursera/NewSG/household_power_consumption/household_power_consumption2.xlsx")
# R Code for Plot1
> png(filename="Plot1", width = 480, height=480, units ="px”)
> hist(PowerData$Global_active_power, col="red", xlab="Global Active Power (kilowatts)", ylab="Frequency", main="Global Active Power")
> dev.off
# Plot1
<img width="229" height="275" alt="Plot1" src="https://github.com/user-attachments/assets/94583d0d-3e34-496f-a824-959be4a9c6ca" />
# R Code for Plot2
> png(filename="Plot2", width = 480, height=480, units ="px”)
> x <- PowerData$Time
> y <-PowerData$Global_active_power
> x_range <- range(PowerData$Time)
> y_range <- range(PowerData$Global_active_power)
> plot(x, y, type="l", ylab="Global_active_power (kwatts)", xlim=x_range, xlab="time", ylim=y_range, main="Global Active Power")
> dev.off
# Plot2
<img width="229" height="275" alt="Plot2" src="https://github.com/user-attachments/assets/1a5c6673-9da4-4432-8ab0-424c05a796dd" />

# R Code for Plot3
> png(filename="Plot2", width = 480, height=480, units ="px”)
> x <- PowerData$Time
> y2 <-PowerData$Sub_metering_1
> y3 <-PowerData$Sub_metering_2
> y4 <-PowerData$Sub_metering_3
> x_range <- range(x)
> y2_range <- range(y2)
> y3_range <- range(y3)
> y4_range <- range(y4)
> plot(x, y2, type="l", ylim=y2_range, ylab="Energy Sub Metering", xlim=x_range, xlab="time", main="Sub Metering")
> lines(x, y3, col="red")
> lines(x, y4, col="blue")
> dev.off
#Plot3
<img width="229" height="275" alt="Plot3" src="https://github.com/user-attachments/assets/04ffc25d-c0a6-4afd-90ab-f48df06b6e9f" />
 
# R Code for Plot4
> png(filename="Plot4", width = 480, height=480, units ="px”)
> par(mfrow=c(2,2), mar=c(4,4,2,2))
> x <- PowerData$Time
> x_range <- range(x)
> y <-PowerData$Global_active_power
> y_range <- range(y)
> plot(x, y, type="l", ylim=y_range, ylab="Voltage", xlim=x_range, xlab="time", main="Global Active Power")
> y1 <- PowerData$Voltage
> y1_range <- range(y1)
> plot(x, y1, type="l", ylim=y1_range, ylab="Voltage", xlim=x_range, xlab="time", main="Voltage")
> y2 <- PowerData$Sub_metering_1
> y3 <- PowerData$Sub_metering_2
> y4 <- PowerData$Sub_metering_3
> y2_range <- range(y2)
> y3_range <- range(y3)
> y4_range <- range(y4)
> plot(x, y2, type="l", ylim=y2_range, ylab="Energy Sub Metering", xlim=x_range, xlab="time", main="Sub Metering")
> lines(x, y3, col="red")
> lines(x, y4, col="blue")
> y5 <- PowerData$Global_reactive_power
> y5_range <- range(y5)
> plot(x, y5, type="l", ylim=y5_range, ylab="Global reactive energy", xlim=x_range, xlab="time", main="Global reactive energy")
> dev.off
> <img width="450" height="610" alt="Plot4" src="https://github.com/user-attachments/assets/53ddcd48-16f5-4424-b465-4bc80851ee67" />

