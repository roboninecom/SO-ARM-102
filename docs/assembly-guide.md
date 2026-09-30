# Assembly guide

This guide follows the printed booklet
[SO-ARM102_assembly_A5_v0.6.pdf](SO-ARM102_assembly_A5_v0.6.pdf) page by page.
Print the booklet on A5 landscape if you prefer paper.

Before you start:

- Print all parts from [printing.md](printing.md) and collect the hardware from [bom.md](bom.md).
- You need hex keys 1.5 mm (M2) and 2 mm (M3).
- Read two steps ahead before tightening anything. Two places in the current order are awkward, see [Known issues](../README.md#-known-issues).

> ⚠️ **The leader runs on 5 V, the follower on 12 V.** Keep the power supplies apart.

![Tools and voltage warning](../assets/images/assembly/tools-and-voltage.jpg)

## Order of work

1. Mount the horns on the servos.
2. Build the arm body **twice**, once for the follower and once for the leader (steps 1–11).
3. Build the parallel gripper (gripper steps 1–6).
4. Finish the follower: gripper, camera, controller (follower steps 1–5).
5. Finish the leader: handle, trigger, controller (leader steps 1–4).

## Servo IDs

Set each servo ID before it goes into the arm. Tools for setting IDs and calibrating are at
[lab.robonine.com](https://lab.robonine.com).

![Servo IDs](../assets/images/assembly/servo-ids.jpg)

| ID | Joint | Follower servo | Leader servo |
|:-:|---|---|---|
| 1 | Base rotation | STS3235 | STS3215 |
| 2 | Shoulder lift | STS3250 | STS3215 |
| 3 | Elbow flex | STS3250 | STS3215 |
| 4 | Wrist flex | STS3235 | STS3215 |
| 5 | Wrist roll | STS3215 | STS3215 |
| 6 | Gripper / trigger | STS3215 | STS3215 |

## 0. Servo horns

Mount one horn with an M3 × 6 screw on servo ID 1.
Servos ID 2, 3 and 4 get a horn on both sides. Horn screws come with the servos.

If you add O-rings to the leader, put them between the servo and the horn now. Getting this order wrong can jam the ring between the servo shell and the horn.

## 1–11. Arm body, follower and leader

Repeat these steps for both arms.

| Step | Parts | Fasteners |
|:-:|---|---|
| 1 | SO102.02.060 Bottom servo holder, SO102.02.040 Bottom top plate | 3 × M3×16, 3 × M3 nut |
| 2 | — | 3 × M3×16, 3 × M3 nut |
| 3 | Servo ID 1 | 4 × M2×6 |
| 4 | SO102.02.020 Base ring, bearing 6812, SO102.02.050 Bottom ring, SO102.02.010 Base | 6 × M3×16, 6 × M3 nut |
| 5 | SO102.02.030 Base washer | 4 × M3×10, 6 × M3×16 |
| 6 | Servos ID 2 and ID 3, 2 × SO102.02.070 Bottom arm, 2 short cables, 1 long cable | 16 × M2×6 |
| 7 | Servo ID 4, SO102.02.080-01 Upper arm right, 1 short cable | 4 × M2×6 |
| 8 | SO102.02.080 Upper arm left, 2 × SO102.02.130 Cable snap | 4 × M2×6, 8 × M3×10 |
| 9 | Servo ID 5, SO102.02.090 Wrist holder, servo horn | 1 × M3×6, 4 × 2×6 self-tapping |
| 10 | 1 short cable | 8 × M3×10 |
| 11 | — | 8 × M3×10 |

| | | |
|:-:|:-:|:-:|
| ![Step 1](../assets/images/assembly/steps/shared-01.jpg) | ![Step 2](../assets/images/assembly/steps/shared-02.jpg) | ![Step 3](../assets/images/assembly/steps/shared-03.jpg) |
| ![Step 4](../assets/images/assembly/steps/shared-04.jpg) | ![Step 5](../assets/images/assembly/steps/shared-05.jpg) | ![Step 6](../assets/images/assembly/steps/shared-06.jpg) |
| ![Step 7](../assets/images/assembly/steps/shared-07.jpg) | ![Step 8](../assets/images/assembly/steps/shared-08.jpg) | ![Step 9](../assets/images/assembly/steps/shared-09.jpg) |
| ![Step 10](../assets/images/assembly/steps/shared-10.jpg) | ![Step 11](../assets/images/assembly/steps/shared-11.jpg) | |

Check that each servo cable reaches the next joint with some slack before you close the joint.

## Gripper 1–6, follower only

| Step | Parts | Fasteners |
|:-:|---|---|
| 1 | RB9.01.062.040 Gear for gripper on the servo horn, servo ID 6 | 4 × M3×4 set screw, 1 × M3×6 |
| 2 | 2 × RB9.01.062.024 Clamp, 2 × RB9.01.062.030 Gear rack, 2 × RB9.01.062.100 Nail | — |
| 3 | 2 × rod Ø6 × 125 mm | — |
| 4 | RB9.01.062.011 Main frame, 2 × bearing MF106ZZ | 2 × M4×8 |
| 5 | Snap the rods into the main frame | — |
| 6 | Push the clamps to their outer stops, insert the servo | 3 × 2×6 self-tapping |

Tighten the set screws from the horn side towards the gear, so no gap opens between them.
Before step 6, move servo ID 6 to its minimum position, so the gripper closes fully and opens to the full 85 mm.
Slide both clamps along the rods by hand before closing up. They should move freely without binding.

| | | |
|:-:|:-:|:-:|
| ![Gripper 1](../assets/images/assembly/steps/gripper-01.jpg) | ![Gripper 2](../assets/images/assembly/steps/gripper-02.jpg) | ![Gripper 3](../assets/images/assembly/steps/gripper-03.jpg) |
| ![Gripper 4](../assets/images/assembly/steps/gripper-04.jpg) | ![Gripper 5](../assets/images/assembly/steps/gripper-05.jpg) | ![Gripper 6](../assets/images/assembly/steps/gripper-06.jpg) |

## Follower 1–5

| Step | Parts | Fasteners |
|:-:|---|---|
| 1 | RB9.01.060.075 Camera holder | 4 × M3×10 |
| 2 | Gripper assembly onto the wrist | 4 × 2×6 self-tapping |
| 3 | RB9.01.062.090 Camera spacer, USB camera | 4 × M2×8, 4 × M2 nut |
| 4 | SO102.02.100 Board holder follower, Waveshare Bus Servo Driver HAT | 4 × M2×8, 4 × M2 nut |
| 5 | SO102.02.100-01 Board cap follower, long cable | — |

| | | |
|:-:|:-:|:-:|
| ![Follower 1](../assets/images/assembly/steps/follower-01.jpg) | ![Follower 2](../assets/images/assembly/steps/follower-02.jpg) | ![Follower 3](../assets/images/assembly/steps/follower-03.jpg) |
| ![Follower 4](../assets/images/assembly/steps/follower-04.jpg) | ![Follower 5](../assets/images/assembly/steps/follower-05.jpg) | |

## Leader 1–4

| Step | Parts | Fasteners |
|:-:|---|---|
| 1 | SO102 Handle, SO102 Wrist roll | 4 × M3×6, 1 × 2×6 self-tapping |
| 2 | SO102 Trigger, servo ID 6 | 4 × M3×6, 4 × 2×6 self-tapping |
| 3 | SO102.02.110 Board holder leader, Waveshare Bus Servo Adapter | 4 × M2×8, 4 × M2 nut |
| 4 | SO102.02.110-01 Board cap leader, long cable | — |

| | |
|:-:|:-:|
| ![Leader 1](../assets/images/assembly/steps/leader-01.jpg) | ![Leader 2](../assets/images/assembly/steps/leader-02.jpg) |
| ![Leader 3](../assets/images/assembly/steps/leader-03.jpg) | ![Leader 4](../assets/images/assembly/steps/leader-04.jpg) |

## Mounting and first start

1. Clamp each base to the table with two C-clamps.
2. Connect the follower controller to the 12 V supply and the leader controller to the 5 V supply.
3. Connect both controllers to the computer with USB-C.
4. Calibrate both arms and start teleoperation at [lab.robonine.com](https://lab.robonine.com), or with the LeRobot SO-101 workflow.
