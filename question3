"""
Read two integers n and m then a maze of size n by m from the input. Then a move will be given. Check if you hit the wall after making the given move. 
If you hit the wall, output Oops... I hit the wall! otherwise Lucky move!.

Maze is composed of the following characters and there is no space between the characters:

S - starting position
# - walls
. - empty spots
The move can be:

u - up
d - down
l - left
r - right
The size of the maze will not be more than 100 by 100.
"""

def find_start(maze, n, m):
    for i in range(n):
        for j in range(m):
            if maze[i][j] == 'S':
                return i, j

n, m = map(int, input().split())
maze = [input().strip() for _ in range(n)]
move = input().strip()

start_x, start_y = find_start(maze, n, m)

if move == 'u':
    new_x, new_y = start_x - 1, start_y
elif move == 'd':
    new_x, new_y = start_x + 1, start_y
elif move == 'l':
    new_x, new_y = start_x, start_y - 1
elif move == 'r':
    new_x, new_y = start_x, start_y + 1
else:
    print("Invalid move input")
    exit()

if 0 <= new_x < n and 0 <= new_y < m and maze[new_x][new_y] != '#':
    print("Lucky move!")
else:
    print("Oops... I hit the wall!")
