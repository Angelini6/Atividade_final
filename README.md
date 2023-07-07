# Atividade_final
function control(left_sensor, right_sensor, speed) {
    var error = right_sensor - left_sensor;
   var P     = 0.75;

    return {
        engineTorque: 3000,
        brakingTorque: 0,
        steeringAngle: P * error,
        log: [
            { name: 'Speed', value: speed, min: 0, max: 100 },
            { name: 'Left_sensor', value: left_sensor, min: 0, max: 1 },
            { name: 'Right_sensor', value: right_sensor, min: 0, max: 1 }
        ]
    };
}
