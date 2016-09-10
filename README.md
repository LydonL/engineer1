# engineer1
first e of my study
#Ball Control Game
import simplegui
width=600
height=400
ball_radius=20
ball_pos=[width/2,height/2]
def draw(canvas):
    canvas.draw_circle(ball_pos,ball_radius,20,"Red")
def keydown(key):
    vel=5 #rate  
    if key==simplegui.KEY_MAP["left"] and ball_pos[0]>20:
        ball_pos[0]-=vel
    elif key==simplegui.KEY_MAP["right"] and ball_pos[0]>20:
        ball_pos[0]+=vel
    elif key==simplegui.KEY_MAP["down"] and ball_pos[1]>20:
        ball_pos[1]+=vel
    elif key==simplegui.KEY_MAP["up"] and ball_pos[1]>20:
        ball_pos[1]-=vel
frame=simplegui.create_frame("Pos Ball Control",width,height)
frame.set_draw_handler(draw)
frame.set_keydown_handler(keydown)
frame.start()
