# Exemplos

 Exemplos de estratégias que obtém estados do VSS-Vision e VSS-Simulator, enviam comandos para 
 o VSS-Simulator e enviam informações de debug para o VSS-Viewer. 
 
## C++
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

## Rust
```cpp
extern crate vss_core_rust;

use vss_core_rust::communications::command_sender::CommandSender;
use vss_core_rust::domain::team_type::TeamType;
use vss_core_rust::domain::command::Command;
use vss_core_rust::domain::wheels_command::WheelsCommand;

fn main() {
    let mut command_sender = CommandSender::new();
    command_sender.create_socket(TeamType::Yellow);
   
    loop {
        let command = Command::new();
        command_sender.send_command(command);
    }
}
```