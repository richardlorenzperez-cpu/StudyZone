Scenario: Many students today find it hard to concentrate, especially when studying online. Things like social media, online/offline games, and notifications can easily break their focus. StudyZone helps by giving students a timer to manage study time, relaxing sounds to stay calm, and motivational quotes to keep them inspired while studying.

Initial Scope / Core Features: 
1. Focus Timer – Keeps track of study and break time automatically. 
2. Calming Sounds – Plays relaxing background music while studying. 
3. Motivational Messages – Shows encouraging quotes during study time. 
4. Progress Tracker – Records total study time and number of completed sessions. 
5. User Profiles – Saves each student’s personal progress and details.

https://www.figma.com/board/DPqwXKmPACwsFHcpAr0yKP/Untitled?node-id=0-1&t=sHSVcSsSdXRFnRuv-1

class MotivationalQuote {
    String text;
    String author;

    public MotivationalQuote(String text, String author) {
        this.text = text;
        this.author = author;
    }

    public void display() {
        System.out.println("\"" + text + "\" — " + author);
    }
}

class Sound {
    String name;
    String filePath;

    public Sound(String name, String filePath) {
        this.name = name;
        this.filePath = filePath;
    }

    public void play() {
        System.out.println("Playing sound: " + name);
    }

    public void stop() {
        System.out.println("Stopped sound: " + name);
    }
}

class SoundManager {
    Sound currentSound;

    public void playSound(Sound sound) {
        currentSound = sound;
        sound.play();
    }

    public void stopSound() {
        if (currentSound != null) {
            currentSound.stop();
        }
    }
}

class StudyTimer {
    int duration;
    int remainingTime;
    boolean isRunning;

    public StudyTimer(int duration) {
        this.duration = duration;
        this.remainingTime = duration * 60;
    }

    public void start() {
        isRunning = true;
        System.out.println("Study Timer Started: " + duration + " minutes");
    }

    public void pause() {
        isRunning = false;
        System.out.println("Timer Paused.");
    }

    public void reset() {
        remainingTime = duration * 60;
        isRunning = false;
        System.out.println("Timer Reset.");
    }
}

class StudyZone {

    public void startStudySession(StudyTimer timer, SoundManager soundManager, Sound sound, MotivationalQuote quote) {
        System.out.println("\n=== STUDY SESSION STARTED ===");
        System.out.println("Student Name: Lorenz");
        timer.start();
        soundManager.playSound(sound);
        quote.display();

    }

    public void startBreak() {
        System.out.println("\nBreak time. Relax for a while.");
    }

    public void stopTimers(StudyTimer timer, SoundManager soundManager) {
        timer.pause();
        soundManager.stopSound();
        System.out.println("All timers and sounds stopped.");
    }
}

public class Main {
    public static void main(String[] args) {

        

        StudyTimer timer = new StudyTimer(25);

        Sound studyMusic = new Sound("Dive by Ellie Banke", "study.mp3");
        SoundManager soundManager = new SoundManager();

        MotivationalQuote quote = new MotivationalQuote(
                "Stay focused. Stay determined.", "StudyZone"
        );

        StudyZone app = new StudyZone();

        app.startStudySession(timer, soundManager, studyMusic, quote);

        app.startBreak();

        app.stopTimers(timer, soundManager);
    }
}
