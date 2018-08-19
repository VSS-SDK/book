# Modelos de comunicação

Domain/State.h
```cpp
namespace vss {
    class State {
    public:
        State();
        State(Ball ball, std::vector<Robot> teamBlue, std::vector<Robot> teamYellow);

        friend std::ostream& operator<<(std::ostream& os, const State& state);

        Ball ball;
        std::vector<Robot> teamBlue;
        std::vector<Robot> teamYellow;
    };
}
```

Domain/Command.h
```cpp
namespace vss {
    class Command {
    public:
        Command();
        Command(int id, std::vector<WheelsCommand> commands);

        friend std::ostream& operator<<(std::ostream& os, const Command& command);

        int id;
        std::vector<WheelsCommand> commands;
    };
}
```

Domain/Debug.h
```cpp
namespace vss {
    class Debug {
    public:
        Debug();
        Debug(std::vector<Point> stepPoints, std::vector<Pose> finalPoses, std::vector<Path> paths);

        friend std::ostream& operator<<(std::ostream& os, const Debug& debug);

        std::vector<Point> stepPoints;
        std::vector<Pose> finalPoses;
        std::vector<Path> paths;
    };
}
```

Domain/Control.h
```cpp
namespace vss {
    class Control {
    public:
        Control();
        Control(bool paused, Ball ball, std::vector<Robot> teamYellow, std::vector<Robot> teamBlue);

        friend std::ostream& operator<<(std::ostream& os, const Control& control);

        bool paused;
        Ball ball;
        std::vector<Robot> teamYellow;
        std::vector<Robot> teamBlue;
    };
}
```