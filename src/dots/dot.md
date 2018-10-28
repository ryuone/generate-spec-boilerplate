<!-- textlint-disable -->
### Records
{% dot %}
digraph structs {
	node[shape=record]
	struct1 [label="<f0> left|<f1> mid\ dle|<f2> right"];
	struct2 [label="{<f0> one|<f1> two\n\n\n}" shape=Mrecord];
	struct3 [label="hello\nworld |{ b |{c|<here> d|e}| f}| g | h"];
	struct1:f1 -> struct2:f0;
	struct1:f0 -> struct3:f1;
}
{% enddot %}

### Finite State Machine
{% dot %}
digraph finite_state_machine {
	rankdir=LR;
	size="8,5"
	node [shape = circle];
	S0 -> S1 [ label = "Lift Nozzle" ]
	S1 -> S0 [ label = "Replace Nozzle" ]
	S1 -> S2 [ label = "Authorize Pump" ]
	S2 -> S0 [ label = "Replace Nozzle" ]
	S2 -> S3 [ label = "Pull Trigger" ]
	S3 -> S2 [ label = "Release Trigger" ]
}
{% enddot %}

### Data Flow Diagrams 2

{% dot %}
digraph dfd2{
        node[shape=record]
        subgraph level0{
        enti1 [label="Customer" shape=box];
        enti2 [label="Manager" shape=box];
        }
        subgraph cluster_level1{
                        label ="Level 1";
                        proc1 [label="{<f0> 1.0|<f1> One process here\n\n\n}" shape=Mrecord];
                        proc2 [label="{<f0> 2.0|<f1> Other process here\n\n\n}" shape=Mrecord];
                        store1 [label="<f0>    |<f1> Data store one"];
                        store2 [label="<f0>   |<f1> Data store two"];
			{rank=same; store1, store2}

        }
        enti1 -> proc1
        enti2 -> proc2
        store1 -> proc1
        store2 -> proc2
	proc1 -> store2
	store2 -> proc1 
}
{% enddot %}
<!-- textlint-enable -->
