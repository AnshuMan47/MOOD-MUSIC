import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class MusicPlayer {
    private Map<String, String> musicMap;

    public MusicPlayer() {
        musicMap = new HashMap<>();
        musicMap.put("happy", "Happy.mp3");
        musicMap.put("sad", "Sad.mp3");
        musicMap.put("energetic", "Energetic.mp3");
        // Add more moods and corresponding music files as needed
    }

    public void playMusic(String mood) {
        String musicFile = musicMap.get(mood);
        if (musicFile != null) {
            System.out.println("Playing " + musicFile);
            // Add code to play the music file here
        } else {
            System.out.println("No music found for mood: " + mood);
        }
    }

    public static void main(String[] args) {
        MusicPlayer musicPlayer = new MusicPlayer();
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.print("Enter your mood (happy, sad, energetic, etc.): ");
            String mood = scanner.nextLine();
            musicPlayer.playMusic(mood);
        }
    }
}
