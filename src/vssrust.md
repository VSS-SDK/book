# VSS-SampleRust

```rust
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