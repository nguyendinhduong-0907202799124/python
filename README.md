class Player:
    def __init__(self,name:str,endurance:int,sprint:int,dribble:int,passing:int,shooting:int):
        self.name=name
        self.endurance=endurance
        self.sprint=sprint
        self.dribble=dribble
        self.passing=passing
        self.shooting=shooting
    def __str__(self):
        return print('Player',self.name,'Endurance',self.endurance,'Sprint',self.sprint,'Dribble',self.dribble,'Passing',self.passing,'Shooting',self.shooting)

class Team:
    def __init__(self,name:str,rating:int):
        self.name=name
        self.rating=rating
    def players(self):
        return self.__players
    def players(self, players: list):
        self.__players = players
    def add_player(self,player:int):
        if player in self.__players:
            return f"Player {player.name} has already joined"
        self.__players.append(player)
        return f"Player {player.name} joined team {self.name}"
    def remove_player(self, player_name: str):
        for player in self.players:
            if player.name == player_name:
                self.players.remove(player)
                return player
        return f"Player {player_name} not found"
