```bash

chart {
    input {
        cpu [
            {
                bytes
            },
            {
                bytes
            },
            {
                bytes
            }
        ],
        random [
            {
                bytes
            }
        ]
    }
    output {

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