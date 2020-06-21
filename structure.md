```bash

chart {
    input {
        cpu [
            {
                records
                bytes
            },
            {   
                records
                bytes
            },
            {
                records
                bytes
            }
        ],
        random [
            {   
                records
                bytes
            }
        ]
    }
    parser {
        xyz {
            "add_records": 
            "drop_records": 
        }
    }
    output {
        stdout [
            {
                "proc_records": 0,
                "proc_bytes": 0,
                "errors": 0,
                "retries": 0,
                "retries_failed": 0   
            }
        ]

    }
}

const x = {
    input: {}
    output: {}
}
const i =response.data.input;
i - keys // [cpu.1, cpu.2, random]
Object.keys(i).forEach( k => {
    // random
    let key = k.split(".");
    if (x.input[key[0]]) {
        x.input[key[0]].push(i[k])
    } else {
        x.input[key[0]] = [i[k]]
        // 1. x.ipnut.cpu = [{bytes:}, {bytes:}]
        // x.input.randaom = [{asdasda}]
    }
})


response.data {
    input {
        cpu.1{

        }
        cpu.2 {

        }
        random {}
    }
}

```

Objects

