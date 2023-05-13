# awdaqwDFAEFSAEG
import pygame

pygame.init()

# set the dimensions of the game window
WINDOW_WIDTH = 700
WINDOW_HEIGHT = 840

# create the game window
game_window = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))

# set the title of the game window
pygame.display.set_caption('My Game')

# load the background image
background_image = pygame.image.load('another image.png')

# set the font and size of the text in the menu
menu_font = pygame.font.Font(None, 36)

# create the text for the menu items
start_text = menu_font.render('Start Game', True, (255, 255, 255))
quit_text = menu_font.render('Quit Game', True, (255, 255, 255))

# set the position of the menu items
start_pos = (WINDOW_WIDTH/2 - start_text.get_width()/2, 200)
quit_pos = (WINDOW_WIDTH/2 - quit_text.get_width()/2, 300)

# game loop
running = True
while running:
    # handle events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    
    # draw the background image
    game_window.blit(background_image, (0, 0))
    
    # draw the menu items
    game_window.blit(start_text, start_pos)
    game_window.blit(quit_text, quit_pos)
    
    # update the display
    pygame.display.update()

pygame.quit()

