# Types of ML Tasks

## Agent-Environment Interaction Model

```
┌─────────┐    Perception     ┌─────────────────┐
│         │ ◄──────────────── │                 │
│  Agent  │    Learning       │      Data       │
│         │                   │   Environment   │
│         │    Actions        │                 │
│         │ ──────────────────┤                 │
└─────────┘                   └─────────────────┘
```

## Environment Characteristics

The data environment can be characterized by several dimensions:

- **Observable/partially observable**
- **Single agent/multi-agent**
- **Stochastic or deterministic**
- **Episodic or sequential**
- **Discrete or continuous**

## Online/Off-line Learning

**Note:** In offline settings, the environment is replaced by static data.

## Learning Paradigms

| Type | Description |
|------|-------------|
| **Perception + Learning** | Agent receives data from environment and learns patterns |
| **Actions** | Agent can take actions that affect the environment |
| **Online Learning** | Learning occurs in real-time as agent interacts with environment |
| **Offline Learning** | Learning occurs from pre-collected static datasets |