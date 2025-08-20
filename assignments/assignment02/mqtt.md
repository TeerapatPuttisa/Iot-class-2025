# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
[16:31:05] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [16:31:05] DEBUG | Received CONNACK (0, 0)
oak
Enter QoS level (0, 1, 2): 0
[16:31:11] DEBUG | Sending PUBLISH (d0, q0, r0, m1), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:11] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=1
Enter message to publish: [16:31:11] PUBLISHED | msgid=1
oak
Enter QoS level (0, 1, 2): 0
[16:31:20] DEBUG | Sending PUBLISH (d0, q0, r0, m2), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:20] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=2
Enter message to publish: [16:31:20] PUBLISHED | msgid=2
oak
Enter QoS level (0, 1, 2): 0
[16:31:59] DEBUG | Sending PUBLISH (d0, q0, r0, m3), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:59] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=3
[16:31:59] PUBLISHED | msgid=3
Enter message to publish: [16:32:05] DEBUG | Sending PINGREQ
```

## Subscriber_qos.py Output

```
[16:31:05] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [16:31:05] DEBUG | Received CONNACK (0, 0)
oak
Enter QoS level (0, 1, 2): 0
[16:31:11] DEBUG | Sending PUBLISH (d0, q0, r0, m1), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:11] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=1
Enter message to publish: [16:31:11] PUBLISHED | msgid=1
oak
Enter QoS level (0, 1, 2): 0
[16:31:20] DEBUG | Sending PUBLISH (d0, q0, r0, m2), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:20] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=2
Enter message to publish: [16:31:20] PUBLISHED | msgid=2
oak
Enter QoS level (0, 1, 2): 0
[16:31:59] DEBUG | Sending PUBLISH (d0, q0, r0, m3), 'b'test/qos/6510301035/temperature'', ... (3 bytes)
[16:31:59] PUBLISH REQUESTED | QoS=0 | Message='oak' | msgid=3
[16:31:59] PUBLISHED | msgid=3
Enter message to publish: [16:32:05] DEBUG | Sending PINGREQ
[16:32:05] DEBUG | Received PINGRESP
```