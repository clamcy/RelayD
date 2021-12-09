# RelayD

Stratum relay with simple obfuscation written in C++ and Qt. 

This is a backup of my old project that hasn't been maintained since 2019.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

See the GNU General Public License for more details.

## Build

```bash
qmake
make
```

## Configuration

Configuration is done via env.


### Manual

```bash
export RELAYD_CONF = "Manual"
export RELAYD_LISTEN_PORT = "1000"
export RELAYD_FORWARD_ADDR = "www.google.com"
export RELAYD_FORWARD_PORT = "1001"
export RELAYD_XFER_MODE = "01" # or "10" or "11" or "00"
```

The program will output an `ALL_IN_ONE_CONF_STRING`.

### Lazy

```bash
export RELAYD_CONF = $(ALL_IN_ONE_CONF_STRING)
```

### Xfer Mode

- 00: input plain, output plain
- 01: input plain, output obfuscated
- 10: input obfuscated, output plain
- 11: input obfuscated, output obfuscated

