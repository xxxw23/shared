本次修改了:
solefoot_flat_config.commands.range.lin_vel_x
solefoot_flat_config.commands.range.lin_vel_y
让速度范围变大

solefoot_flat_config.gait.range.frequencies
让步频变快
solefoot_flat_config.gait.range.durations
减少每一步持续的时间
solefoot_flat_config.gait.range.swing_height
增大摆腿高度范围，防止高速时被绊倒

solefoot_flat_config.control.action_scale
增大动作生效概率

solefoot_flat_config.control.user_torque_limit
solefoot_flat_config.control.max_power
增大电机功率

class reward:
    class scale:
        tracking_lin_vel_x = 3.0 # 增大速度奖励
        # 减小与速度相关的惩罚
        torques = -0.00003
        action_rate = -0.005
        collision = -50
        orientation = -2.0
        zero_command_nominal_state = -5.0
其中，collision是跌倒惩罚，本次设置的较小，如果不够稳定可以再设大一些
zero_command_nominal_state让机器人更倾向与稳态与零速
