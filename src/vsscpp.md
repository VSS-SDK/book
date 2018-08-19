# VSS-SampleCpp

```cpp
#include <StateReceiver.h>
#include <CommandSender.h>
#include <DebugSender.h>

using namespace vss;

int main(int argc, char** argv){
    IStateReceiver *stateReceiver = new StateReceiver();
    ICommandSender *commandSender = new CommandSender();
    IDebugSender *debugSender = new DebugSender();

    stateReceiver->createSocket();
    commandSender->createSocket(TeamType::Yellow);
    debugSender->createSocket(TeamType::Yellow);

    while(true){
        State state;
        Command command;
        Debug debug;
        
        state = stateReceiver->receiveState(FieldTransformationType::None);
        commandSender->sendCommand(command);
        debugSender->sendDebug(debug);
    }

    return 0;
}
```
