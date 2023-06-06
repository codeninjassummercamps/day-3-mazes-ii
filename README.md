# Day 3 Mazes II

```template
let going = 0
player.onChat("maze", function () {
    agent.teleport(world(-7, 0, -3), NORTH)
})
```

## Mazes II

Listen to Sensei to learn how to write code that will allow the agent to navigate the spiral maze.

## Finished Code

Good job listening to Sensei, you can check your code with the hint. Now try the bonus!

```blocks
let going = 0
player.onChat("maze", function () {
    agent.teleport(world(-7, 0, -3), NORTH)
    going = 1
})
loops.forever(function(){
    if(going == 1){
        if(agent.detect(AgentDetection.Block, FORWARD)){
            agent.turn(TurnDirection.Right)
        }else{
            agent.move(FORWARD, 1)
        }
    }
})
```

## Bonus

The agent can get into the maze and get to the center, but what happens in the center? First, try making a way to stop the agent from moving using a chat command. Once you've tried that, what can you do to teach the agent to get back out of the maze? This is a really tricky challenge, but if there is time, your Senseis can show you how to do it!

```blocks
player.onChat("stop", function () {
    going = 0
})
```

## Activity Complete!

You did it! You explored new conditionals and learned about the ``||logic.else||`` part of a conditional! 
