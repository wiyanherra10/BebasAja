def drawXYZ(height):
    for i in range(1, height+1):
        if i % 3 == 0:
            print("X", end="")
        else:
            for j in range(1, i+1):
                if j % 2 == 1:
                    print("Y", end="")
                elif j % 2 == 0:
                    print("Z", end="")
        print()
