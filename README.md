import serial
s = serial.Serial(6)
ps = ''
ch = ''
count = 0
while (True):
    ch = s.read()
    if ch != '\r':
        ps = ps + ch
    else:
        print ps
        ps = ''
        count = count +1
        if count == 3:
            print '**************'
            count = 0

