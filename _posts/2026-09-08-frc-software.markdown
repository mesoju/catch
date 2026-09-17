---
layout: post
title:  "FRC Software"
date:   2026-09-08 11:43:22 -0400
author: Vincent Tong
team: programming
---

If you have your own laptop for programming, you're going to need some software downloaded on your laptop before you are able to script, deploy, and control the robot. 

> [!NOTE]
> Some of the resources below may **require you to create an account** in order to install from their website. Currently, none of these vendors will clutter your inbox, but you should have a **burner e-mail** account if you prefer.
>
> Additionally, most will ask whether you would like to install this program for only your user or all users. I recommend you select the option for **'this user only'** if you have a shared computer.

> [!CAUTION]
> Some of the resources **require a computer restart**. You should only proceed after you have finished or backed up your work. 

---

## WPILib
>[WPILib Installation](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html)
>
>WPILib is a comprehensive library of tools and dependencies intended to store the majority of software you need for coding an FRC robot. It installs its own separate copy of **Visual Studio Code** where you will write all of your code, and a handful of WPILib tools. The only tools that are currently important to us are **Elastic** and **Advantage Scope**, but more on this later.

## NI Tools
>[!WARNING]
>These tools MAY be **deprecated after 2026**, as these were created in partnership with *National Instruments LabVIEW* which use the **roboRIO**, however FRC has decided to roll out the **Systemcore** by *Limelight* in future seasons.<br> ***As of 9/17/26, WPILib is planning for a new driver station app.***

>[Driver Station Installation](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/frc-game-tools.html)
>
> NI Tools is another software suite that provides the **Driver Station** app and the **roboRIO Imaging Tool**. Driver Station is used to control and interact robots that use the **roboRIO**, and the Imaging Tool is used to update **roboRIO** firmware. You will use the Driver Station much more often. 

## Phoenix Tuner X
>[Phoenix Tuner X Installation](https://apps.microsoft.com/detail/9nvv4pwdw27z?hl=en-US&gl=US)
>
>Phoenix Tuner X is an app that allows you to configure and update connected motors, sensors, and CanBUS expansions that are ***built by CTR Electronics***. Most accessories on our team's robot after 2026 should be **CTRE devices**, however if you utilize another device (i.e. REV's SPARK MAX + Neo motors), you will **not be able to see those devices on this app**. This app can also be extremely useful in **determining what devices are successfully connected and seen by the robot**, as well as **auto-generating swerve drive for robots** that utilize CTRE's swerve drivetrain.

## REV Hardware Client
>[REV Hardware Client Installation](https://docs.revrobotics.com/rev-hardware-client)
>
>REV Hardware Client allows you to control devices that are ***built by REV Robotics***. While most of our devices have upgraded to **CTRE**, devices such as the robot power-distribution hub (PDH) still requires **REV** software to manage. For the first few weeks of robot prototyping, the PDH will fault *many times*. It is important to connect to the PDH with the software via USB-C cable in order to clear these faults and allow the PDH to continue operating. PDHs will *fault* to indicate when an issue has occurred in delivering power and will often **halt power delivery until the issue is resolved and manually cleared in the Hardware Client.**

## PathPlanner
>[PathPlanner Installation](https://apps.microsoft.com/detail/9nqbkb5dw909?hl=en-US&gl=US)
>
>PathPlanner is an app that allows you to create robot autonomous actions in an extremely clean environment using bezier curves. It can also run `NamedCommands` that are defined for auto. 