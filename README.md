# Function2
def calculate_batting_average(hits, at_bats):
    if at_bats == 0:
        return 0.0
    else:
        return hits / at_bats

def main():
    player_count = 0

    try:
        while True:
            # User input for player information
            last_name = input("Enter player's last name (Ctrl+Z to stop): ")
            hits = int(input("Enter number of hits: "))
            at_bats = int(input("Enter number of at-bats: "))

            # Calculate batting average
            batting_average = calculate_batting_average(hits, at_bats)

            # Display last name and batting average
            print(f"{last_name}'s Batting Average: {batting_average:.3f}")

            # Increment player count
            player_count += 1

    except EOFError:
        # Display the number of players entered
        print(f"\nNumber of Players Entered: {player_count}")

if __name__ == "__main__":
    main()
