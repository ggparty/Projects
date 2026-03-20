import random
def deck():
    cards = []
    i = 0
    numbers = [1,1,2,2,3,3,4,4,5,5,6,6,7,7,8,8]
    random.shuffle(numbers)
    for row in range(4):
        cards.append([])
        for column in range(4):
                cards[row].append(numbers[i])
                i += 1
    return cards
            
def postion(cards):
    while True:
        position = input("Enter the row (1 to 4) and colunm (1 to 4): ")
        position = position.split()
        r = int(position[0]) - 1
        c = int(position[1]) - 1
        if not (0<=r<=3) or not (0<=c<=3):
            print("Invaild position.\n")
            continue
        else:
            card = cards[r][c]
            break
    return card, r, c

def setup(board):
    for row in range(0,len(board)):
        for column in range(0,len(board[row])):
            print(board[row][column], end= ' ')
        print()

def game(cards):
    board = []
    for row in range(4):
        board.append([])
        for column in range(4):
            board[row].append('*')
    while any('*' in row for row in board):
        pick =[]
        flipped = []
        setup(board)
        for i in range(2):
            while True:
                card, r, c = postion(cards)
                if board[r][c] != '*':
                    print("Card at this position already faced up. Select postition again.\n")
                    continue
                else:
                    break
            board[r][c] = card
            setup(board)
            flipped.append(card)
            pick.append(r)
            pick.append(c)
        if flipped[0] == flipped[1]:
            print("Pair match\n")
        else:
            print("Pair do not match select again!\n")
            board[pick[0]][pick[1]] = '*'
            board[pick[2]][pick[3]] = '*' 

            
        
def main():
    while True:
        cards = deck()
        game(cards)
        Idk = input("Enter any key to continue....\n")

main()
