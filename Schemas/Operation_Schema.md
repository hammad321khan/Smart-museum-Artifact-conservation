# Smart Museum Artifact Conservation System

# Task 2 — Complete Operation Schema

## Operation Schema Format

Each operation is defined using the following fields:

- Operation ID
- Operation Name
- Trigger
- Preconditions
- Inputs
- Processing
- Outputs
- Postconditions
- Exceptions

---

## O1 — Perform System Self-Check

**Operation ID:** O1

**Operation Name:** Perform System Self-Check

**Trigger:** Chamber is powered on.

**Preconditions:**
- Chamber power is available.
- Sensors and environmental-control devices are connected.

**Inputs:**
- Sensor status.
- Environmental-control device status.

**Processing:**
- Check all essential sensors.
- Check environmental-control devices.
- Determine whether all required components are functioning correctly.

**Outputs:**
- Self-check result.

**Postconditions:**
- If all essential components are working, the chamber can enter normal monitoring.
- If a required component fails, normal conservation cannot begin.

**Exceptions:**
- Sensor failure.
- Environmental-control device failure.

---

## O2 — Verify Sensor Availability

**Operation ID:** O2

**Operation Name:** Verify Sensor Availability

**Trigger:** Before normal conservation begins or when sensor status must be verified.

**Preconditions:**
- Required sensors are installed.

**Inputs:**
- Temperature sensor status.
- Humidity sensor status.
- Vibration sensor status.
- Door sensor status.
- Other required sensor readings.

**Processing:**
- Check whether sensors are operational.
- Check whether sensor readings are valid.

**Outputs:**
- Sensor availability status.

**Postconditions:**
- Sensor status is confirmed as valid or a sensor problem is identified.

**Exceptions:**
- Missing sensor.
- Sensor malfunction.
- Invalid sensor reading.

---

## O3 — Record Artifact Information

**Operation ID:** O3

**Operation Name:** Record Artifact Information

**Trigger:** An artifact is placed inside the chamber.

**Preconditions:**
- The chamber is available for artifact placement.
- Artifact identification information is available.

**Inputs:**
- Artifact identification.
- Artifact details.

**Processing:**
- Capture and store the artifact identification information.

**Outputs:**
- Stored artifact record.

**Postconditions:**
- The artifact is registered in the conservation system.

**Exceptions:**
- Missing artifact identification.
- Invalid artifact information.

---

## O4 — Load Environmental Profile

**Operation ID:** O4

**Operation Name:** Load Environmental Profile

**Trigger:** Artifact information has been recorded.

**Preconditions:**
- Artifact record exists.
- Required environmental limits are available.

**Inputs:**
- Artifact environmental requirements.
- Temperature limits.
- Humidity limits.
- Other required environmental limits.

**Processing:**
- Load the environmental limits associated with the artifact.

**Outputs:**
- Active environmental profile.

**Postconditions:**
- The system knows the permitted environmental ranges for the artifact.

**Exceptions:**
- Environmental profile unavailable.
- Invalid environmental limits.

---

## O5 — Monitor Environmental Conditions

**Operation ID:** O5

**Operation Name:** Monitor Environmental Conditions

**Trigger:** Artifact is inside the chamber.

**Preconditions:**
- Required sensors are operational.
- Artifact information has been recorded.

**Inputs:**
- Temperature.
- Humidity.
- Light exposure.
- Vibration.
- Door status.
- Artifact condition.
- Power availability.

**Processing:**
- Continuously collect and evaluate environmental sensor readings.

**Outputs:**
- Current environmental status.

**Postconditions:**
- The system has current environmental information for decision making.

**Exceptions:**
- Sensor failure.
- Invalid reading.
- Communication failure with a sensor.

---

## O6 — Verify Chamber Door Status

**Operation ID:** O6

**Operation Name:** Verify Chamber Door Status

**Trigger:** Before active conservation begins or when door status changes.

**Preconditions:**
- Door sensor is operational.

**Inputs:**
- Current chamber door status.

**Processing:**
- Determine whether the chamber door is open or closed.

**Outputs:**
- Door status.

**Postconditions:**
- Conservation can only begin when the door is confirmed closed.

**Exceptions:**
- Door sensor failure.
- Unknown door status.

---

## O7 — Compare Temperature With Permitted Range

**Operation ID:** O7

**Operation Name:** Compare Temperature With Permitted Range

**Trigger:** Temperature monitoring occurs.

**Preconditions:**
- Artifact environmental profile is loaded.
- Temperature sensor is operational.

**Inputs:**
- Current temperature.
- Minimum permitted temperature.
- Maximum permitted temperature.

**Processing:**
- Compare the current temperature with the permitted range.

**Outputs:**
- Temperature status: Within Range or Outside Range.

**Postconditions:**
- The system determines whether temperature correction is required.

**Exceptions:**
- Invalid temperature reading.
- Temperature limits unavailable.

---

## O8 — Correct Temperature

**Operation ID:** O8

**Operation Name:** Correct Temperature

**Trigger:** Temperature is outside the permitted range.

**Preconditions:**
- Temperature deviation has been detected.
- Environmental-control mechanism is available.

**Inputs:**
- Current temperature.
- Required temperature range.

**Processing:**
- Activate the appropriate environmental-control mechanism.
- Attempt to restore temperature to the permitted range.

**Outputs:**
- Temperature correction command.

**Postconditions:**
- Temperature is corrected or the recovery attempt is unsuccessful.

**Exceptions:**
- Environmental-control mechanism failure.
- Recovery period exceeded.

---

## O9 — Verify Temperature Recovery

**Operation ID:** O9

**Operation Name:** Verify Temperature Recovery

**Trigger:** A temperature correction command has been issued.

**Preconditions:**
- Temperature correction has been attempted.
- Temperature sensor is operational.

**Inputs:**
- Current temperature.
- Permitted temperature range.
- Recovery time.

**Processing:**
- Read the temperature sensor.
- Determine whether temperature has returned to the permitted range.
- Continue verification during the allowed recovery period.

**Outputs:**
- Temperature recovery result.

**Postconditions:**
- Temperature is confirmed within range, or recovery is declared unsuccessful.

**Exceptions:**
- Temperature remains outside the permitted range.
- Sensor failure.
- Recovery period exceeded.

---

## O10 — Compare Humidity With Permitted Range

**Operation ID:** O10

**Operation Name:** Compare Humidity With Permitted Range

**Trigger:** Humidity monitoring occurs.

**Preconditions:**
- Artifact environmental profile is loaded.
- Humidity sensor is operational.

**Inputs:**
- Current humidity.
- Minimum permitted humidity.
- Maximum permitted humidity.

**Processing:**
- Compare current humidity with the permitted range.

**Outputs:**
- Humidity status: Within Range or Outside Range.

**Postconditions:**
- The system determines whether humidity correction is required.

**Exceptions:**
- Invalid humidity reading.
- Humidity limits unavailable.

---

## O11 — Correct Humidity

**Operation ID:** O11

**Operation Name:** Correct Humidity

**Trigger:** Humidity is outside the permitted range.

**Preconditions:**
- Humidity deviation has been detected.
- Environmental-control mechanism is available.

**Inputs:**
- Current humidity.
- Required humidity range.

**Processing:**
- Activate the appropriate environmental-control mechanism.
- Attempt to restore humidity to the permitted range.

**Outputs:**
- Humidity correction command.

**Postconditions:**
- Humidity is corrected or the recovery attempt is unsuccessful.

**Exceptions:**
- Environmental-control mechanism failure.
- Recovery period exceeded.

---

## O12 — Verify Humidity Recovery

**Operation ID:** O12

**Operation Name:** Verify Humidity Recovery

**Trigger:** A humidity correction command has been issued.

**Preconditions:**
- Humidity correction has been attempted.
- Humidity sensor is operational.

**Inputs:**
- Current humidity.
- Permitted humidity range.
- Recovery time.

**Processing:**
- Read the humidity sensor.
- Determine whether humidity has returned to the permitted range.
- Continue verification during the allowed recovery period.

**Outputs:**
- Humidity recovery result.

**Postconditions:**
- Humidity is confirmed within range, or recovery is declared unsuccessful.

**Exceptions:**
- Humidity remains outside the permitted range.
- Sensor failure.
- Recovery period exceeded.

---

# Additional Operations

The following operations are also identified from the scenario:

## O13 — Activate Protection Measures

**Trigger:** Environmental condition cannot be corrected within the allowed recovery period.

**Preconditions:**
- Artifact is inside the chamber.
- Recovery attempt has failed.

**Inputs:**
- Environmental condition status.
- Artifact protection requirements.

**Processing:**
- Reduce light exposure.
- Activate additional environmental controls.

**Outputs:**
- Protection controls activated.

**Postconditions:**
- Artifact protection measures are active.

**Exceptions:**
- Additional control mechanism unavailable.

---

## O14 — Generate Operator Alert

**Trigger:** Protection response is activated.

**Preconditions:**
- An abnormal condition requiring operator attention has been detected.

**Inputs:**
- Fault information.
- Environmental condition.
- Artifact information.

**Processing:**
- Generate an alert for the museum operator.

**Outputs:**
- Operator alert.

**Postconditions:**
- Operator is notified of the abnormal condition.

**Exceptions:**
- Alert mechanism unavailable.

---

## O15 — Detect Significant Vibration

**Trigger:** Vibration sensor detects movement.

**Preconditions:**
- Artifact is inside the chamber.
- Vibration sensor is operational.

**Inputs:**
- Vibration sensor reading.
- Permitted vibration threshold.

**Processing:**
- Compare the vibration reading with the permitted threshold.

**Outputs:**
- Vibration status.

**Postconditions:**
- Significant vibration is identified when the threshold is exceeded.

**Exceptions:**
- Vibration sensor failure.

---

## O16 — Verify Vibration Stabilization

**Trigger:** Significant vibration has stopped.

**Preconditions:**
- Vibration response has been activated.
- Vibration sensor is operational.

**Inputs:**
- Current vibration level.
- Permitted vibration threshold.
- Required stabilization period.

**Processing:**
- Monitor vibration continuously.
- Verify that the level remains below the permitted threshold for the required period.

**Outputs:**
- Stabilization result.

**Postconditions:**
- Normal operation can be considered for resumption only after successful stabilization.

**Exceptions:**
- Vibration rises above the threshold again.
- Stabilization period not completed.

---

## O17 — Suspend Conservation Activities

**Trigger:** Chamber door opens or significant vibration is detected.

**Preconditions:**
- Conservation activities are active.

**Inputs:**
- Door status.
- Vibration status.

**Processing:**
- Immediately suspend activities that could increase risk to the artifact.

**Outputs:**
- Conservation suspension command.

**Postconditions:**
- Risk-increasing conservation activities are stopped.

**Exceptions:**
- Control system failure.

---

## O18 — Verify Safe Conditions

**Trigger:** Door is closed again or artifact removal is requested.

**Preconditions:**
- Required sensors are operational.

**Inputs:**
- Environmental conditions.
- Sensor status.
- Protection response status.
- Door status.

**Processing:**
- Verify that environmental conditions are acceptable.
- Verify sensor status.
- Verify that no active protection response is underway.

**Outputs:**
- Safe condition result.

**Postconditions:**
- System confirms whether normal operation or artifact removal is safe.

**Exceptions:**
- Environmental condition outside limits.
- Sensor failure.
- Protection response still active.

---

## O19 — Switch to Emergency Power

**Trigger:** Normal power is lost.

**Preconditions:**
- Emergency power source is available.

**Inputs:**
- Power availability status.

**Processing:**
- Activate and switch to the emergency power source.

**Outputs:**
- Emergency power activated.

**Postconditions:**
- System continues operating using emergency power.

**Exceptions:**
- Emergency power unavailable.

---

## O20 — Record Power Failure Incident

**Trigger:** Normal power is lost.

**Preconditions:**
- System can record events.

**Inputs:**
- Power failure information.
- Timestamp.
- System status.

**Processing:**
- Record the power failure incident.

**Outputs:**
- Stored power failure event.

**Postconditions:**
- Power failure is available in the system event record.

**Exceptions:**
- Event storage unavailable.

---

## O21 — Perform Safe Shutdown

**Trigger:** Normal power is lost and emergency power is unavailable.

**Preconditions:**
- Emergency power is unavailable.

**Inputs:**
- Power status.
- System status.

**Processing:**
- Record the incident.
- Stop normal conservation activities.
- Safely shut down the system.

**Outputs:**
- Safe shutdown status.

**Postconditions:**
- System enters a safe shutdown condition.

**Exceptions:**
- Shutdown mechanism failure.

---

## O22 — Authorize Artifact Removal

**Trigger:** Operator requests artifact removal.

**Preconditions:**
- Artifact is inside the chamber.
- Chamber is confirmed safe.
- No active protection response is underway.

**Inputs:**
- Environmental status.
- Sensor status.
- Protection response status.
- Operator removal request.

**Processing:**
- Verify all safety conditions.
- Approve or reject artifact removal.

**Outputs:**
- Removal authorization or rejection.

**Postconditions:**
- Artifact removal is authorized only when all safety conditions are satisfied.

**Exceptions:**
- Unsafe environmental condition.
- Sensor failure.
- Active protection response.
