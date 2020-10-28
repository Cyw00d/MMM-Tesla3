# MMM-Tesla3
I needed a better Tesla module for the mirror, I know there is a version 1 (MMM-Tesla Not working and last updated 3 yrs ago) and version 2 (MMM-Tesla2 No car-wake and you need to manually find the VIN for config).

## Installation
```bash
cd ~/MagicMirror/modules
```

```bash
git clone https://github.com/Cyw00d/MMM-Tesla3.git
```

```bash
cd MMM-Tesla3 && npm install
```

## Configuration
Copy the example config to your MagicMirror config file:

```javascript

{
  module: 'MMM-Tesla3',
  position: 'bottom_left',	// This can be any of the regions.
  config: {
    email: 'elonmusk@tesla.com',
    password: 'B3tterTh4nG4zz',
    region: 'EU',
    client_id: '81527cff06843c8634fdc09e8ac0abefb46ac849f38fe1e431c2ef2106796384',
    client_secret:  'c7257eb71a564034f9419ee651c7d0e5f7aa6bfbd18bafb5c5c033b093bb2fa3',
    refreshIntervalWhileCharging:  1000 * 60 * 2, // 1000 = 1s || * 60 = 1 minute * 10 = 10 minutes
    wakeOnModuleLoad: true,
    wakeOnRefresh: false,
  }
},
```
| key  | Required | Description | Default |
| - | - | - | - |
| email | yes | Your Tesla login email |  | 
| password | yes | Your Tesla login password |  |
| client_id | yes | You can get it from the config example above, Tesla needs this to authenticate  | |
| client_secret| yes | You can get it from the config example above, Tesla needs this to authenticate | |
| refreshInterval | no | When should the data be refreshed when not charging? | `1000 * 60 * 60` (60 minutes) |
| refreshIntervalWhileCharging | no | When should the data be refreshed when the car is charging? | `1000 * 60 * 10` (10 minutes) |
| wakeOnModuleLoad | no | When true, on initial module load the car will be woken up when in sleep mode to get the latest data | `false` |
| wakeOnRefresh | no | When set to true, the car will be woken up every time the module refreshes his data (see refreshInterval) | `false` |
| showLastUpdated | no | Show 'Updated 4 minutes ago' at the bottom | `true` |

## Preview
![Tesla example](/preview.jpg)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
