# -*- coding: utf-8 -*-
"""
Created on Tue Oct 17 14:47:43 2023

@author: aayamc
"""

# -*- coding: utf-8 -*-
"""
Created on Sat Oct 14 13:47:01 2023

@author: aayamc
"""

import pandas as pd 
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt 
import plotly.graph_objects as go
import plotly.offline as pyo
import statistics 



qns = pd.read_csv('bratteberg_141_230315_093400_nilu_noserialnumber.csv',encoding='latin1')
qns.info()
qns.head()


feel_air = qns['feel_air']
x11 = qns['feel_air'].value_counts()[0]
print(qns['feel_air'].value_counts()[0])
x12 = qns['feel_air'].value_counts()[1]
print(qns['feel_air'].value_counts()[1])
x13 = qns['feel_air'].value_counts()[2]
print(qns['feel_air'].value_counts()[2])
x14 = qns['feel_air'].value_counts()[3]
print(qns['feel_air'].value_counts()[3])
x15 = qns['feel_air'].value_counts()[4]
print(qns['feel_air'].value_counts()[4])
x1sum = x11 + x12 + x13 + x14 + x15

p11 = (x11/x1sum)*100
p12 = (x12/x1sum)*100
p13 = (x13/x1sum)*100
p14 = (x14/x1sum)*100
p15 = (x15/x1sum)*100






print('Okay')
print(x1sum)

y11 = qns['_air_smell'].value_counts()[1]
print(qns['_air_smell'].value_counts()[1])

y12 = qns['_air_heavy'].value_counts()[1]
print(qns['_air_heavy'].value_counts()[1])

y13 = qns['_air_dry'].value_counts()[1]
print(qns['_air_dry'].value_counts()[1])

y14 = qns['_air_dust'].value_counts()[1]
print(qns['_air_dust'].value_counts()[1])

Y1 = [y11, y12, y13, y14]

feel_temp = qns['feel_temp']
x21 = qns['feel_temp'].value_counts()[0]
print(qns['feel_temp'].value_counts()[0])
x22 = qns['feel_temp'].value_counts()[1]
print(qns['feel_temp'].value_counts()[1])
x23 = qns['feel_temp'].value_counts()[2]
print(qns['feel_temp'].value_counts()[2])
x24 = qns['feel_temp'].value_counts()[3]
print(qns['feel_temp'].value_counts()[3])
x25 = qns['feel_temp'].value_counts()[4]
print(qns['feel_temp'].value_counts()[4])
x2sum = x21 + x22 + x23 + x24 + x25

p21 = (x21/x2sum)*100
p22 = (x22/x2sum)*100
p23 = (x23/x2sum)*100
p24 = (x24/x2sum)*100
p25 = (x25/x2sum)*100

per25 = x25/x2sum

print('Okay')
print(x2sum)

y21 = qns['_temp_el_shock'].value_counts()[1]
print(qns['_temp_el_shock'].value_counts()[1])

y22 = qns['_temp_coldhot'].value_counts()[1]
print(qns['_air_heavy'].value_counts()[1])

y23 = qns['_temp_draw'].value_counts()[1]
print(qns['_temp_draw'].value_counts()[1])

y24 = qns['_temp_floor_cold'].value_counts()[1]
print(qns['_temp_floor_cold'].value_counts()[1])

y25 = qns['_temp_heatsun'].value_counts()[1]
print(qns['_temp_heatsun'].value_counts()[1])

y26 = qns['_temp_heater'].value_counts()[1]
print(qns['_temp_heater'].value_counts()[1])

Y2 = [y21, y22, y23, y24, y25, y26]

feel_light = qns['feel_light']
x31 = qns['feel_light'].value_counts()[0]
print(qns['feel_light'].value_counts()[0])
x32 = qns['feel_light'].value_counts()[1]
print(qns['feel_light'].value_counts()[1])
x33 = qns['feel_light'].value_counts()[2]
print(qns['feel_light'].value_counts()[2])
x34 = qns['feel_light'].value_counts()[3]
print(qns['feel_light'].value_counts()[3])
x35 = qns['feel_light'].value_counts()[4]
print(qns['feel_light'].value_counts()[4])
x3sum = x31 + x32 + x33 + x34 + x35

p31 = (x31/x3sum)*100
p32 = (x32/x3sum)*100
p33 = (x33/x3sum)*100
p34 = (x34/x3sum)*100
p35 = (x35/x3sum)*100

per35 = x35/x3sum

print('Okay')
print(x3sum)

y31 = qns['_light_sun'].value_counts()[1]
print(qns['_light_sun'].value_counts()[1])

y32 = qns['_light_lamp_hi'].value_counts()[1]
print(qns['_light_lamp_hi'].value_counts()[1])

y33 = qns['_light_lamp_low'].value_counts()[1]
print(qns['_light_lamp_low'].value_counts()[1])


Y3 = [y31, y32, y33]

feel_health = qns['feel_health']
x41 = qns['feel_health'].value_counts()[0]
print(qns['feel_health'].value_counts()[0])
x42 = qns['feel_health'].value_counts()[1]
print(qns['feel_health'].value_counts()[1])
x43 = qns['feel_health'].value_counts()[2]
print(qns['feel_health'].value_counts()[2])
x44 = qns['feel_health'].value_counts()[3]
print(qns['feel_health'].value_counts()[3])
x45 = qns['feel_health'].value_counts()[4]
print(qns['feel_health'].value_counts()[4])
x4sum = x41 + x42 + x43 + x44 + x45

p41 = (x41/x4sum)*100
p42 = (x42/x4sum)*100
p43 = (x43/x4sum)*100
p44 = (x44/x4sum)*100
p45 = (x45/x4sum)*100

per45 = x45/x4sum

print('Okay')
print(x4sum)

y41 = qns['_health_head'].value_counts()[1]
print(qns['_health_head'].value_counts()[1])

y42 = qns['_health_cough'].value_counts()[1]
print(qns['_health_cough'].value_counts()[1])

y43 = qns['_health_tired'].value_counts()[1]
print(qns['_health_tired'].value_counts()[1])

y44 = qns['_health_dryskin'].value_counts()[1]
print(qns['_health_dryskin'].value_counts()[1])

Y4 = [y41, y42, y43, y44]

feel_noise = qns['feel_noise']
x51 = qns['feel_noise'].value_counts()[0]
print(qns['feel_noise'].value_counts()[0])
x52 = qns['feel_noise'].value_counts()[1]
print(qns['feel_noise'].value_counts()[1])
x53 = qns['feel_noise'].value_counts()[2]
print(qns['feel_noise'].value_counts()[2])
x54 = qns['feel_noise'].value_counts()[3]
print(qns['feel_noise'].value_counts()[3])
x55 = qns['feel_noise'].value_counts()[4]
print(qns['feel_noise'].value_counts()[4])
x5sum = x51 + x52 + x53 + x54 + x55

p51 = (x51/x5sum)*100
p52 = (x52/x5sum)*100
p53 = (x53/x5sum)*100
p54 = (x54/x5sum)*100
p55 = (x55/x5sum)*100

print('Okay')
print(x5sum)

per55 = x55/x5sum


genre = ['Excellent', 'Good', 'Fair', 'Poor', 'Bad']
c_1 = [p11, p12, p13, p14, p15]
c_2 = [p21, p22, p23, p24, p25]
c_3 = [p31, p32, p33, p34, p35]
c_4 = [p41, p42, p43, p44, p45]
c_5 = [p51, p52, p53, p54, p55]

fig = go.Figure(
    data=[
        go.Scatterpolar(r=c_1, theta=genre, fill='toself', name='How is air?'),
        go.Scatterpolar(r=c_2, theta=genre, fill='toself', name='How is temperautre?'),
        go.Scatterpolar(r=c_3, theta=genre, fill='toself', name='How is light?'),
        go.Scatterpolar(r=c_4, theta=genre, fill='toself', name='How is your health?'),
        go.Scatterpolar(r=c_5, theta=genre, fill='toself', name='How is acoustic?')
    ],
    layout=go.Layout(
        title=go.layout.Title(text='Bratteberg room 141'),
        polar={'radialaxis': {'visible': True}},
        showlegend=True
    )
)


pyo.plot(fig)




per15 = (x15/x1sum) * 100
per25 = (x25/x2sum) * 100
per35 = (x35/x3sum) * 100
per45 = (x45/x4sum) * 100
per55 = (x55/x5sum) * 100
print(per15)
print(per25)
print(per35)
print(per45)
print(per55)
perx = ('Air','Temperature','light','Health', 'Noise' )
pery = [per15, per25, per35, per45, per55]


day1 = qns.iloc[0:100, 10]

day1B = day1.value_counts()[4]
print('Number of dissatisfied vote')
print(day1B)
day1P = day1.value_counts()[3]
print('Number of dissatisfied vote')
print(day1P)
t_1= 100
p_11 = (day1B/100) * 100
p_12 = (day1P/100) * 100
P_1 = p_11 + p_12

ACC1 = statistics.mean(qns.iloc[0:100, 9])
print('The ACC is')
print(ACC1)
PD_air1 = (np.exp(-0.18 - 5.28 * ACC1))/(1 + np.exp(-0.18 - 5.28 * ACC1))  * 100
print('the pd air is ')
print(PD_air1)
decipol_1 = 112 * (np.log (PD_air1)- 5.98)**(-4)
print(decipol_1)
m_col_hot_1 = statistics.mean(qns.iloc[0:100, 19])
PD_elec_1 = (qns.iloc[0:100, 18].value_counts()[1]/(qns.iloc[0:100, 18].value_counts()[1]+qns.iloc[0:100, 18].value_counts()[0]))*100
PD_draw_1 = (qns.iloc[0:100, 20].value_counts()[1]/(qns.iloc[0:100, 20].value_counts()[1]+qns.iloc[0:100, 20].value_counts()[0]))*100
PD_coldfloor_1 = (qns.iloc[0:100, 21].value_counts()[1]/(qns.iloc[0:100, 21].value_counts()[1]+qns.iloc[0:100, 21].value_counts()[0]))*100
PD_heatsun_1 = 0
PD_heater_1 = (qns.iloc[0:100, 23].value_counts()[1]/(qns.iloc[0:100, 23].value_counts()[1]+qns.iloc[0:100, 23].value_counts()[0]))*100
PPD_m_col_hot_1 = (100 - 95 * np.exp(-0.03353 * m_col_hot_1**4 - 0.2179 * m_col_hot_1**2))

PD_smell1 = (qns.iloc[0:100, 14].value_counts()[1]/(qns.iloc[0:100, 14].value_counts()[1]+qns.iloc[0:100, 14].value_counts()[0]))*100
PD_heavy1 = (qns.iloc[0:100, 15].value_counts()[1]/(qns.iloc[0:100, 15].value_counts()[1]+qns.iloc[0:100, 15].value_counts()[0]))*100
PD_dry1 = (qns.iloc[0:100, 16].value_counts()[1]/(qns.iloc[0:100, 16].value_counts()[1]+qns.iloc[0:100, 16].value_counts()[0]))*100
PD_dust1 = (qns.iloc[0:100, 17].value_counts()[1]/(qns.iloc[0:100, 17].value_counts()[1]+qns.iloc[0:100, 17].value_counts()[0]))*100


Per_t_1 = PD_elec_1 + PD_draw_1 + PD_coldfloor_1 + PD_heatsun_1 + PD_heater_1 + PPD_m_col_hot_1

Per_PD_elec_1 = PD_elec_1 / Per_t_1
Per_PD_draw_1 = PD_draw_1 / Per_t_1
Per_PD_coldfloor_1 = PD_coldfloor_1 / Per_t_1
Per_PD_heatsun_1 = 0 
Per_PD_heater_1 = PD_heater_1 / Per_t_1
Per_PPD_m_col_hot_1 = PPD_m_col_hot_1 / Per_t_1

Per_ta_1 = PD_smell1 + PD_heavy1 + PD_dry1 + PD_dust1
Per_PD_smell1 = PD_smell1 / Per_ta_1
Per_PD_heavy1 = PD_heavy1 / Per_ta_1
Per_PD_dry1 = PD_dry1 / Per_ta_1
Per_PD_dust1 = PD_dust1 / Per_ta_1


day2 = qns.iloc[101:151, 10]
print('its here')
print(day2)

day2B = day2.value_counts()[4]
print('Number of dissatisfied vote')
print(day2B)
day2P = day2.value_counts()[3]
print('Number of dissatisfied vote')
print(day2P)
t_2= 50
p_21 = (day2B/50) * 100
p_22 = (day2P/50) * 100
P_2 = p_21 + p_22


ACC2 = statistics.mean(qns.iloc[101:151, 9])
PD_air2 = (np.exp(-0.18 - 5.28 * ACC2))/(1 + np.exp(-0.18 - 5.28 * ACC2))  * 100
decipol_2 = 112 * (np.log (PD_air2)- 5.98)**(-4)

m_col_hot_2 = statistics.mean(qns.iloc[101:151, 19])
print(m_col_hot_2)
PD_elec_2 = (qns.iloc[101:151, 18].value_counts()[1]/(qns.iloc[101:151, 18].value_counts()[1]+qns.iloc[101:151, 18].value_counts()[0]))*100
PD_draw_2 = (qns.iloc[101:151, 20].value_counts()[1]/(qns.iloc[101:151, 20].value_counts()[1]+qns.iloc[101:151, 20].value_counts()[0]))*100
PD_coldfloor_2 = (qns.iloc[101:151, 21].value_counts()[1]/(qns.iloc[101:151, 21].value_counts()[1]+qns.iloc[101:151, 21].value_counts()[0]))*100
PD_heatsun_2 = (qns.iloc[101:151, 22].value_counts()[1]/(qns.iloc[101:151, 22].value_counts()[1]+qns.iloc[101:151, 22].value_counts()[0]))*100
PD_heater_2 = (qns.iloc[101:151, 23].value_counts()[1]/(qns.iloc[101:151, 23].value_counts()[1]+qns.iloc[101:151, 23].value_counts()[0]))*100
PPD_m_col_hot_2 = (100 - 95 * np.exp(-0.03353 * m_col_hot_2**4 - 0.2179 * m_col_hot_2**2))


PD_smell2 = 0
PD_heavy2 = (qns.iloc[101:151, 15].value_counts()[1]/(qns.iloc[101:151, 15].value_counts()[1]+qns.iloc[101:151, 15].value_counts()[0]))*100
PD_dry2 = (qns.iloc[101:151, 16].value_counts()[1]/(qns.iloc[101:151, 16].value_counts()[1]+qns.iloc[101:151, 16].value_counts()[0]))*100
PD_dust2 = (qns.iloc[101:151, 17].value_counts()[1]/(qns.iloc[101:151, 17].value_counts()[1]+qns.iloc[101:151, 17].value_counts()[0]))*100



Per_t_2 = PD_elec_2 + PD_draw_2 + PD_coldfloor_2 + PD_heatsun_2 + PD_heater_2 + PPD_m_col_hot_2
Per_ta_2 = PD_smell2 + PD_heavy2 + PD_dry2 + PD_dust2
Per_PD_smell2 = PD_smell2 / Per_ta_2
Per_PD_heavy2 = PD_heavy2 / Per_ta_2
Per_PD_dry2 = PD_dry2 / Per_ta_2
Per_PD_dust2 = PD_dust2 / Per_ta_2

Per_PD_elec_2 = PD_elec_2 / Per_t_2
Per_PD_draw_2 = PD_draw_2 / Per_t_2
Per_PD_coldfloor_2 = PD_coldfloor_2 / Per_t_2
Per_PD_heatsun_2 = PD_heatsun_2 / Per_t_2
Per_PD_heater_2 = PD_heater_2 / Per_t_2
Per_PPD_m_col_hot_2 = PPD_m_col_hot_2 / Per_t_2

day3 = qns.iloc[152:205, 10]

day3B = day3.value_counts()[4]
print('Number of dissatisfied vote')
print(day3B)
day3P = day3.value_counts()[3]
print('Number of dissatisfied vote')
print(day3P)
t_3= 205 - 152
p_31 = (day3B/t_3) * 100
p_32 = (day3P/t_3) * 100
P_3 = p_31 + p_32


ACC3 = statistics.mean(qns.iloc[152:205, 9])
PD_air3 = (np.exp(-0.18 - 5.28 * ACC3))/(1 + np.exp(-0.18 - 5.28 * ACC3))  * 100
decipol_3 = 112 * (np.log (PD_air3)- 5.98)**(-4)


m_col_hot_3 = statistics.mean(qns.iloc[152:205, 19])
print(m_col_hot_3)
PD_elec_3 = (qns.iloc[152:205, 18].value_counts()[1]/(qns.iloc[152:205, 18].value_counts()[1]+qns.iloc[152:205, 18].value_counts()[0]))*100
PD_draw_3 = (qns.iloc[152:205, 20].value_counts()[1]/(qns.iloc[152:205, 20].value_counts()[1]+qns.iloc[152:205, 20].value_counts()[0]))*100
PD_coldfloor_3 = (qns.iloc[152:205, 21].value_counts()[1]/(qns.iloc[152:205, 21].value_counts()[1]+qns.iloc[152:205, 21].value_counts()[0]))*100
PD_heatsun_3 = (qns.iloc[152:205, 22].value_counts()[1]/(qns.iloc[152:205, 22].value_counts()[1]+qns.iloc[152:205, 22].value_counts()[0]))*100
PD_heater_3 = (qns.iloc[152:205, 23].value_counts()[1]/(qns.iloc[152:205, 23].value_counts()[1]+qns.iloc[152:205, 23].value_counts()[0]))*100
PPD_m_col_hot_3 = (100 - 95 * np.exp(-0.03353 * m_col_hot_3**4 - 0.2179 * m_col_hot_3**2))



PD_smell3 = (qns.iloc[152:205, 14].value_counts()[1]/(qns.iloc[152:205, 14].value_counts()[1]+qns.iloc[152:205, 14].value_counts()[0]))*100
PD_heavy3 = (qns.iloc[152:205, 15].value_counts()[1]/(qns.iloc[152:205, 15].value_counts()[1]+qns.iloc[152:205, 15].value_counts()[0]))*100
PD_dry3 = (qns.iloc[152:205, 16].value_counts()[1]/(qns.iloc[152:205, 16].value_counts()[1]+qns.iloc[152:205, 16].value_counts()[0]))*100
PD_dust3 = (qns.iloc[152:205, 17].value_counts()[1]/(qns.iloc[152:205, 17].value_counts()[1]+qns.iloc[152:205, 17].value_counts()[0]))*100


Per_t_3 = PD_elec_3 + PD_draw_3 + PD_coldfloor_3 + PD_heatsun_3 + PD_heater_3 + PPD_m_col_hot_3
Per_ta_3 = PD_smell3 + PD_heavy3 + PD_dry3 + PD_dust3
Per_PD_elec_3 = PD_elec_3 / Per_t_3
Per_PD_draw_3 = PD_draw_3 / Per_t_3
Per_PD_coldfloor_3 = PD_coldfloor_3 / Per_t_3
Per_PD_heatsun_3 = PD_heatsun_3 / Per_t_3
Per_PD_heater_3 = PD_heater_3 / Per_t_3
Per_PPD_m_col_hot_3 = PPD_m_col_hot_3 / Per_t_3


Per_ta_3 = PD_smell3 + PD_heavy3 + PD_dry3 + PD_dust3
Per_PD_smell3 = PD_smell3 / Per_ta_3
Per_PD_heavy3 = PD_heavy3 / Per_ta_3
Per_PD_dry3 = PD_dry3 / Per_ta_3
Per_PD_dust3 = PD_dust3 / Per_ta_3

day4 = qns.iloc[206:253, 10]

day4B = day4.value_counts()[4]
print('Number of dissatisfied vote')
print(day4B)
day4P = day4.value_counts()[3]
print('Number of dissatisfied vote')
print(day4P)
t_4= 253 - 206
p_41 = (day4B/t_4) * 100
p_42 = (day4P/t_4) * 100
P_4 = p_41 + p_42

ACC4 = statistics.mean(qns.iloc[206:253, 9])
PD_air4 = (np.exp(-0.18 - 5.28 * ACC4))/(1 + np.exp(-0.18 - 5.28 * ACC4))  * 100
decipol_4 = 112 * (np.log (PD_air4)- 5.98)**(-4)



PD_elec_4 = (qns.iloc[206:253, 18].value_counts()[1]/(qns.iloc[206:253, 18].value_counts()[1]+qns.iloc[206:253, 18].value_counts()[0]))*100
PD_draw_4 = (qns.iloc[206:253, 20].value_counts()[1]/(qns.iloc[206:253, 20].value_counts()[1]+qns.iloc[206:253, 20].value_counts()[0]))*100
PD_coldfloor_4 = (qns.iloc[206:253, 21].value_counts()[1]/(qns.iloc[206:253, 21].value_counts()[1]+qns.iloc[206:253, 21].value_counts()[0]))*100
PD_heatsun_4 = (qns.iloc[206:253, 22].value_counts()[1]/(qns.iloc[206:253, 22].value_counts()[1]+qns.iloc[206:253, 22].value_counts()[0]))*100
PD_heater_4 = (qns.iloc[206:253, 23].value_counts()[1]/(qns.iloc[206:253, 23].value_counts()[1]+qns.iloc[206:253, 23].value_counts()[0]))*100


m_col_hot_4 = statistics.mean(qns.iloc[206:253, 19])
print(m_col_hot_4)



PPD_m_col_hot_4 = (100 - 95 * np.exp(-0.03353 * m_col_hot_4**4 - 0.2179 * m_col_hot_4**2))

PD_smell4 = (qns.iloc[206:253, 14].value_counts()[1]/(qns.iloc[206:253, 14].value_counts()[1]+qns.iloc[206:253, 14].value_counts()[0]))*100
PD_heavy4 = (qns.iloc[206:253, 15].value_counts()[1]/(qns.iloc[206:253, 15].value_counts()[1]+qns.iloc[206:253, 15].value_counts()[0]))*100
PD_dry4 = (qns.iloc[206:253, 16].value_counts()[1]/(qns.iloc[206:253, 16].value_counts()[1]+qns.iloc[206:253, 16].value_counts()[0]))*100
PD_dust4 = (qns.iloc[206:253, 17].value_counts()[1]/(qns.iloc[206:253, 17].value_counts()[1]+qns.iloc[206:253, 17].value_counts()[0]))*100



Per_t_4 = PD_elec_4 + PD_draw_4 + PD_coldfloor_4 + PD_heatsun_4 + PD_heater_4 + PPD_m_col_hot_4

Per_PD_elec_4 = PD_elec_4 / Per_t_4
Per_PD_draw_4 = PD_draw_4 / Per_t_4
Per_PD_coldfloor_4 = PD_coldfloor_4 / Per_t_4
Per_PD_heatsun_4 = PD_heatsun_4 / Per_t_4
Per_PD_heater_4 = PD_heater_4 / Per_t_4
Per_PPD_m_col_hot_4 = PPD_m_col_hot_4 / Per_t_4


Per_ta_4 = PD_smell4 + PD_heavy4 + PD_dry4 + PD_dust4
Per_PD_smell4 = PD_smell4 / Per_ta_4
Per_PD_heavy4 = PD_heavy4 / Per_ta_4
Per_PD_dry4 = PD_dry4 / Per_ta_4
Per_PD_dust4 = PD_dust4 / Per_ta_4

day5 = qns.iloc[254:323, 10]

day5B = day5.value_counts()[4]
print('Number of dissatisfied vote')
print(day5B)
day5P = day5.value_counts()[3]
print('Number of dissatisfied vote')
print(day5P)
t_5= 323 - 254
p_51 = (day5B/t_5) * 100
p_52 = (day5P/t_5) * 100
P_5 = p_51 + p_52

ACC5 = statistics.mean(qns.iloc[254:323, 9])
PD_air5 = (np.exp(-0.18 - 5.28 * ACC5))/(1 + np.exp(-0.18 - 5.28 * ACC5))  * 100
decipol_5 = 112 * (np.log (PD_air5)- 5.98)**(-4)
m_col_hot_5 = statistics.mean(qns.iloc[254:323, 19])
print(m_col_hot_5)


PD_elec_5 = (qns.iloc[254:323, 18].value_counts()[1]/(qns.iloc[254:323, 18].value_counts()[1]+qns.iloc[254:323, 18].value_counts()[0]))*100
PD_draw_5 = (qns.iloc[254:323, 20].value_counts()[1]/(qns.iloc[254:323, 20].value_counts()[1]+qns.iloc[254:323, 20].value_counts()[0]))*100
PD_coldfloor_5 = (qns.iloc[254:323, 21].value_counts()[1]/(qns.iloc[254:323, 21].value_counts()[1]+qns.iloc[254:323, 21].value_counts()[0]))*100
PD_heatsun_5 = (qns.iloc[254:323, 22].value_counts()[1]/(qns.iloc[254:323, 22].value_counts()[1]+qns.iloc[254:323, 22].value_counts()[0]))*100
PD_heater_5 = (qns.iloc[254:323, 23].value_counts()[1]/(qns.iloc[254:323, 23].value_counts()[1]+qns.iloc[254:323, 23].value_counts()[0]))*100

PPD_m_col_hot_5 = (100 - 95 * np.exp(-0.03353 * m_col_hot_5**4 - 0.2179 * m_col_hot_5**2))


PD_smell5 = (qns.iloc[254:323, 14].value_counts()[1]/(qns.iloc[254:323, 14].value_counts()[1]+qns.iloc[254:323, 14].value_counts()[0]))*100
PD_heavy5 = (qns.iloc[254:323, 15].value_counts()[1]/(qns.iloc[254:323, 15].value_counts()[1]+qns.iloc[254:323, 15].value_counts()[0]))*100
PD_dry5 = (qns.iloc[254:323, 16].value_counts()[1]/(qns.iloc[254:323, 16].value_counts()[1]+qns.iloc[254:323, 16].value_counts()[0]))*100
PD_dust5 = (qns.iloc[254:323, 17].value_counts()[1]/(qns.iloc[254:323, 17].value_counts()[1]+qns.iloc[254:323, 17].value_counts()[0]))*100


Per_ta_5 = PD_smell5 + PD_heavy5 + PD_dry5 + PD_dust5
Per_PD_smell5 = PD_smell5 / Per_ta_5
Per_PD_heavy5 = PD_heavy5 / Per_ta_5
Per_PD_dry5 = PD_dry5 / Per_ta_5
Per_PD_dust5 = PD_dust5 / Per_ta_5

Per_t_5 = PD_elec_5 + PD_draw_5 + PD_coldfloor_5 + PD_heatsun_5 + PD_heater_5 + PPD_m_col_hot_5
Per_PD_elec_5 = PD_elec_5 / Per_t_5
Per_PD_draw_5 = PD_draw_5 / Per_t_5
Per_PD_coldfloor_5 = PD_coldfloor_5 / Per_t_5
Per_PD_heatsun_5 = PD_heatsun_5 / Per_t_5
Per_PD_heater_5 = PD_heater_5 / Per_t_5
Per_PPD_m_col_hot_5 = PPD_m_col_hot_5 / Per_t_5

day6 = qns.iloc[324:370, 10]

day6B = day6.value_counts()[4]
print('Number of dissatisfied vote')
print(day6B)
day6P = day6.value_counts()[3]
print('Number of dissatisfied vote')
print(day6P)
t_6= 370 - 324
p_61 = (day6B/t_6) * 100
p_62 = (day6P/t_6) * 100
P_6 = p_61 + p_62

ACC6 = statistics.mean(qns.iloc[324:370, 9])
PD_air6 = (np.exp(-0.18 - 5.28 * ACC6))/(1 + np.exp(-0.18 - 5.28 * ACC6))  * 100
decipol_6 = 112 * (np.log (PD_air6)- 5.98)**(-4)


m_col_hot_6 = statistics.mean(qns.iloc[324:370, 19])


PD_elec_6 = 0
PD_draw_6 = 0
PD_coldfloor_6 = (qns.iloc[324:370, 21].value_counts()[1]/(qns.iloc[324:370, 21].value_counts()[1]+qns.iloc[324:370, 21].value_counts()[0]))*100
PD_heatsun_6 = (qns.iloc[324:370, 22].value_counts()[1]/(qns.iloc[324:370, 22].value_counts()[1]+qns.iloc[324:370, 22].value_counts()[0]))*100
PD_heater_6 = (qns.iloc[324:370, 23].value_counts()[1]/(qns.iloc[324:370, 23].value_counts()[1]+qns.iloc[324:370, 23].value_counts()[0]))*100
PPD_m_col_hot_6 = (100 - 95 * np.exp(-0.03353 * m_col_hot_6**4 - 0.2179 * m_col_hot_6**2))


PD_smell6 = (qns.iloc[324:370, 14].value_counts()[1]/(qns.iloc[324:370, 14].value_counts()[1]+qns.iloc[324:370, 14].value_counts()[0]))*100
PD_heavy6 = (qns.iloc[324:370, 15].value_counts()[1]/(qns.iloc[324:370, 15].value_counts()[1]+qns.iloc[324:370, 15].value_counts()[0]))*100
PD_dry6 = (qns.iloc[324:370, 16].value_counts()[1]/(qns.iloc[324:370, 16].value_counts()[1]+qns.iloc[324:370, 16].value_counts()[0]))*100
PD_dust6 = (qns.iloc[324:370, 17].value_counts()[1]/(qns.iloc[324:370, 17].value_counts()[1]+qns.iloc[324:370, 17].value_counts()[0]))*100


Per_t_6 = PD_elec_6 + PD_draw_6 + PD_coldfloor_6 + PD_heatsun_6 + PD_heater_6 + PPD_m_col_hot_6
Per_PD_elec_6 = PD_elec_6 / Per_t_6
Per_PD_draw_6 = PD_draw_6 / Per_t_6
Per_PD_coldfloor_6 = PD_coldfloor_6 / Per_t_6
Per_PD_heatsun_6 = PD_heatsun_6 / Per_t_6
Per_PD_heater_6 = PD_heater_6 / Per_t_6
Per_PPD_m_col_hot_6 = PPD_m_col_hot_6 / Per_t_6

Per_ta_6 = PD_smell6 + PD_heavy6 + PD_dry6 + PD_dust6
Per_PD_smell6 = PD_smell6 / Per_ta_6
Per_PD_heavy6 = PD_heavy6 / Per_ta_6
Per_PD_dry6 = PD_dry6 / Per_ta_6
Per_PD_dust6 = PD_dust6 / Per_ta_6


day7 = qns.iloc[371:422, 10]

day7B = day7.value_counts()[4]
print('Number of dissatisfied vote')
print(day7B)
day7P = day7.value_counts()[3]
print('Number of dissatisfied vote')
print(day7P)
t_7= 422 - 371
p_71 = (day7B/t_7) * 100
p_72 = (day7P/t_7) * 100
P_7 = p_71 + p_72

ACC7 = statistics.mean(qns.iloc[371:422, 9])
PD_air7 = (np.exp(-0.18 - 5.28 * ACC7))/(1 + np.exp(-0.18 - 5.28 * ACC7))  * 100
decipol_7 = 112 * (np.log (PD_air7)- 5.98)**(-4)
m_col_hot_7 = statistics.mean(qns.iloc[371:422, 19])
print(m_col_hot_7)



PD_elec_7 = (qns.iloc[371:422, 18].value_counts()[1]/(qns.iloc[371:422, 18].value_counts()[1]+qns.iloc[371:422, 18].value_counts()[0]))*100
PD_draw_7 = (qns.iloc[371:422, 20].value_counts()[1]/(qns.iloc[371:422, 20].value_counts()[1]+qns.iloc[371:422, 20].value_counts()[0]))*100
PD_coldfloor_7 = (qns.iloc[371:422, 21].value_counts()[1]/(qns.iloc[371:422, 21].value_counts()[1]+qns.iloc[371:422, 21].value_counts()[0]))*100
PD_heatsun_7 = 0
PD_heater_7 = (qns.iloc[371:422, 23].value_counts()[1]/(qns.iloc[371:422, 23].value_counts()[1]+qns.iloc[371:422, 23].value_counts()[0]))*100
PPD_m_col_hot_7 = (100 - 95 * np.exp(-0.03353 * m_col_hot_7 **4 - 0.2179 * m_col_hot_7 **2))

PD_smell7 = 0
PD_heavy7 = (qns.iloc[371:422, 15].value_counts()[1]/(qns.iloc[371:422, 15].value_counts()[1]+qns.iloc[371:422, 15].value_counts()[0]))*100
PD_dry7 = (qns.iloc[371:422, 16].value_counts()[1]/(qns.iloc[371:422, 16].value_counts()[1]+qns.iloc[371:422, 16].value_counts()[0]))*100
PD_dust7 = (qns.iloc[371:422, 17].value_counts()[1]/(qns.iloc[371:422, 17].value_counts()[1]+qns.iloc[371:422, 17].value_counts()[0]))*100


Per_t_7 = PD_elec_7 + PD_draw_7 + PD_coldfloor_7 + PD_heatsun_7 + PD_heater_7 + PPD_m_col_hot_7
Per_PD_elec_7 = PD_elec_7 / Per_t_7
Per_PD_draw_7 = PD_draw_7 / Per_t_7
Per_PD_coldfloor_7 = PD_coldfloor_7 / Per_t_7
Per_PD_heatsun_7 = PD_heatsun_7 / Per_t_7
Per_PD_heater_7 = PD_heater_7 / Per_t_7
Per_PPD_m_col_hot_7 = PPD_m_col_hot_7 / Per_t_7

Per_ta_7 = PD_smell7 + PD_heavy7 + PD_dry7 + PD_dust7
Per_PD_smell7 = PD_smell7 / Per_ta_7
Per_PD_heavy7 = PD_heavy7 / Per_ta_7
Per_PD_dry7 = PD_dry7 / Per_ta_7
Per_PD_dust7 = PD_dust7 / Per_ta_7


day8 = qns.iloc[423:459, 10]

day8B = day8.value_counts()[4]
print('Number of dissatisfied vote')
print(day8B)
day8P = day8.value_counts()[3]
print('Number of dissatisfied vote')
print(day8P)
t_8= 459 - 423
p_81 = (day8B/t_8) * 100
p_82 = (day8P/t_8) * 100
P_8 = p_81 + p_82


ACC8 = statistics.mean(qns.iloc[423:459, 9])
PD_air8 = (np.exp(-0.18 - 5.28 * ACC8))/(1 + np.exp(-0.18 - 5.28 * ACC8))  * 100
decipol_8 = 112 * (np.log (PD_air8)- 5.98)**(-4)
PD_elec_8 = (qns.iloc[423:459, 18].value_counts()[1]/(qns.iloc[423:459, 18].value_counts()[1]+qns.iloc[423:459, 18].value_counts()[0]))*100
PD_draw_8 = (qns.iloc[423:459, 20].value_counts()[1]/(qns.iloc[423:459, 20].value_counts()[1]+qns.iloc[423:459, 20].value_counts()[0]))*100
PD_coldfloor_8 = (qns.iloc[423:459, 21].value_counts()[1]/(qns.iloc[423:459, 21].value_counts()[1]+qns.iloc[423:459, 21].value_counts()[0]))*100
PD_heatsun_8 = (qns.iloc[423:459, 22].value_counts()[1]/(qns.iloc[423:459, 22].value_counts()[1]+qns.iloc[423:459, 22].value_counts()[0]))*100
PD_heater_8 = (qns.iloc[423:459, 23].value_counts()[1]/(qns.iloc[423:459, 23].value_counts()[1]+qns.iloc[423:459, 23].value_counts()[0]))*100



m_col_hot_8 = statistics.mean(qns.iloc[423:459, 19])
print(m_col_hot_8)



PD_smell8 = (qns.iloc[423:459, 14].value_counts()[1]/(qns.iloc[423:459, 14].value_counts()[1]+qns.iloc[423:459, 14].value_counts()[0]))*100
PD_heavy8 = (qns.iloc[423:459, 15].value_counts()[1]/(qns.iloc[423:459, 15].value_counts()[1]+qns.iloc[423:459, 15].value_counts()[0]))*100
PD_dry8 = (qns.iloc[423:459, 16].value_counts()[1]/(qns.iloc[423:459, 16].value_counts()[1]+qns.iloc[423:459, 16].value_counts()[0]))*100
PD_dust8 = (qns.iloc[423:459, 17].value_counts()[1]/(qns.iloc[423:459, 17].value_counts()[1]+qns.iloc[423:459, 17].value_counts()[0]))*100




PPD_m_col_hot_8 = (100 - 95 * np.exp(-0.03353 * m_col_hot_8 **4 - 0.2179 * m_col_hot_8 **2))
Per_t_8 = PD_elec_8 + PD_draw_8 + PD_coldfloor_8 + PD_heatsun_8 + PD_heater_8 + PPD_m_col_hot_8
Per_PD_elec_8 = PD_elec_8 / Per_t_8
Per_PD_draw_8 = PD_draw_8 / Per_t_8
Per_PD_coldfloor_8 = PD_coldfloor_8 / Per_t_8
Per_PD_heatsun_8 = PD_heatsun_8 / Per_t_8
Per_PD_heater_8 = PD_heater_8 / Per_t_8
Per_PPD_m_col_hot_8 = PPD_m_col_hot_8 / Per_t_8

Per_ta_8 = PD_smell8 + PD_heavy8 + PD_dry8 + PD_dust8
Per_PD_smell8 = PD_smell8 / Per_ta_8
Per_PD_heavy8 = PD_heavy8 / Per_ta_8
Per_PD_dry8 = PD_dry8 / Per_ta_8
Per_PD_dust8 = PD_dust8 / Per_ta_8

day9 = qns.iloc[460:501, 10]

day9B = day9.value_counts()[4]
print('Number of dissatisfied vote')
print(day9B)
day9P = day9.value_counts()[3]
print('Number of dissatisfied vote')
print(day9P)
t_9= 501 - 460
p_91 = (day9B/t_9) * 100
p_92 = (day9P/t_9) * 100
P_9 = p_91 + p_92


ACC9 = statistics.mean(qns.iloc[460:501, 9])
PD_air9 = (np.exp(-0.18 - 5.28 * ACC9))/(1 + np.exp(-0.18 - 5.28 * ACC9))  * 100
decipol_9 = 112 * (np.log (PD_air9)- 5.98)**(-4)
PD_elec_9 = (qns.iloc[460:501, 18].value_counts()[1]/(qns.iloc[460:501, 18].value_counts()[1]+qns.iloc[460:501, 18].value_counts()[0]))*100
PD_draw_9 = (qns.iloc[460:501, 20].value_counts()[1]/(qns.iloc[460:501, 20].value_counts()[1]+qns.iloc[460:501, 20].value_counts()[0]))*100
PD_coldfloor_9 = (qns.iloc[460:501, 21].value_counts()[1]/(qns.iloc[460:501, 21].value_counts()[1]+qns.iloc[460:501, 21].value_counts()[0]))*100
PD_heatsun_9 = (qns.iloc[460:501, 22].value_counts()[1]/(qns.iloc[460:501, 22].value_counts()[1]+qns.iloc[460:501, 22].value_counts()[0]))*100
PD_heater_9 = (qns.iloc[460:501, 23].value_counts()[1]/(qns.iloc[460:501, 23].value_counts()[1]+qns.iloc[460:501, 23].value_counts()[0]))*100



m_col_hot_9 = statistics.mean(qns.iloc[460:501, 19])
print(m_col_hot_9)


PD_smell9 = (qns.iloc[460:501, 14].value_counts()[1]/(qns.iloc[460:501, 14].value_counts()[1]+qns.iloc[460:501, 14].value_counts()[0]))*100
PD_heavy9 = (qns.iloc[460:501, 15].value_counts()[1]/(qns.iloc[460:501, 15].value_counts()[1]+qns.iloc[460:501, 15].value_counts()[0]))*100
PD_dry9 = (qns.iloc[460:501, 16].value_counts()[1]/(qns.iloc[460:501, 16].value_counts()[1]+qns.iloc[460:501, 16].value_counts()[0]))*100
PD_dust9 = (qns.iloc[460:501, 17].value_counts()[1]/(qns.iloc[460:501, 17].value_counts()[1]+qns.iloc[460:501, 17].value_counts()[0]))*100




PPD_m_col_hot_9 = (100 - 95 * np.exp(-0.03353 * m_col_hot_9 **4 - 0.2179 * m_col_hot_9 **2))
Per_t_9 = PD_elec_9 + PD_draw_9 + PD_coldfloor_9 + PD_heatsun_9 + PD_heater_9 + PPD_m_col_hot_9
Per_PD_elec_9 = PD_elec_9 / Per_t_9
Per_PD_draw_9 = PD_draw_9 / Per_t_9
Per_PD_coldfloor_9 = PD_coldfloor_9 / Per_t_9
Per_PD_heatsun_9 = PD_heatsun_9 / Per_t_9
Per_PD_heater_9 = PD_heater_9 / Per_t_9
Per_PPD_m_col_hot_9 = PPD_m_col_hot_9 / Per_t_9

Per_ta_9 = PD_smell9 + PD_heavy9 + PD_dry9 + PD_dust9
Per_PD_smell9 = PD_smell9 / Per_ta_9
Per_PD_heavy9 = PD_heavy9 / Per_ta_9
Per_PD_dry9 = PD_dry9 / Per_ta_9
Per_PD_dust9 = PD_dust9 / Per_ta_9

day10 = qns.iloc[502:538, 10]

day10B = day10.value_counts()[4]
print('Number of dissatisfied vote')
print(day10B)
day10P = day10.value_counts()[3]
print('Number of dissatisfied vote')
print(day10P)
t_10= 538 - 502
p_101 = (day10B/t_10) * 100
p_102 = (day10P/t_10) * 100
P_10 = p_101 + p_102

ACC10 = statistics.mean(qns.iloc[502:538, 9])
PD_air10 = (np.exp(-0.18 - 5.28 * ACC10))/(1 + np.exp(-0.18 - 5.28 * ACC10))  * 100
decipol_10 = 112 * (np.log (PD_air10)- 5.98)**(-4)
m_col_hot_10 = statistics.mean(qns.iloc[502:538, 19])
print(m_col_hot_10)


PD_elec_10 = 0
PD_draw_10 = (qns.iloc[502:538, 20].value_counts()[1]/(qns.iloc[502:538, 20].value_counts()[1]+qns.iloc[502:538, 20].value_counts()[0]))*100
PD_coldfloor_10 = (qns.iloc[502:538, 21].value_counts()[1]/(qns.iloc[502:538, 21].value_counts()[1]+qns.iloc[502:538, 21].value_counts()[0]))*100
PD_heatsun_10 = (qns.iloc[502:538, 22].value_counts()[1]/(qns.iloc[502:538, 22].value_counts()[1]+qns.iloc[502:538, 22].value_counts()[0]))*100
PD_heater_10 = (qns.iloc[502:538, 23].value_counts()[1]/(qns.iloc[502:538, 23].value_counts()[1]+qns.iloc[502:538, 23].value_counts()[0]))*100


PD_smell10 = 0
PD_heavy10 = (qns.iloc[502:538, 15].value_counts()[1]/(qns.iloc[502:538, 15].value_counts()[1]+qns.iloc[502:538, 15].value_counts()[0]))*100
PD_dry10 = (qns.iloc[502:538, 16].value_counts()[1]/(qns.iloc[502:538, 16].value_counts()[1]+qns.iloc[502:538, 16].value_counts()[0]))*100
PD_dust10 = (qns.iloc[502:538, 17].value_counts()[1]/(qns.iloc[502:538, 17].value_counts()[1]+qns.iloc[502:538, 17].value_counts()[0]))*100




PPD_m_col_hot_10 = (100 - 95 * np.exp(-0.03353 * m_col_hot_10 **4 - 0.2179 * m_col_hot_10 **2))
Per_t_10 = PD_elec_10 + PD_draw_10 + PD_coldfloor_10 + PD_heatsun_10 + PD_heater_10 + PPD_m_col_hot_10
Per_PD_elec_10 = PD_elec_10 / Per_t_10
Per_PD_draw_10 = PD_draw_10 / Per_t_10
Per_PD_coldfloor_10 = PD_coldfloor_10 / Per_t_10
Per_PD_heatsun_10 = PD_heatsun_10 / Per_t_10
Per_PD_heater_10 = PD_heater_10 / Per_t_10
Per_PPD_m_col_hot_10 = PPD_m_col_hot_10 / Per_t_10


Per_ta_10 = PD_smell10 + PD_heavy10 + PD_dry10 + PD_dust10
Per_PD_smell10 = PD_smell10 / Per_ta_10
Per_PD_heavy10 = PD_heavy10 / Per_ta_10
Per_PD_dry10 = PD_dry10 / Per_ta_10
Per_PD_dust10 = PD_dust10 / Per_ta_10

day11 = qns.iloc[539:586, 10]

day11B = day11.value_counts()[4]
print('Number of dissatisfied vote')
print(day11B)
day11P = day11.value_counts()[3]
print('Number of dissatisfied vote')
print(day11P)
t_11= 539-586
p_111 = (day11B/t_11) * 100
p_112 = (day11P/t_11) * 100
P_11 = p_111 + p_112


ACC11 = statistics.mean(qns.iloc[539:586, 9])
PD_air11 = (np.exp(-0.18 - 5.28 * ACC11))/(1 + np.exp(-0.18 - 5.28 * ACC11))  * 100
decipol_11 = 112 * (np.log (PD_air11)- 5.98)**(-4)
PD_elec_11 = (qns.iloc[539:586, 18].value_counts()[1]/(qns.iloc[539:586, 18].value_counts()[1]+qns.iloc[539:586, 18].value_counts()[0]))*100
PD_draw_11 = (qns.iloc[539:586, 20].value_counts()[1]/(qns.iloc[539:586, 20].value_counts()[1]+qns.iloc[539:586, 20].value_counts()[0]))*100
PD_coldfloor_11 = (qns.iloc[539:586, 21].value_counts()[1]/(qns.iloc[539:586, 21].value_counts()[1]+qns.iloc[539:586, 21].value_counts()[0]))*100
PD_heatsun_11 = (qns.iloc[539:586, 22].value_counts()[1]/(qns.iloc[539:586, 22].value_counts()[1]+qns.iloc[539:586, 22].value_counts()[0]))*100
PD_heater_11 = (qns.iloc[539:586, 23].value_counts()[1]/(qns.iloc[539:586, 23].value_counts()[1]+qns.iloc[539:586, 23].value_counts()[0]))*100



m_col_hot_11 = statistics.mean(qns.iloc[539:586, 19])
print(m_col_hot_11)



PPD_m_col_hot_11 = (100 - 95 * np.exp(-0.03353 * m_col_hot_11 **4 - 0.2179 * m_col_hot_11 **2))

PD_smell11 = (qns.iloc[539:586, 14].value_counts()[1]/(qns.iloc[539:586, 14].value_counts()[1]+qns.iloc[539:586, 14].value_counts()[0]))*100
PD_heavy11 = (qns.iloc[539:586, 15].value_counts()[1]/(qns.iloc[539:586, 15].value_counts()[1]+qns.iloc[539:586, 15].value_counts()[0]))*100
PD_dry11 = (qns.iloc[539:586, 16].value_counts()[1]/(qns.iloc[539:586, 16].value_counts()[1]+qns.iloc[539:586, 16].value_counts()[0]))*100
PD_dust11 = (qns.iloc[539:586, 17].value_counts()[1]/(qns.iloc[539:586, 17].value_counts()[1]+qns.iloc[539:586, 17].value_counts()[0]))*100


Per_ta_11 = PD_smell11 + PD_heavy11 + PD_dry11 + PD_dust11
Per_PD_smell11 = PD_smell11 / Per_ta_11
Per_PD_heavy11 = PD_heavy11 / Per_ta_11
Per_PD_dry11 = PD_dry11 / Per_ta_11
Per_PD_dust11 = PD_dust11 / Per_ta_11


PD_smell11 = (qns.iloc[539:586, 14].value_counts()[1]/(qns.iloc[539:586, 14].value_counts()[1]+qns.iloc[539:586, 14].value_counts()[0]))*100
PD_heavy11 = (qns.iloc[539:586, 15].value_counts()[1]/(qns.iloc[539:586, 15].value_counts()[1]+qns.iloc[539:586, 15].value_counts()[0]))*100
PD_dry11 = (qns.iloc[539:586, 16].value_counts()[1]/(qns.iloc[539:586, 16].value_counts()[1]+qns.iloc[539:586, 16].value_counts()[0]))*100
PD_dust11 = (qns.iloc[539:586, 17].value_counts()[1]/(qns.iloc[539:586, 17].value_counts()[1]+qns.iloc[539:586, 17].value_counts()[0]))*100



Per_t_11 = PD_elec_11 + PD_draw_11 + PD_coldfloor_11 + PD_heatsun_11 + PD_heater_11 + PPD_m_col_hot_11
Per_PD_elec_11 = PD_elec_11 / Per_t_11
Per_PD_draw_11 = PD_draw_11 / Per_t_11
Per_PD_coldfloor_11 = PD_coldfloor_11 / Per_t_11
Per_PD_heatsun_11 = PD_heatsun_11 / Per_t_11
Per_PD_heater_11 = PD_heater_11 / Per_t_11
Per_PPD_m_col_hot_11 = PPD_m_col_hot_11 / Per_t_11

day12 = qns.iloc[587:628, 10]

day12B = day12.value_counts()[4]
print('Number of dissatisfied vote')
print(day12B)
day12P = day12.value_counts()[3]
print('Number of dissatisfied vote')
print(day12P)
t_12 = 628 - 587
p_121 = (day12B/t_12) * 100
p_122 = (day12P/t_12) * 100
P_12 = p_121 + p_122

ACC12 = statistics.mean(qns.iloc[587:628, 9])
PD_air12 = (np.exp(-0.18 - 5.28 * ACC12))/(1 + np.exp(-0.18 - 5.28 * ACC12))  * 100
decipol_12 = 112 * (np.log (PD_air12)- 5.98)**(-4)
PD_elec_12 = (qns.iloc[587:628, 18].value_counts()[1]/(qns.iloc[587:628, 18].value_counts()[1]+qns.iloc[587:628, 18].value_counts()[0]))*100
PD_draw_12 = (qns.iloc[587:628, 20].value_counts()[1]/(qns.iloc[587:628, 20].value_counts()[1]+qns.iloc[587:628, 20].value_counts()[0]))*100
PD_coldfloor_12 = (qns.iloc[587:628, 21].value_counts()[1]/(qns.iloc[587:628, 21].value_counts()[1]+qns.iloc[587:628, 21].value_counts()[0]))*100
PD_heatsun_12 = (qns.iloc[587:628, 22].value_counts()[1]/(qns.iloc[587:628, 22].value_counts()[1]+qns.iloc[587:628, 22].value_counts()[0]))*100
PD_heater_12 = (qns.iloc[587:628, 23].value_counts()[1]/(qns.iloc[587:628, 23].value_counts()[1]+qns.iloc[587:628, 23].value_counts()[0]))*100


m_col_hot_12 = statistics.mean(qns.iloc[587:628, 19])


PPD_m_col_hot_12 = (100 - 95 * np.exp(-0.03353 * m_col_hot_12 **4 - 0.2179 * m_col_hot_12 **2))


PD_smell12 = (qns.iloc[587:628, 14].value_counts()[1]/(qns.iloc[587:628, 14].value_counts()[1]+qns.iloc[587:628, 14].value_counts()[0]))*100
PD_heavy12 = (qns.iloc[587:628, 15].value_counts()[1]/(qns.iloc[587:628, 15].value_counts()[1]+qns.iloc[587:628, 15].value_counts()[0]))*100
PD_dry12 = (qns.iloc[587:628, 16].value_counts()[1]/(qns.iloc[587:628, 16].value_counts()[1]+qns.iloc[587:628, 16].value_counts()[0]))*100
PD_dust12 = (qns.iloc[587:628, 17].value_counts()[1]/(qns.iloc[587:628, 17].value_counts()[1]+qns.iloc[587:628, 17].value_counts()[0]))*100

Per_ta_12 = PD_smell12 + PD_heavy12 + PD_dry12 + PD_dust12
Per_PD_smell12 = PD_smell12 / Per_ta_12
Per_PD_heavy12 = PD_heavy12 / Per_ta_12
Per_PD_dry12 = PD_dry12 / Per_ta_12
Per_PD_dust12 = PD_dust12 / Per_ta_12

Per_t_12 = PD_elec_12 + PD_draw_12 + PD_coldfloor_12 + PD_heatsun_12 + PD_heater_12 + PPD_m_col_hot_12
Per_PD_elec_12 = PD_elec_12 / Per_t_12
Per_PD_draw_12 = PD_draw_12 / Per_t_12
Per_PD_coldfloor_12 = PD_coldfloor_12 / Per_t_12
Per_PD_heatsun_12 = PD_heatsun_12 / Per_t_12
Per_PD_heater_12 = PD_heater_12 / Per_t_12
Per_PPD_m_col_hot_12 = PPD_m_col_hot_12 / Per_t_12

day13 = qns.iloc[629:664, 10]

day13B = day13.value_counts()[4]
print('Number of dissatisfied vote')
print(day13B)
day13P = day13.value_counts()[3]
print('Number of dissatisfied vote')
print(day13P)
t_13 = 664 - 629
p_131 = (day13B/t_13) * 100
p_132 = (day13P/t_13) * 100
P_13 = p_131 + p_132


ACC13 = statistics.mean(qns.iloc[629:664, 9])
PD_air13 = (np.exp(-0.18 - 5.28 * ACC13))/(1 + np.exp(-0.18 - 5.28 * ACC13))  * 100
decipol_13 = 112 * (np.log (PD_air13)- 5.98)**(-4)

PD_elec_13 = 0
PD_draw_13 = (qns.iloc[629:664, 20].value_counts()[1]/(qns.iloc[629:664, 20].value_counts()[1]+qns.iloc[629:664, 20].value_counts()[0]))*100
PD_coldfloor_13 = 0
PD_heatsun_13 = 0
PD_heater_13 = (qns.iloc[629:664, 23].value_counts()[1]/(qns.iloc[629:664, 23].value_counts()[1]+qns.iloc[629:664, 23].value_counts()[0]))*100


m_col_hot_13 = statistics.mean(qns.iloc[629:664, 19])
print(m_col_hot_13)


PPD_m_col_hot_13 = (100 - 95 * np.exp(-0.03353 * m_col_hot_13 **4 - 0.2179 * m_col_hot_13 **2))


PD_smell13 = 0
PD_heavy13 = 0
PD_dry13 = 0
PD_dust13 = (qns.iloc[629:664, 17].value_counts()[1]/(qns.iloc[629:664, 17].value_counts()[1]+qns.iloc[629:664, 17].value_counts()[0]))*100

Per_ta_13 = PD_smell13 + PD_heavy13 + PD_dry13 + PD_dust13
Per_PD_smell13 = PD_smell13 / Per_ta_13
Per_PD_heavy13 = PD_heavy13 / Per_ta_13
Per_PD_dry13 = PD_dry13 / Per_ta_13
Per_PD_dust13 = PD_dust13 / Per_ta_13

Per_t_13 = PD_elec_13 + PD_draw_13 + PD_coldfloor_13 + PD_heatsun_13 + PD_heater_13 + PPD_m_col_hot_13
Per_PD_elec_13 = PD_elec_13 / Per_t_13
Per_PD_draw_13 = PD_draw_13 / Per_t_13
Per_PD_coldfloor_13 = PD_coldfloor_13 / Per_t_13
Per_PD_heatsun_13 = PD_heatsun_13 / Per_t_13
Per_PD_heater_13 = PD_heater_13 / Per_t_13
Per_PPD_m_col_hot_13 = PPD_m_col_hot_13 / Per_t_13

day14 = qns.iloc[665:710, 10]

day14B = day14.value_counts()[4]
print('Number of dissatisfied vote')
print(day14B)
day14P = day14.value_counts()[3]
print('Number of dissatisfied vote')
print(day14P)
t_14 = 710 - 665
p_141 = (day14B/t_14) * 100
p_142 = (day14P/t_14) * 100
P_14 = p_141 + p_142


ACC14 = statistics.mean(qns.iloc[665:710, 9])
PD_air14 = (np.exp(-0.18 - 5.28 * ACC14))/(1 + np.exp(-0.18 - 5.28 * ACC14))  * 100
decipol_14 = 112 * (np.log (PD_air14)- 5.98)**(-4)
PD_elec_14 = (qns.iloc[665:710, 18].value_counts()[1]/(qns.iloc[665:710, 18].value_counts()[1]+qns.iloc[665:710, 18].value_counts()[0]))*100
PD_draw_14 = (qns.iloc[665:710, 20].value_counts()[1]/(qns.iloc[665:710, 20].value_counts()[1]+qns.iloc[665:710, 20].value_counts()[0]))*100
PD_coldfloor_14 = (qns.iloc[665:710, 21].value_counts()[1]/(qns.iloc[665:710, 21].value_counts()[1]+qns.iloc[665:710, 21].value_counts()[0]))*100
PD_heatsun_14 = (qns.iloc[665:710, 22].value_counts()[1]/(qns.iloc[665:710, 22].value_counts()[1]+qns.iloc[665:710, 22].value_counts()[0]))*100
PD_heater_14 = (qns.iloc[665:710, 23].value_counts()[1]/(qns.iloc[665:710, 23].value_counts()[1]+qns.iloc[665:710, 23].value_counts()[0]))*100




m_col_hot_14 = statistics.mean(qns.iloc[665:710, 19])
print(m_col_hot_14)


PPD_m_col_hot_14 = (100 - 95 * np.exp(-0.03353 * m_col_hot_14 **4 - 0.2179 * m_col_hot_14 **2))

PD_smell14 = (qns.iloc[665:710, 14].value_counts()[1]/(qns.iloc[665:710, 14].value_counts()[1]+qns.iloc[665:710, 14].value_counts()[0]))*100
PD_heavy14 = (qns.iloc[665:710, 15].value_counts()[1]/(qns.iloc[665:710, 15].value_counts()[1]+qns.iloc[665:710, 15].value_counts()[0]))*100
PD_dry14 = (qns.iloc[665:710, 16].value_counts()[1]/(qns.iloc[665:710, 16].value_counts()[1]+qns.iloc[665:710, 16].value_counts()[0]))*100
PD_dust14 = (qns.iloc[665:710, 17].value_counts()[1]/(qns.iloc[665:710, 17].value_counts()[1]+qns.iloc[665:710, 17].value_counts()[0]))*100


Per_ta_14 = PD_smell14 + PD_heavy14 + PD_dry14 + PD_dust14
Per_PD_smell14 = PD_smell14 / Per_ta_14
Per_PD_heavy14 = PD_heavy14 / Per_ta_14
Per_PD_dry14 = PD_dry14 / Per_ta_14
Per_PD_dust14 = PD_dust14 / Per_ta_14

Per_t_14 = PD_elec_14 + PD_draw_14 + PD_coldfloor_14 + PD_heatsun_14 + PD_heater_14 + PPD_m_col_hot_14
Per_PD_elec_14 = PD_elec_14 / Per_t_14
Per_PD_draw_14 = PD_draw_14 / Per_t_14
Per_PD_coldfloor_14 = PD_coldfloor_14 / Per_t_14
Per_PD_heatsun_14 = PD_heatsun_14 / Per_t_14
Per_PD_heater_14 = PD_heater_14 / Per_t_14
Per_PPD_m_col_hot_14 = PPD_m_col_hot_14 / Per_t_14




day15 = qns.iloc[711:760, 10]

day15B = day15.value_counts()[4]
print('Number of dissatisfied vote')
print(day15B)
day15P = day15.value_counts()[3]
print('Number of dissatisfied vote')
print(day15P)
t_15 = 760 - 711
p_151 = (day15B/t_15) * 100
p_152 = (day15P/t_15) * 100
P_15 = p_151 + p_152

ACC15 = statistics.mean(qns.iloc[711:760, 9])
PD_air15 = (np.exp(-0.18 - 5.28 * ACC15))/(1 + np.exp(-0.18 - 5.28 * ACC15))  * 100
decipol_15 = 112 * (np.log (PD_air15)- 5.98)**(-4)
PD_elec_15 = (qns.iloc[711:760, 18].value_counts()[1]/(qns.iloc[711:760, 18].value_counts()[1]+qns.iloc[711:760, 18].value_counts()[0]))*100
PD_draw_15 = (qns.iloc[711:760, 20].value_counts()[1]/(qns.iloc[711:760, 20].value_counts()[1]+qns.iloc[711:760, 20].value_counts()[0]))*100
PD_coldfloor_15 = (qns.iloc[711:760, 21].value_counts()[1]/(qns.iloc[711:760, 21].value_counts()[1]+qns.iloc[711:760, 21].value_counts()[0]))*100
PD_heatsun_15 = (qns.iloc[711:760, 22].value_counts()[1]/(qns.iloc[711:760, 22].value_counts()[1]+qns.iloc[711:760, 22].value_counts()[0]))*100
PD_heater_15 = (qns.iloc[711:760, 23].value_counts()[1]/(qns.iloc[711:760, 23].value_counts()[1]+qns.iloc[711:760, 23].value_counts()[0]))*100




m_col_hot_15 = statistics.mean(qns.iloc[711:760, 19])
print(m_col_hot_15)

PPD_m_col_hot_15 = (100 - 95 * np.exp(-0.03353 * m_col_hot_15 **4 - 0.2179 * m_col_hot_15 **2))



PD_smell15 = (qns.iloc[711:760, 14].value_counts()[1]/(qns.iloc[711:760, 14].value_counts()[1]+qns.iloc[711:760, 14].value_counts()[0]))*100
PD_heavy15 = (qns.iloc[711:760, 15].value_counts()[1]/(qns.iloc[711:760, 15].value_counts()[1]+qns.iloc[711:760, 15].value_counts()[0]))*100
PD_dry15 = (qns.iloc[711:760, 16].value_counts()[1]/(qns.iloc[711:760, 16].value_counts()[1]+qns.iloc[711:760, 16].value_counts()[0]))*100
PD_dust15 = (qns.iloc[711:760, 17].value_counts()[1]/(qns.iloc[711:760, 17].value_counts()[1]+qns.iloc[711:760, 17].value_counts()[0]))*100


Per_ta_15 = PD_smell15 + PD_heavy15 + PD_dry15 + PD_dust15
Per_PD_smell15 = PD_smell15 / Per_ta_15
Per_PD_heavy15 = PD_heavy15 / Per_ta_15
Per_PD_dry15 = PD_dry15 / Per_ta_15
Per_PD_dust15 = PD_dust15 / Per_ta_15

Per_t_15 = PD_elec_15 + PD_draw_15 + PD_coldfloor_15 + PD_heatsun_15 + PD_heater_15 + PPD_m_col_hot_15
Per_PD_elec_15 = PD_elec_15 / Per_t_15
Per_PD_draw_15 = PD_draw_15 / Per_t_15
Per_PD_coldfloor_15 = PD_coldfloor_15 / Per_t_15
Per_PD_heatsun_15 = PD_heatsun_15 / Per_t_15
Per_PD_heater_15 = PD_heater_15 / Per_t_15
Per_PPD_m_col_hot_15 = PPD_m_col_hot_15 / Per_t_15


day16 = qns.iloc[761:809, 10]

day16B = day16.value_counts()[4]
print('Number of dissatisfied vote')
print(day16B)
day16P = day16.value_counts()[3]
print('Number of dissatisfied vote')
print(day16P)

t_16 = 809 - 761
p_161 = (day16B/t_16) * 100
p_162 = (day16P/t_16) * 100
P_16 = p_161 + p_162

ACC16 = statistics.mean(qns.iloc[761:809, 9])
PD_air16 = (np.exp(-0.18 - 5.28 * ACC16))/(1 + np.exp(-0.18 - 5.28 * ACC16))  * 100
decipol_16 = 112 * (np.log (PD_air16)- 5.98)**(-4)
PD_elec_16 = (qns.iloc[761:809, 18].value_counts()[1]/(qns.iloc[761:809, 18].value_counts()[1]+qns.iloc[761:809, 18].value_counts()[0]))*100
PD_draw_16 = (qns.iloc[761:809, 20].value_counts()[1]/(qns.iloc[761:809, 20].value_counts()[1]+qns.iloc[761:809, 20].value_counts()[0]))*100
PD_coldfloor_16 = (qns.iloc[761:809, 21].value_counts()[1]/(qns.iloc[761:809, 21].value_counts()[1]+qns.iloc[761:809, 21].value_counts()[0]))*100
PD_heatsun_16 = (qns.iloc[761:809, 22].value_counts()[1]/(qns.iloc[711:760, 22].value_counts()[1]+qns.iloc[761:809, 22].value_counts()[0]))*100
PD_heater_16 = (qns.iloc[761:809, 23].value_counts()[1]/(qns.iloc[711:760, 23].value_counts()[1]+qns.iloc[761:809, 23].value_counts()[0]))*100




m_col_hot_16 = statistics.mean(qns.iloc[665:710, 19])
print(m_col_hot_16)

PPD_m_col_hot_16 = (100 - 95 * np.exp(-0.03353 * m_col_hot_16 **4 - 0.2179 * m_col_hot_16 **2))



PD_smell16 = (qns.iloc[761:809, 14].value_counts()[1]/(qns.iloc[761:809, 14].value_counts()[1]+qns.iloc[761:809, 14].value_counts()[0]))*100
PD_heavy16 = (qns.iloc[761:809, 15].value_counts()[1]/(qns.iloc[761:809, 15].value_counts()[1]+qns.iloc[761:809, 15].value_counts()[0]))*100
PD_dry16 = (qns.iloc[761:809, 16].value_counts()[1]/(qns.iloc[761:809, 16].value_counts()[1]+qns.iloc[761:809, 16].value_counts()[0]))*100
PD_dust16 = (qns.iloc[761:809, 17].value_counts()[1]/(qns.iloc[761:809, 17].value_counts()[1]+qns.iloc[761:809, 17].value_counts()[0]))*100




Per_t_16 = PD_elec_16 + PD_draw_16 + PD_coldfloor_16 + PD_heatsun_16 + PD_heater_16 + PPD_m_col_hot_16
Per_PD_elec_16 = PD_elec_16 / Per_t_16
Per_PD_draw_16 = PD_draw_16 / Per_t_16
Per_PD_coldfloor_16 = PD_coldfloor_16 / Per_t_16
Per_PD_heatsun_16 = PD_heatsun_16 / Per_t_16
Per_PD_heater_16 = PD_heater_16 / Per_t_16
Per_PPD_m_col_hot_16 = PPD_m_col_hot_16 / Per_t_16

Per_ta_16 = PD_smell16 + PD_heavy16 + PD_dry16 + PD_dust16
Per_PD_smell16 = PD_smell16 / Per_ta_16
Per_PD_heavy16 = PD_heavy16 / Per_ta_16
Per_PD_dry16 = PD_dry16 / Per_ta_16
Per_PD_dust16 = PD_dust16 / Per_ta_16


po4 = [p_11,p_21,p_31,p_41,p_51,p_61,p_71,p_81,p_91,p_101,p_111,p_121,p_131,p_141,p_151,p_161]
print('the laddo')
print(po4)
po3 = [p_12,p_22,p_32,p_42,p_52,p_62,p_72,p_82,p_92,p_102,p_112,p_122,p_132,p_142,p_152,p_162]
print(po3)
pt = [P_1,P_2,P_3,P_4,P_5,P_6,P_7,P_8,P_9,P_10,P_11,P_12,P_13,P_14,P_15,P_16]
print(pt)

ele_p = [PD_elec_1,PD_elec_2,PD_elec_3,PD_elec_4,PD_elec_5,PD_elec_6,PD_elec_7,PD_elec_8,PD_elec_9,PD_elec_10,PD_elec_11,PD_elec_12,PD_elec_13,PD_elec_14,PD_elec_15,PD_elec_16]
col_hot_p = [PPD_m_col_hot_1, PPD_m_col_hot_2,PPD_m_col_hot_3,PPD_m_col_hot_4,PPD_m_col_hot_5,PPD_m_col_hot_6,PPD_m_col_hot_7,PPD_m_col_hot_8,PPD_m_col_hot_9,PPD_m_col_hot_10,PPD_m_col_hot_11,PPD_m_col_hot_12,PPD_m_col_hot_13,PPD_m_col_hot_14,PPD_m_col_hot_15,PPD_m_col_hot_16]
draw_p = [PD_draw_1,PD_draw_2,PD_draw_3,PD_draw_4,PD_draw_5,PD_draw_6,PD_draw_7,PD_draw_8,PD_draw_9,PD_draw_10,PD_draw_11,PD_draw_12,PD_draw_13,PD_draw_14,PD_draw_15,PD_draw_16]
fcold_p = [PD_coldfloor_1,PD_coldfloor_2,PD_coldfloor_3,PD_coldfloor_4,PD_coldfloor_5,PD_coldfloor_6,PD_coldfloor_7,PD_coldfloor_8,PD_coldfloor_9,PD_coldfloor_10,PD_coldfloor_11,PD_coldfloor_12,PD_coldfloor_13,PD_coldfloor_14,PD_coldfloor_15,PD_coldfloor_16]
t_sun_p = [PD_heatsun_1,PD_heatsun_2,PD_heatsun_3,PD_heatsun_4,PD_heatsun_5,PD_heatsun_6,PD_heatsun_7,PD_heatsun_8,PD_heatsun_9,PD_heatsun_10,PD_heatsun_11,PD_heatsun_12,PD_heatsun_13,PD_heatsun_14,PD_heatsun_15,PD_heatsun_16]
t_heater_p =[PD_heater_1,PD_heater_2,PD_heater_3,PD_heater_4,PD_heater_5,PD_heater_6,PD_heater_7,PD_heater_8,PD_heater_9,PD_heater_10,PD_heater_11,PD_heater_12, PD_heater_13,PD_heater_14,PD_heater_15,PD_heater_16]
PD_air = [PD_air1,PD_air2,PD_air3,PD_air4,PD_air5,PD_air6,PD_air7,PD_air8,PD_air9,PD_air10,PD_air11,PD_air12,PD_air13,PD_air14,PD_air15,PD_air16]
PD_smell = [PD_smell1, PD_smell2, PD_smell3, PD_smell4, PD_smell5, PD_smell6, PD_smell7, PD_smell8, PD_smell9, PD_smell10, PD_smell11, PD_smell12, PD_smell13, PD_smell14, PD_smell15, PD_smell16]
PD_heavy = [PD_heavy1, PD_heavy2, PD_heavy3, PD_heavy4, PD_heavy5, PD_heavy6, PD_heavy7, PD_heavy8, PD_heavy9, PD_heavy10, PD_heavy11, PD_heavy12, PD_heavy13, PD_heavy14, PD_heavy15, PD_heavy16]
PD_dry = [PD_dry1, PD_dry2, PD_dry3, PD_dry4, PD_dry5, PD_dry6, PD_dry7, PD_dry8, PD_dry9, PD_dry10, PD_dry11, PD_dry12, PD_dry13, PD_dry14, PD_dry15, PD_dry16]
PD_dust = [PD_dust1, PD_dust2, PD_dust3, PD_dust4, PD_dust5, PD_dust6, PD_dust7, PD_dust8, PD_dust9, PD_dust10, PD_dust11, PD_dust12, PD_dust13, PD_dust14, PD_dust15, PD_dust16]






ele_p1 = [Per_PD_elec_1,Per_PD_elec_2,Per_PD_elec_3,Per_PD_elec_4,Per_PD_elec_5,Per_PD_elec_6,Per_PD_elec_7,Per_PD_elec_8,Per_PD_elec_9,Per_PD_elec_10,Per_PD_elec_11,Per_PD_elec_12,Per_PD_elec_13,Per_PD_elec_14,Per_PD_elec_15,Per_PD_elec_16]
col_hot_p1 = [Per_PPD_m_col_hot_1, Per_PPD_m_col_hot_2,Per_PPD_m_col_hot_3,Per_PPD_m_col_hot_4,Per_PPD_m_col_hot_5,Per_PPD_m_col_hot_6,Per_PPD_m_col_hot_7,Per_PPD_m_col_hot_8,Per_PPD_m_col_hot_9,Per_PPD_m_col_hot_10,Per_PPD_m_col_hot_11,Per_PPD_m_col_hot_12,Per_PPD_m_col_hot_13,Per_PPD_m_col_hot_14,Per_PPD_m_col_hot_15,Per_PPD_m_col_hot_16]
draw_p1 = [Per_PD_draw_1,Per_PD_draw_2,Per_PD_draw_3,Per_PD_draw_4,Per_PD_draw_5,Per_PD_draw_6,Per_PD_draw_7,Per_PD_draw_8,Per_PD_draw_9,Per_PD_draw_10,Per_PD_draw_11,Per_PD_draw_12,Per_PD_draw_13,Per_PD_draw_14,Per_PD_draw_15,Per_PD_draw_16]
fcold_p1 = [Per_PD_coldfloor_1,Per_PD_coldfloor_2,Per_PD_coldfloor_3,Per_PD_coldfloor_4,Per_PD_coldfloor_5,Per_PD_coldfloor_6,Per_PD_coldfloor_7,Per_PD_coldfloor_8,Per_PD_coldfloor_9,Per_PD_coldfloor_10,Per_PD_coldfloor_11,Per_PD_coldfloor_12,Per_PD_coldfloor_13,Per_PD_coldfloor_14,Per_PD_coldfloor_15,Per_PD_coldfloor_16]
t_sun_p1 = [Per_PD_heatsun_1,Per_PD_heatsun_2,Per_PD_heatsun_3,Per_PD_heatsun_4,Per_PD_heatsun_5,Per_PD_heatsun_6,Per_PD_heatsun_7,Per_PD_heatsun_8,Per_PD_heatsun_9,Per_PD_heatsun_10,Per_PD_heatsun_11,Per_PD_heatsun_12,Per_PD_heatsun_13,Per_PD_heatsun_14,Per_PD_heatsun_15,Per_PD_heatsun_16]
t_heater_p1 =[Per_PD_heater_1,Per_PD_heater_2,Per_PD_heater_3,Per_PD_heater_4,Per_PD_heater_5,Per_PD_heater_6,Per_PD_heater_7,Per_PD_heater_8,Per_PD_heater_9,Per_PD_heater_10,Per_PD_heater_11,Per_PD_heater_12,Per_PD_heater_13,Per_PD_heater_14,Per_PD_heater_15,Per_PD_heater_16]
decipol = [decipol_1,decipol_2,decipol_3,decipol_4,decipol_5,decipol_6,decipol_7,decipol_8,decipol_9,decipol_10,decipol_11,decipol_12,decipol_13,decipol_14,decipol_15,decipol_16]
P_PD_smell = [Per_PD_smell1,Per_PD_smell2,Per_PD_smell3,Per_PD_smell4,Per_PD_smell5,Per_PD_smell6,Per_PD_smell7,Per_PD_smell8,Per_PD_smell9,Per_PD_smell10,Per_PD_smell11,Per_PD_smell12,Per_PD_smell13,Per_PD_smell14,Per_PD_smell15,Per_PD_smell16]
P_PD_heavy = [Per_PD_heavy1,Per_PD_heavy2,Per_PD_heavy3,Per_PD_heavy4,Per_PD_heavy5,Per_PD_heavy6,Per_PD_heavy7,Per_PD_heavy8,Per_PD_heavy9,Per_PD_heavy10,Per_PD_heavy11,Per_PD_heavy12,Per_PD_heavy13,Per_PD_heavy14,Per_PD_heavy15,Per_PD_heavy16]
P_PD_dry = [Per_PD_dry1,Per_PD_dry2,Per_PD_dry3,Per_PD_dry4,Per_PD_dry5,Per_PD_dry6,Per_PD_dry7,Per_PD_dry8,Per_PD_dry9,Per_PD_dry10,Per_PD_dry11,Per_PD_dry12,Per_PD_dry13,Per_PD_dry14,Per_PD_dry15,Per_PD_dry16]
P_PD_dust = [Per_PD_dust1,Per_PD_dust2,Per_PD_dust3,Per_PD_dust4,Per_PD_dust5,Per_PD_dust6,Per_PD_dust7,Per_PD_dust8,Per_PD_dust9,Per_PD_dust10,Per_PD_dust11,Per_PD_dust12,Per_PD_dust13,Per_PD_dust14,Per_PD_dust15,Per_PD_dust16]


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, ele_p1, color='r',hatch='/',label = 'Electric shock')
plt.bar(Days, col_hot_p1,bottom=ele_p1 ,color='b',hatch='O',label = 'Cold and hot')
plt.bar(Days, draw_p1,bottom = np.add(ele_p1,col_hot_p1),color='g',hatch='+',label = 'Draught')
plt.bar(Days, fcold_p1,bottom = np.add(np.add(ele_p1,col_hot_p1),draw_p1),color='k',hatch='x',label = 'Cold floor')
plt.bar(Days, t_sun_p1,bottom = np.add(np.add(np.add(ele_p1,col_hot_p1),draw_p1),fcold_p1),color='m',hatch='-',label = 'Heat from sun')
plt.bar(Days, t_heater_p1,bottom = np.add(np.add(np.add(np.add(ele_p1,col_hot_p1),draw_p1),fcold_p1),t_sun_p1),color='c',hatch='.',label = 'Heat from heater')
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied(%)',fontsize=20)
plt.title('Percentage distribution of dissatisfaction due to different aspects in temperature with respect to days',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()




plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, ele_p, color='r',hatch='/',label = 'Electric shock')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to electric shock',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, col_hot_p,color='b',hatch='O',label = 'Cold and hot')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 6, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(5, 6),fontsize=12)
plt.axhline(y = 10, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(5, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(5, 15),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to thermal state (cold/hot)',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, draw_p,color='g',hatch='+',label = 'Draught')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 10, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(0, 10),fontsize=12)
plt.axhline(y = 20, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(0, 20),fontsize=12)
plt.axhline(y = 30, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 30),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to draught',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, fcold_p,color='k',hatch='x',label = 'Cold floor')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 10, color = 'g', linestyle = '-')
plt.annotate('Category A&B',
            xy=(0, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 15),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to cold floor',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, t_sun_p,color='m',hatch='-',label = 'Heat from sun')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 5, color = 'g', linestyle = '-')
plt.annotate('Category A&B ',
            xy=(0, 5),fontsize=12)
plt.axhline(y = 10, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 10),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to sunlight',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, t_heater_p,color='c',hatch='.',label = 'Heat from heater')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 5, color = 'g', linestyle = '-')
plt.annotate('Category A&B ',
            xy=(0, 5),fontsize=12)
plt.axhline(y = 10, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 10),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to heat from heater',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()



plt.figure(figsize=(10, 10))

plt.scatter(sorted(decipol),sorted(PD_air),color='r',label = 'Decipol vs PD')
plt.plot(sorted(decipol),sorted(PD_air),color='r')
#add trendline to plot

plt.xlabel('Perceived air Quality (Ci)',fontsize=20)
plt.ylabel('Perceived Air Quality % Dissatisfied (PD)',fontsize=20)
plt.title('Relationship between perceived air quality dissatisfied (PD) % vs Perceived air quality',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()





plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, P_PD_smell, color='r',hatch='/',label = 'PD due to smell in air ')
plt.bar(Days, P_PD_heavy,bottom=P_PD_smell ,color='b',hatch='O',label = 'PD due to heavy air')
plt.bar(Days, P_PD_dry,bottom = np.add(P_PD_smell,P_PD_heavy),color='g',hatch='+',label = 'PD due to dry air')
plt.bar(Days, P_PD_dust,bottom = np.add(np.add(P_PD_smell,P_PD_heavy),P_PD_dry),color='k',hatch='x',label = 'PD due to dust in air')
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied(%)',fontsize=20)
plt.title('Percentage distribution of dissatisfaction due to different aspects in air with respect to days',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days, PD_smell, color='b',hatch='+',label = 'PD due to smell')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to smell in air',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days,PD_heavy , color='k',hatch='-',label = 'PD due to heavy air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to heavy air',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days,PD_dry, color='m',hatch='x',label = 'PD due to dry air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to dry air ',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
plt.bar(Days,PD_dust, color='c',hatch='o',label = 'PD due to dust in air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to dust in air ',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

x_axisd = np.arange(len(Days))


#plt.figure(figsize=(8, 6))
#Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
#plt.bar(x_axisd -0.2,po3,width=0.2,label='Partially dissatisfied and said poor')
#plt.bar(x_axisd + 0,po4,width=0.2,label='Fully dissatisfied and said bad')
#plt.bar(x_axisd + 0.2,pt,width=0.2,label='Dissatisfied')
#plt.grid()
#plt.legend()
#plt.xlabel('Days')
#plt.ylabel('Percentage Dissatisfied (%)')
#plt.title('Percentage Dissatisfied due to temperature with respect to days 141')
#plt.xticks(x_axisd,Days)



import numpy as np
import pandas as pd 
import seaborn as sns
import matplotlib.pyplot as plt 
from pythermalcomfort.models import pmv_ppd 
from pythermalcomfort.utilities import v_relative, clo_dynamic
from scipy import stats as st


data141 = pd.read_csv('bratteberg_141_230221_123209_spaceplus_2930127271.csv')
data141.info()
data141.head()




temp1 = data141.iloc[6179:6467, 5]
rh1 = data141.iloc[6179:6467,6]
co2_1 = data141.iloc[6179:6467,7]
voc_1 = data141.iloc[6179:6467,8]
tm1 = temp1.mode().iloc[0]
co2m_1 = co2_1.mode().iloc[0]
vocm_1 = voc_1.mode().iloc[0]
print('the mode is')
print(tm1)
rhm1 = rh1.mode().iloc[0]
rhmn1 =statistics.mean(rh1)
PDc1 = 395 * np.exp(-15.15*(co2m_1-400)**-0.25)
Draught1 = (34 - tm1)*0.4924


temp2 = data141.iloc[6468:6754,5]
rh2 = data141.iloc[6468:6754,6]
co2_2 = data141.iloc[6179:6467,7]
voc_2 = data141.iloc[6179:6467,8]
tm2 = temp2.mode().iloc[0]
co2m_2 = co2_2.mode().iloc[0]
vocm_2 = voc_2.mode().iloc[0]
print('the mode is ')
print(tm2)
rhm2 = rh2.mode().iloc[0]
rhmn2 =statistics.mean(rh2)
PDc2 = 395 * np.exp(-15.15*(co2m_2-400)**-0.25)
Draught2 = (34 - tm2)*0.4924

temp3 = data141.iloc[6755:7042,5]
rh3 = data141.iloc[6755:7042,6]
co2_3 = data141.iloc[6755:7042,7]
voc_3 = data141.iloc[6755:7042,8]
tm3 = temp3.mode().iloc[0]
rhm3 = rh3.mode().iloc[0]
rhmn3 =statistics.mean(rh3)
co2m_3 = co2_3.mode().iloc[0]
vocm_3 = voc_3.mode().iloc[0]
PDc3 = 395 * np.exp(-15.15*(co2m_3-400)**-0.25)
Draught3 = (34 - tm3)*0.4924

temp4 = data141.iloc[7619:7905,5]
rh4 = data141.iloc[7619:7905,6]
co2_4 = data141.iloc[7619:7905,7]
voc_4 = data141.iloc[7619:7905,8]
tm4 = temp4.mode().iloc[0]
rhm4 = rh4.mode().iloc[0]
rhmn4 =statistics.mean(rh4)
co2m_4 = co2_4.mode().iloc[0]
vocm_4 = voc_4.mode().iloc[0]
PDc4 = 395 * np.exp(-15.15*(co2m_4-400)**-0.25)
Draught4 = (34 - tm4)*0.4924


temp5 = data141.iloc[7906:8193,5]
rh5 = data141.iloc[7906:8193,6]
co2_5 = data141.iloc[7906:8193,7]
voc_5 = data141.iloc[7906:8193,8]
tm5 = temp5.mode().iloc[0]
rhm5 = rh5.mode().iloc[0]
rhmn5 =statistics.mean(rh5)
co2m_5 = co2_5.mode().iloc[0]
vocm_5 = voc_5.mode().iloc[0]
PDc5 = 395 * np.exp(-15.15*(co2m_5-400)**-0.25)
Draught5 = (34 - tm5)*0.4924



temp6 = data141.iloc[8194:8481,5]
rh6 = data141.iloc[8194:8481,6]
co2_6 = data141.iloc[8194:8481,7]
voc_6 = data141.iloc[8194:8481,8]
tm6 = temp6.mode().iloc[0]
rhm6 = rh6.mode().iloc[0]
rhmn6 =statistics.mean(rh6)
co2m_6 = co2_6.mode().iloc[0]
vocm_6 = voc_6.mode().iloc[0]
PDc6 = 395 * np.exp(-15.15*(co2m_6-400)**-0.25)
Draught6 = (34 - tm6)*0.4924


temp7 = data141.iloc[8482:8769,5]
rh7 = data141.iloc[8482:8769,6]
co2_7 = data141.iloc[8482:8769,7]
voc_7 = data141.iloc[8482:8769,8]
tm7 = temp7.mode().iloc[0]
rhm7 = rh7.mode().iloc[0]
rhmn7 =statistics.mean(rh7)
co2m_7 = co2_7.mode().iloc[0]
vocm_7 = voc_7.mode().iloc[0]
PDc7 = 395 * np.exp(-15.15*(co2m_7-400)**-0.25)
Draught7 = (34 - tm7)*0.4924



temp8 = data141.iloc[8770:9057,5]
rh8 = data141.iloc[8770:9057,6]
co2_8 = data141.iloc[8770:9057,7]
voc_8 = data141.iloc[8770:9057,8]
tm8 = temp8.mode().iloc[0]
rhm8 = rh8.mode().iloc[0]
rhmn8 =statistics.mean(rh8)
co2m_8 = co2_8.mode().iloc[0]
vocm_8 = voc_8.mode().iloc[0]
PDc8 = 395 * np.exp(-15.15*(co2m_8-400)**-0.25)
Draught8 = (34 - tm8)*0.4924

temp9 = data141.iloc[9634:9921,5]
rh9 = data141.iloc[9634:9921,6]
co2_9 = data141.iloc[9634:9921,7]
voc_9 = data141.iloc[9634:9921,8]
tm9 = temp9.mode().iloc[0]
rhm9 = rh9.mode().iloc[0]
rhmn9 =statistics.mean(rh9)
co2m_9 = co2_9.mode().iloc[0]
vocm_9 = voc_9.mode().iloc[0]
PDc9 = 395 * np.exp(-15.15*(co2m_9-400)**-0.25)
Draught9 = (34 - tm9)*0.4924

temp10 = data141.iloc[9922:10209,5]
rh10 = data141.iloc[9922:10209,6]
co2_10 = data141.iloc[9922:10209,7]
voc_10 = data141.iloc[9922:10209,8]
tm10 = temp10.mode().iloc[0]
rhm10 = rh10.mode().iloc[0]
rhmn10 =statistics.mean(rh10)
co2m_10 = co2_10.mode().iloc[0]
vocm_10 = voc_10.mode().iloc[0]
PDc10 = 395 * np.exp(-15.15*(co2m_10-400)**-0.25)
Draught10 = (34 - tm10)*0.4924


temp11 = data141.iloc[10210:10497,5]
rh11 = data141.iloc[10210:10497,6]
co2_11 = data141.iloc[10210:10497,7]
voc_11 = data141.iloc[10210:10497,8]
tm11 = temp11.mode().iloc[0]
rhm11 = rh11.mode().iloc[0]
rhmn11 =statistics.mean(rh11)
co2m_11 = co2_11.mode().iloc[0]
vocm_11 = voc_11.mode().iloc[0]
PDc11 = 395 * np.exp(-15.15*(co2m_11-400)**-0.25)
Draught11 = (34 - tm11)*0.4924

temp12 = data141.iloc[10498:10785,5]
rh12 = data141.iloc[10498:10785,6]
co2_12 = data141.iloc[10498:10785,7]
voc_12 = data141.iloc[10498:10785,8]
tm12 = temp12.mode().iloc[0]
rhm12 = rh12.mode().iloc[0]
rhmn12 =statistics.mean(rh12)
co2m_12 = co2_12.mode().iloc[0]
vocm_12 = voc_12.mode().iloc[0]
PDc12 = 395 * np.exp(-15.15*(co2m_12-400)**-0.25)
Draught12 = (34 - tm12)*0.4924


temp13 = data141.iloc[10786:11072,5]
rh13 = data141.iloc[10786:11072,6]
rhmn13 =statistics.mean(rh13)
co2_13 = data141.iloc[10786:11072,7]
voc_13 = data141.iloc[10786:11072,8]
tm13 = temp13.mode().iloc[0]
rhm13 = rh13.mode().iloc[0]
co2m_13 = co2_13.mode().iloc[0]
vocm_13 = voc_13.mode().iloc[0]
PDc13 = 395 * np.exp(-15.15*(co2m_13-400)**-0.25)
Draught13 = (34 - tm13)*0.4924

temp14 = data141.iloc[13939:14226,5]
rh14 = data141.iloc[13939:14226,6]
rhmn14 =statistics.mean(rh14)
co2_14 = data141.iloc[13939:14226,7]
voc_14 = data141.iloc[13939:14226,8]
tm14 = temp14.mode().iloc[0]
rhm14 = rh14.mode().iloc[0]
co2m_14 = co2_14.mode().iloc[0]
vocm_14 = voc_14.mode().iloc[0]
PDc14 = 395 * np.exp(-15.15*(co2m_14-400)**-0.25)
Draught14 = (34 - tm14)*0.4924


temp15 = data141.iloc[14227:14514,5]
rh15 = data141.iloc[14227:14514,6]
rhmn15 =statistics.mean(rh15)
co2_15 = data141.iloc[14227:14514,7]
voc_15 = data141.iloc[14227:14514,8]
tm15 = temp15.mode().iloc[0]
rhm15 = rh15.mode().iloc[0]
co2m_15 = co2_15.mode().iloc[0]
vocm_15 = voc_15.mode().iloc[0]
PDc15 = 395 * np.exp(-15.15*(co2m_15-400)**-0.25)
Draught15 = (34 - tm15)*0.4924


temp16 = data141.iloc[14803:15090,5]
rh16 = data141.iloc[14803:15090,6]
rhmn16 =statistics.mean(rh16)
co2_16 = data141.iloc[14803:15090,7]
voc_16 = data141.iloc[14803:15090,8]
tm16 = temp16.mode().iloc[0]
rhm16 = rh16.mode().iloc[0]
co2m_16 = co2_16.mode().iloc[0]
vocm_16 = voc_16.mode().iloc[0]
PDc16 = 395 * np.exp(-15.15*(co2m_16-400)**-0.25)
Draught16 = (34 - tm16)*0.4924


tempd = [tm1,tm2,tm3,tm4,tm5,tm6,tm7,tm8,tm9,tm10,tm11,tm12,tm13,tm14,tm15,tm16]
#[temp1,temp2,temp3,temp4,temp5,temp6,temp7,temp8,temp9,temp10,temp11,temp12,temp13,temp14,temp15,temp16]
rhd = [rhm1,rhm2,rhm3,rhm4,rhm5,rhm6,rhm7,rhm8,rhm9,rhm10,rhm11,rhm12,rhm13,rhm14,rhm15,rhm16] 
rhdn = [rhmn1,rhmn2,rhmn3,rhmn4,rhmn5,rhmn6,rhmn7,rhmn8,rhmn9,rhmn10,rhmn11,rhmn12,rhmn13,rhmn14,rhmn15,rhmn16] 
#[rh1,rh2,rh3,rh4,rh5,rh6,rh7,rh8,rh9,rh10,rh11,rh12,rh13,rh14,rh15,rh16]
co2d = [co2m_1,co2m_2,co2m_3,co2m_4,co2m_5,co2m_6,co2m_7,co2m_8,co2m_9,co2m_10,co2m_11,co2m_12,co2m_13,co2m_14,co2m_15,co2m_16]
vocd = [vocm_1,vocm_2,vocm_3,vocm_4,vocm_5,vocm_6,vocm_7,vocm_8,vocm_9,vocm_10,vocm_11,vocm_12,vocm_13,vocm_14,vocm_15,vocm_16]
PDc = [PDc1,PDc2,PDc3,PDc4,PDc5,PDc6,PDc7,PDc8,PDc9,PDc10,PDc11,PDc12,PDc13,PDc14,PDc15,PDc16]
Draught = [Draught1,Draught2,Draught3,Draught4,Draught5,Draught6,Draught7,Draught8,Draught9,Draught10,Draught11,Draught12,Draught13,Draught14,Draught15,Draught16]

plt.figure(figsize=(10, 6))
CO2days = [co2_1, co2_2, co2_3,co2_4,co2_5,co2_6,co2_7,co2_8,co2_9,co2_10,co2_11,co2_12,co2_13,co2_14,co2_15,co2_16]
Dayse = ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
x_axise = np.arange(len(Dayse))
sns.boxplot(CO2days)
plt.xlabel('Days',fontsize=20) 
plt.ylabel('CO2(ppm)',fontsize=20) 
plt.title('CO2(ppm) with days',fontsize=20)
plt.xticks(x_axise,Dayse)
plt.grid()
plt.show()




plt.figure(figsize=(10, 6))
VOCdays = [voc_1, voc_2, voc_3,voc_4,voc_5,voc_6,voc_7,voc_8,voc_9,voc_10,voc_11,voc_12,voc_13,voc_14,voc_15,voc_16]
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
x_axise = np.arange(len(Dayse))
sns.boxplot(VOCdays)
plt.xlabel('Days',fontsize=20) 
plt.ylabel('VOC(I¼g/m3)',fontsize=20) 
plt.title('VOC(I¼g/m3) with days',fontsize=20)
plt.xticks(x_axise,Dayse)
plt.grid()
plt.show()

plt.figure(figsize=(10, 6))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
x_axise = np.arange(len(Dayse))
plt.bar(Days, PDc,color='r',hatch='/',label='Percentage Dissatisfied due to CO2')
plt.xlabel('Days',fontsize=20) 
plt.ylabel('Percentage dissatisfied (PD %)',fontsize=20) 
plt.title('1st maximum occurring percentage Dissatisfied with CO2 concentration (PD %) with days',fontsize=20)
plt.xticks(x_axise,Dayse)
plt.legend(loc='center left', bbox_to_anchor=(1, 0.9),fontsize=12)
plt.grid()
plt.show()

fig, ax1 = plt.subplots(figsize=(10, 6))

ax2 = ax1.twinx()

X_axis = np.arange(len(Days)) 

ax1.bar(X_axis -0.2, co2d , color='r',hatch='/',label='CO2(ppm)')
ax2.bar(X_axis +0.2, vocd, color='b',hatch='O',label = 'VOC(I¼g/m3)')

ax1.set_xlabel('Days',fontsize=20)
ax1.set_ylabel('CO2(ppm)', color='r',fontsize=20)
ax2.set_ylabel('VOC(I¼g/m3)', color='b',fontsize=20)
ax1.axhline(y = 1000, color = 'r', linestyle = '-')
ax1.annotate('Concentration limit for CO2',
            xy=(0, 1000),fontsize=12)
plt.xticks(x_axise,Dayse)
plt.title('1st maximum occurring CO2(ppm) and VOC(I¼g/m3) level with days',fontsize=20)

ax1.legend(loc='center left', bbox_to_anchor=(1.1, 0.9),fontsize=12)
ax2.legend(loc='center left', bbox_to_anchor=(1.1, 0.8),fontsize=12)

plt.grid()
plt.show()

tdb1 = tempd
tr1 = tdb1
rh1 = rhd
v1 = 0.1
met1 = 1.2
clo1 =1
  
#calculate relative air speed 
v_r1 = v_relative (v=v1, met=met1)

#calculate dynamic clothing
clo_d1 = clo_dynamic(clo=clo1, met=met1)
results1 = pmv_ppd(tdb=tdb1, tr=tr1, vr=v_r1, rh=rh1, met=met1, clo=clo_d1)

Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
x_axisd = np.arange(len(Days))

plt.figure(figsize=(10, 6))
plt.plot(x_axisd,tempd,'g--')
plt.axhline(y = 20, color = 'r', linestyle = '-') 
plt.axhline(y = 22, color = 'g', linestyle = '-') 
plt.axhline(y = 27, color = 'r', linestyle = '-') 
plt.xlabel('Days',fontsize=20)
plt.ylabel('Temperature (°C)',fontsize=20)
plt.title('1st maximum occuring temperature (°C) with days',fontsize=20)
plt.xticks(x_axisd,Days)
plt.grid()
plt.show()

plt.figure(figsize=(10, 6))
plt.plot(x_axisd,rhd,'g--')
plt.axhline(y = 30, color = 'r', linestyle = '-')  
plt.axhline(y = 70, color = 'r', linestyle = '-') 
plt.xlabel('Days',fontsize=20)
plt.ylabel('Relative Humidity (%)',fontsize=20)
plt.title('1st maximum  occurring relative humidity (%) with days',fontsize=20)
plt.xticks(x_axisd,Days)
plt.grid()
plt.show()


print(results1["pmv"])
print(results1["ppd"])

PMVs = [-0.51,	-0.5,	-0.44,	-0.43,	-0.37,	-0.36,	-0.34,	-0.31,	-0.24,	-0.22,	-0.2,	-0.17,	-0.07,	-0.02,	0,	0.02]
PPDs = [10.4,	10.3,	9.1,	8.8,	7.9,	7.7,	7.3,	6.9,	6.2,	6,	5.8,	5.6,	5.1,	5,	5,	5]


plt.figure(figsize=(10, 10))

plt.scatter(PMVs,PPDs,color='r',label = 'PMV vs PPD')
plt.plot(PMVs,PPDs,color='r')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 6, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(-0.5, 6),fontsize=12)
plt.axhline(y = 10, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(-0.5, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(-0.5, 15),fontsize=12)
plt.xlabel('PMV',fontsize=20)
plt.ylabel('PPD (%)',fontsize=20)
plt.title('Relationship between Percentage Dissatisfied and PMV',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()



    
#plt.figure().set_figwidth(15)

#plt.plot(x_axisd,po4,'g--',label='Fully dissatisfied and said bad')
#plt.plot(x_axisd,po3,'r--',label='Partially dissatisfied and said poor')
#plt.plot(x_axisd,pt,'p--',label='Sum of  badly and poorly dissatisfied')
#plt.plot(x_axisd,results1["ppd"],'b--',label='Predicted percentage dissatisfied with ISO 7730')
#plt.title('141 comparison')
#plt.xlabel('Days')
#plt.ylabel('Percentage dissatified')
#plt.legend()
#plt.grid()
#plt.show()

    
#plt.figure().set_figwidth(15)
#Diff1 = po3 - results1["ppd"]
#Diff2 = po4 - results1["ppd"]
#Diff3 = pt - results1["ppd"]
#plt.plot(x_axisd,Diff1,'g--',label='Error between predicted and measured who said poor')
#plt.plot(x_axisd,Diff2,'r--',label='Error between predicted and measured who said bad')
#plt.plot(x_axisd,Diff3,'p--',label='Error between predicted and measured with sum')
#plt.title('141')
#plt.xlabel('Days')
#plt.ylabel('Difference in percentage')
#plt.xticks(x_axisd,Days)
#plt.legend()
#plt.grid()
#plt.show()

plt.figure(figsize=(10, 6))
# -*- coding: utf-8 -*-
"""
Created on Wed Oct 18 16:29:18 2023

@author: aayamc
"""

import numpy as np
import pandas as pd 
import seaborn as sns
import matplotlib.pyplot as plt 
from pythermalcomfort.models import pmv_ppd 
from pythermalcomfort.utilities import v_relative, clo_dynamic
from scipy import stats as st


data_bems_141 = pd.read_csv('bratteberg_141_230308_0000_sauter_noserialnumber.csv')
data_bems_141.info()
data_bems_141.head()

heater1 = data_bems_141.iloc[11650:11746, 1]
heater0_1 = 0
heater1_1 = heater1.value_counts()[1]
heatert_1 = heater0_1 + heater1_1
per_heater0_1 = heater0_1/heatert_1
per_heater1_1 = heater1_1/heatert_1
floor_heater1 = data_bems_141.iloc[11650:11746, 2]
floor_heater0_1 = floor_heater1.value_counts()[0]
floor_heater1_1 = 0
floor_heatert_1 = floor_heater0_1 + floor_heater1_1
per_floor_heater0_1 = floor_heater0_1/floor_heatert_1
per_floor_heater1_1 = floor_heater1_1/floor_heatert_1
room_temp1 = data_bems_141.iloc[11650:11746, 3]
room_temp0_1 = 0
room_temp1_1 = 0
room_temp1_1 = room_temp0_1 + room_temp1
floor_temp1 = data_bems_141.iloc[11650:11746, 4]
floor_tempm1 = data_bems_141.iloc[11650:11746, 4].mode().iloc[0]
Temp_diff1 = floor_temp1 - room_temp1
PDv1 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff1))
PDf1 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp1 - 0.0025 * floor_temp1**2)
PDfm1 = PDf1.mode().iloc[0]



heater2 = data_bems_141.iloc[12987:13240,1]
heater0_2 = 0
heater1_2 = heater2.value_counts()[1]
print('The number ')
print(heater1_2)
heatert_2 = heater0_2 + heater1_2
print(heatert_2)
per_heater0_2 = heater0_2/heatert_2
per_heater1_2 = heater1_2/heatert_2
floor_heater2 = data_bems_141.iloc[12987:13240,2]
floor_heater0_2 = floor_heater2.value_counts()[0]
print('the number')
print(floor_heater0_2)
floor_heater1_2 = 0
print(floor_heater1_2)
floor_heatert_2 = floor_heater0_2 + floor_heater1_2
print(floor_heatert_2)
per_floor_heater0_2 = floor_heater0_2/floor_heatert_2
per_floor_heater1_2 = floor_heater1_2/floor_heatert_2
room_temp2 = data_bems_141.iloc[12987:13240,3]
room_temp0_2 = 0
room_temp1_2 = 0
floor_temp2 = data_bems_141.iloc[12987:13240, 4]

floor_tempm2 = data_bems_141.iloc[12987:13240, 4].mode().iloc[0]
Temp_diff2 = floor_temp2 - room_temp2
PDv2 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff2))
PDf2 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp2 - 0.0025 * floor_temp2**2)
PDfm2 = PDf2.mode().iloc[0]

heater3 = data_bems_141.iloc[14423:14677,1]
heater0_3 = 0
heater1_3 = heater3.value_counts()[1]
heatert_3 = heater0_3 + heater1_3
per_heater0_3 = heater0_3/heatert_3
per_heater1_3 = heater1_3/heatert_3
floor_heater3 = data_bems_141.iloc[14423:14677,2]
floor_heater0_3 = floor_heater3.value_counts()[0]
floor_heater1_3 = 0
floor_heatert_3 = floor_heater0_3 + floor_heater1_3
per_floor_heater0_3 = floor_heater0_3/floor_heatert_3
per_floor_heater1_3 = floor_heater1_3/floor_heatert_3
room_temp3 = data_bems_141.iloc[14423:14677,3]
room_temp0_3 = 0
room_temp1_3 = 0
floor_temp3 = data_bems_141.iloc[14423:14677, 4]
floor_tempm3 = data_bems_141.iloc[14423:14677, 4].mode().iloc[0]
Temp_diff3 = floor_temp3 - room_temp3
PDv3 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff3))
PDf3 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp3 - 0.0025 * floor_temp3**2)
PDfm3 = PDf3.mode().iloc[0]


heater4 = data_bems_141.iloc[18736:19000,1]
heater0_4 = 0
heater1_4 = heater4.value_counts()[1]
heatert_4 = heater0_4 + heater1_4
per_heater0_4 = heater0_4/heatert_4
per_heater1_4 = heater1_4/heatert_4
floor_heater4 = data_bems_141.iloc[18736:19000,2]
floor_heater0_4 = floor_heater4.value_counts()[0]
floor_heater1_4 = 0
floor_heatert_4 = floor_heater0_4 + floor_heater1_4
per_floor_heater0_4 = floor_heater0_4/floor_heatert_4
per_floor_heater1_4 = floor_heater1_4/floor_heatert_4
room_temp4 = data_bems_141.iloc[18736:19000,3]
room_temp0_4 = 0
room_temp1_4 = 0
floor_temp4 = data_bems_141.iloc[18736:19000, 4]
floor_tempm4 = data_bems_141.iloc[18736:19000, 4].mode().iloc[0]
Temp_diff4 = floor_temp4 - room_temp4
PDv4 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff4))
PDf4 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp4 - 0.0025 * floor_temp4**2)
PDfm4 = PDf4.mode().iloc[0]


heater5 = data_bems_141.iloc[20181:20436,1]
heater0_5 = 0
heater1_5 = heater5.value_counts()[1]
heatert_5 = heater0_5 + heater1_5
per_heater0_5 = heater0_5/heatert_5
per_heater1_5 = heater1_5/heatert_5
floor_heater5 = data_bems_141.iloc[20181:20436,2]
floor_heater0_5 = floor_heater5.value_counts()[0]
floor_heater1_5 = 0
floor_heatert_5 = floor_heater0_5 + floor_heater1_5
per_floor_heater0_5 = floor_heater0_5/floor_heatert_5
per_floor_heater1_5 = floor_heater1_5/floor_heatert_5
room_temp5 = data_bems_141.iloc[20181:20436,3]
room_temp0_5 = 0
room_temp1_5 = 0
floor_temp5 = data_bems_141.iloc[20181:20436, 4]
floor_tempm5 = data_bems_141.iloc[20181:20436, 4].mode().iloc[0]
Temp_diff5 = floor_temp5 - room_temp5
PDv5 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff5))
PDf5 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp5 - 0.0025 * floor_temp5**2)
PDfm5 = PDf5.mode().iloc[0]


heater6 = data_bems_141.iloc[21619:21940,1]
heater0_6 = 0
heater1_6 = heater6.value_counts()[1]
heatert_6 = heater0_6 + heater1_6
per_heater0_6 = heater0_6/heatert_6
per_heater1_6 = heater1_6/heatert_6
floor_heater6 = data_bems_141.iloc[21619:21940,2]
floor_heater0_6 = floor_heater6.value_counts()[0]
print(floor_heater0_6)
floor_heater1_6 = 0
print(floor_heater1_6)
floor_heatert_6 = floor_heater0_6 + floor_heater1_6
print(floor_heatert_6)
per_floor_heater0_6 = floor_heater0_6/floor_heatert_6
print()
per_floor_heater1_6 = floor_heater1_6/floor_heatert_6
room_temp6 = data_bems_141.iloc[21619:21940,3]
room_temp0_6 = 0
room_temp1_6 = 0
floor_temp6 = data_bems_141.iloc[21619:21940, 4]
floor_tempm6 = data_bems_141.iloc[21619:21940, 4].mode().iloc[0]
Temp_diff6 = floor_temp6 - room_temp6
PDv6 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff6))
PDf6 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp6 - 0.0025 * floor_temp5**6)
PDfm6 = 0



heater8 = data_bems_141.iloc[23062:23316,1]
heater0_8 = 0
heater1_8 = heater8.value_counts()[1]
heatert_8 = heater0_8 + heater1_8
per_heater0_8 = heater0_8/heatert_8
per_heater1_8 = heater1_8/heatert_8
floor_heater8 = data_bems_141.iloc[23062:23316,2]
floor_heater0_8 = floor_heater8.value_counts()[0]
floor_heater1_8 = 0
floor_heatert_8 = floor_heater0_8 + floor_heater1_8
per_floor_heater0_8 = floor_heater0_8/floor_heatert_8
per_floor_heater1_8 = floor_heater1_8/floor_heatert_8
room_temp8 = data_bems_141.iloc[23062:23316,3]
room_temp0_8 = 0
room_temp1_8 = 0
floor_temp8 = data_bems_141.iloc[23062:23316, 4]
floor_tempm8 = data_bems_141.iloc[23062:23316, 4].mode().iloc[0]
Temp_diff8 = floor_temp8 - room_temp8
PDv8 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff8))
PDf8 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp8 - 0.0025 * floor_temp8**2)
PDfm8 = PDf8.mode().iloc[0]



heater9 = data_bems_141.iloc[24514:24771,1]
heater0_9 = 0
heater1_9 = heater9.value_counts()[1]
heatert_9 = heater0_9 + heater1_9
per_heater0_9 = heater0_9/heatert_9
per_heater1_9 = heater1_9/heatert_9
floor_heater9 = data_bems_141.iloc[24514:24771,2]
floor_heater0_9 = floor_heater9.value_counts()[0]
floor_heater1_9 = 0
floor_heatert_9 = floor_heater0_9 + floor_heater1_9
per_floor_heater0_9 = floor_heater0_9/floor_heatert_9
per_floor_heater1_9 = floor_heater1_9/floor_heatert_9
room_temp9 = data_bems_141.iloc[24514:24771,3]
room_temp0_9 = 0
room_temp1_9 = 0
floor_temp9 = data_bems_141.iloc[24514:24771, 4]
floor_tempm9 = data_bems_141.iloc[24514:24771, 4].mode().iloc[0]
Temp_diff9 = floor_temp9 - room_temp9
PDv9 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff9))
PDf9 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp9 - 0.0025 * floor_temp9**2)
PDfm9 = PDf9.mode().iloc[0]



heater10 = data_bems_141.iloc[28718:28959,1]
heater0_10 = 0
heater1_10 = heater10.value_counts()[1]
heatert_10 = heater0_10 + heater1_10
per_heater0_10 = heater0_10/heatert_10
per_heater1_10 = heater1_10/heatert_10
floor_heater10 = data_bems_141.iloc[28718:28959,2]
floor_heater0_10 = floor_heater10.value_counts()[0]
floor_heater1_10 = 0
floor_heatert_10 = floor_heater0_10 + floor_heater1_10
per_floor_heater0_10 = floor_heater0_10/floor_heatert_10
per_floor_heater1_10 = floor_heater1_10/floor_heatert_10
room_temp10 = data_bems_141.iloc[28718:28959,3]
room_temp0_10 = 0
room_temp1_10 = 0
floor_temp10 = data_bems_141.iloc[28718:28959, 4]
floor_tempm10 = data_bems_141.iloc[28718:28959, 4].mode().iloc[0]
Temp_diff10 = floor_temp10 - room_temp10
PDv10 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff10))
PDf10 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp10 - 0.0025 * floor_temp10**2)
PDfm10 = 0



heater11 = data_bems_141.iloc[30141:30391,1]
heater0_11 = 0
heater1_11 = heater11.value_counts()[1]
heatert_11 = heater0_11 + heater1_11
per_heater0_11 = heater0_11/heatert_11
per_heater1_11 = heater1_11/heatert_11
floor_heater11 = data_bems_141.iloc[30141:30391,2]
floor_heater0_11 = floor_heater11.value_counts()[0]
floor_heater1_11 = 0
floor_heatert_11 = floor_heater0_11 + floor_heater1_11
per_floor_heater0_11 = floor_heater0_11/floor_heatert_11
per_floor_heater1_11 = floor_heater1_11/floor_heatert_11
room_temp11 = data_bems_141.iloc[30141:30391,3]
room_temp0_11 = 0
room_temp1_11 = 0
floor_temp11 = data_bems_141.iloc[30141:30391, 4]
floor_tempm11 = data_bems_141.iloc[30141:30391, 4].mode().iloc[0]
Temp_diff11 = floor_temp11 - room_temp11
PDv11 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff11))
PDf11 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp11 - 0.0025 * floor_temp11**2)
PDfm11 = PDf11.mode().iloc[0]



heater12 = data_bems_141.iloc[31586:31796,1]
heater0_12 = 0
heater1_12 = heater12.value_counts()[1]
heatert_12 = heater0_12 + heater1_12
per_heater0_12 = heater0_12/heatert_12
per_heater1_12 = heater1_12/heatert_12
floor_heater12 = data_bems_141.iloc[31586:31796,2]
floor_heater0_12 = floor_heater11.value_counts()[0]
floor_heater1_12 = 0
floor_heatert_12 = floor_heater0_12 + floor_heater1_12
per_floor_heater0_12 = floor_heater0_12/floor_heatert_12
per_floor_heater1_12 = floor_heater1_12/floor_heatert_12
room_temp12 = data_bems_141.iloc[31586:31796,3]
room_temp0_12 = 0
room_temp1_12 = 0
floor_temp12 = data_bems_141.iloc[31586:31796, 4]
floor_tempm12 = data_bems_141.iloc[31586:31796, 4].mode().iloc[0]
Temp_diff12 = floor_temp12 - room_temp12
PDv12 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff12))
PDf12 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp12 - 0.0025 * floor_temp12**2)
PDfm12 = PDf12.mode().iloc[0]



heater15 = data_bems_141.iloc[33024:33270,1]
heater0_15 = 0
heater1_15 = heater15.value_counts()[1]
heatert_15 = heater0_15 + heater1_15
per_heater0_15 = heater0_15/heatert_15
per_heater1_15 = heater1_15/heatert_15
floor_heater15 = data_bems_141.iloc[33024:33270,2]
floor_heater0_15 = floor_heater15.value_counts()[0]
floor_heater1_15 = 0
floor_heatert_15 = floor_heater0_15 + floor_heater1_15
per_floor_heater0_15 = floor_heater0_15/floor_heatert_15
per_floor_heater1_15 = floor_heater1_15/floor_heatert_15
room_temp15 = data_bems_141.iloc[33024:33270,3]
room_temp0_15 = 0
room_temp1_15 = 0
floor_temp15 = data_bems_141.iloc[33024:33270, 4]
floor_tempm15 = data_bems_141.iloc[33024:33270, 4].mode().iloc[0]
Temp_diff15 = floor_temp15 - room_temp15
PDv15 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff15))
PDf15 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp15 - 0.0025 * floor_temp15**2)
PDfm15 = PDf15.mode().iloc[0]

heater16 = data_bems_141.iloc[34467:34717,1]
heater0_16 = 0
heater1_16 = heater16.value_counts()[1]
heatert_16 = heater0_16 + heater1_16
per_heater0_16 = heater0_16/heatert_16
per_heater1_16 = heater1_16/heatert_16
floor_heater16 = data_bems_141.iloc[34467:34717,2]
floor_heater0_16 = floor_heater16.value_counts()[0]
floor_heater1_16 = 0
floor_heatert_16 = floor_heater0_16 + floor_heater1_16
per_floor_heater0_16 = floor_heater0_16/floor_heatert_16
per_floor_heater1_16 = floor_heater1_16/floor_heatert_16
room_temp16 = data_bems_141.iloc[34467:34717,3]
room_temp0_16 = 0
room_temp1_16 = 0
floor_temp16 = data_bems_141.iloc[34467:34717, 4]
floor_tempm16 = data_bems_141.iloc[34467:34717, 4].mode().iloc[0]
Temp_diff16 = floor_temp16 - room_temp16
PDv16 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff16))
PDf16 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp16 - 0.0025 * floor_temp16**2)
PDfm16 = PDf16.mode().iloc[0]

heater17 = data_bems_141.iloc[50325:50505,1]
heater0_17 = 0
heater1_17 = heater17.value_counts()[1]
heatert_17 = heater0_17 + heater1_17
per_heater0_17 = heater0_17/heatert_17
per_heater1_17 = heater1_17/heatert_17
floor_heater17 = data_bems_141.iloc[50325:50505,2]
floor_heater0_17 = floor_heater17.value_counts()[0]
floor_heater1_17 = 0
floor_heatert_17 = floor_heater0_17 + floor_heater1_17
per_floor_heater0_17 = floor_heater0_17/floor_heatert_17
per_floor_heater1_17 = floor_heater1_17/floor_heatert_17
room_temp17 = data_bems_141.iloc[50325:50505,3]
room_temp0_17 = 0
room_temp1_17 = 0
floor_temp17 = data_bems_141.iloc[50325:50505, 4]
floor_tempm17 = data_bems_141.iloc[50325:50505, 4].mode().iloc[0]
Temp_diff17 = floor_temp17 - room_temp17
PDv17 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff17))
PDf17 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp17 - 0.0025 * floor_temp17**2)
PDfm17 = PDf17.mode().iloc[0]

heater18 = data_bems_141.iloc[51748:51852,1]
heater0_18 = 0
heater1_18 = heater18.value_counts()[1]
heatert_18 = heater0_18 + heater1_18
per_heater0_18 = heater0_18/heatert_18
per_heater1_18 = heater1_18/heatert_18
floor_heater18 = data_bems_141.iloc[51748:51852,2]
floor_heater0_18 = floor_heater18.value_counts()[0]
floor_heater1_18 = 0
floor_heatert_18 = floor_heater0_18 + floor_heater1_18
per_floor_heater0_18 = floor_heater0_18/floor_heatert_18
per_floor_heater1_18 = floor_heater1_18/floor_heatert_18
room_temp18 = data_bems_141.iloc[51748:51852,3]
room_temp0_18 = 0
room_temp1_18 = 0
floor_temp18 = data_bems_141.iloc[51748:51852, 4]
floor_tempm18 = data_bems_141.iloc[51748:51852, 4].mode().iloc[0]
Temp_diff18 = floor_temp18 - room_temp18
PDv18 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff18))
PDf18 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp18 - 0.0025 * floor_temp18**2)
PDfm18 = PDf18.mode().iloc[0]

heater19 = data_bems_141.iloc[51748:51852,1]
heater0_19 = 0
heater1_19 = heater19.value_counts()[1]
heatert_19 = heater0_19 + heater1_19
per_heater0_19 = heater0_19/heatert_19
per_heater1_19 = heater1_19/heatert_19
floor_heater19 = data_bems_141.iloc[51748:51852,2]
floor_heater0_19 = floor_heater19.value_counts()[0]
floor_heater1_19 = 0
floor_heatert_19 = floor_heater0_19 + floor_heater1_19
per_floor_heater0_19 = floor_heater0_19/floor_heatert_19
per_floor_heater1_19 = floor_heater1_19/floor_heatert_19
room_temp19 = data_bems_141.iloc[51748:51852,3]
room_temp0_19 = 0
room_temp1_19 = 0
floor_temp19 = data_bems_141.iloc[51748:51852, 4]
floor_tempm19 = data_bems_141.iloc[51748:51852, 4].mode().iloc[0]
Temp_diff19 = floor_temp18 - room_temp18 
PDv19 = 100 / (1 + np.exp(5.76 - 0.856 * Temp_diff19))
PDf19 = 100 - 94 * np.exp(-1.387 + 0.118 * floor_temp19 - 0.0025 * floor_temp19**2)
PDfm19 = PDf19.mode().iloc[0]

p1 = [per_heater0_1,per_heater0_2,per_heater0_3,per_heater0_4,per_heater0_5,per_heater0_6,per_heater0_8,per_heater0_9,per_heater0_10,per_heater0_11,per_heater0_12,per_heater0_15,per_heater0_16,per_heater0_17,per_heater0_18,per_heater0_19] 
print('okeay perce')
print(p1)
p2 = [per_heater1_1,per_heater1_2,per_heater1_3,per_heater1_4,per_heater1_5,per_heater1_6,per_heater1_8,per_heater1_9,per_heater1_10,per_heater1_11,per_heater1_12,per_heater1_15,per_heater1_16,per_heater1_17,per_heater1_18,per_heater1_19] 
print(p2)
p3 = [per_floor_heater0_1,per_floor_heater0_2,per_floor_heater0_3,per_floor_heater0_4,per_floor_heater0_5,per_floor_heater0_6,per_floor_heater0_8,per_floor_heater0_9,per_floor_heater0_10,per_floor_heater0_11,per_floor_heater0_12,per_floor_heater0_15,per_floor_heater0_16,per_floor_heater0_17,per_floor_heater0_18,1]
print(p3)
p4 = [per_floor_heater1_1,per_floor_heater1_2,per_floor_heater1_3,per_floor_heater1_4,per_floor_heater1_5,per_floor_heater1_6,per_floor_heater1_8,per_floor_heater1_9,per_floor_heater1_10,per_floor_heater1_11,per_floor_heater1_12,per_floor_heater1_15,per_floor_heater1_16,per_floor_heater1_17,per_floor_heater1_18,floor_heater1_19] 
print(p4)
PDV = [PDv1,PDv2,PDv3,PDv4,PDv5,PDv6,PDv8,PDv9,PDv10,PDv11,PDv12,PDv15,PDv16,PDv17,PDv18,PDv19]
PDf = [PDf1, PDf2, PDf3,PDf4,PDf5,PDf6,PDf8,PDf9,PDf10,PDf11,PDf12,PDf15,PDf16,PDf17,PDf18,PDf19]
PDfm = [PDfm1, PDfm2, PDfm3,PDfm4,PDfm5,PDfm6,PDfm8,PDfm9,PDfm10,PDfm11,PDfm12,PDfm15,PDfm16,PDfm17,PDfm18,PDfm19]

Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13','D14','D15','D16']
x_axisdx = np.arange(len(Days))

plt.figure(figsize=(10, 6))
PDV = [PDv1,PDv2,PDv3,PDv4,PDv5,PDv6,PDv8,PDv9,PDv10,PDv11,PDv12,PDv15,PDv16,PDv17,PDv18]
sns.boxplot(PDV)
plt.xlabel('Days',fontsize=20) 
plt.ylabel('Percentage Dissatisfied (PD %)',fontsize=20) 
plt.title('Dissatisfaction due to vertical temperature asymmetry with days',fontsize=20)
plt.xticks(x_axisdx,Days)
plt.grid()
plt.show()

plt.figure(figsize=(10, 6))
sns.boxplot(PDf)
plt.xlabel('Days',fontsize=20) 
plt.ylabel('Percentage Dissatisfied (PD %)',fontsize=20) 
plt.title('Dissatisfaction due to cold floor with days',fontsize=20)
plt.xticks(x_axisdx,Days)
plt.grid()
plt.show()

#fig, ax = plt.subplots(figsize = (10, 10))

#ax2 = ax.twinx()
#ax.plot(x_axisdx ,p1,'g--',label='Percentage of time the heater is not functioning')
#ax.plot(x_axisdx ,p2,'r*',label='Percentage of time the heater is functioning')
#ax.plot(x_axisdx ,p3,'b--',label='Percentage of time the floor heater is not functioning')
#ax.plot(x_axisdx ,p4,'y*',label='Percentage of time the floor heater is functioning')

#ax.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
#ax.set_xlabel('Days',fontsize=20)
#ax.set_ylabel('Percentage of time the system is functioning',fontsize=20)
#ax2.bar(x_axisd -0.2,po3,width=0.2,hatch='o',label='Partially dissatisfied and said poor')
#ax2.bar(x_axisd + 0,po4,width=0.2,hatch='*',label='Fully dissatisfied and said bad')
#ax2.bar(x_axisd + 0.2,pt,width=0.2,hatch='x',label='Dissatisfied')
#ax2.bar(x_axisd + 0.4,(results1["ppd"]) ,width=0.2,hatch='+',label='Predicted percentage dissatisfied (ISO 7730)')
#ax2.grid()
#ax2.legend(loc='center left', bbox_to_anchor=(1.05, 0.5),fontsize=20)
#ax2.set_ylabel('Percentage Dissatisfied (PD %)',fontsize=20)
#plt.title('Operational situation of systems and the percentage dissatisfied with respect to days at bratteberg room 141',fontsize=20)

#plt.xticks(x_axisdx,Days)


import numpy as np
import pandas as pd 
import seaborn as sns
import matplotlib.pyplot as plt 
from pythermalcomfort.models import pmv_ppd 
from pythermalcomfort.utilities import v_relative, clo_dynamic
from prettytable import PrettyTable

data_bems_141 = pd.read_csv('bratteberg_141_230308_0000_sauter_noserialnumber - Copy1.csv')
data_bems_141.info()
data_bems_141.head()

heater1 = data_bems_141.iloc[11053:12531, 1]
heater0_1 = 0
heater1_1 = heater1.value_counts()[1]
heatert_1 = heater0_1 + heater1_1
per_heater0_1 = heater0_1/heatert_1
per_heater1_1 = heater1_1/heatert_1
floor_heater1 = data_bems_141.iloc[11053:12531, 2]
floor_heater0_1 = floor_heater1.value_counts()[0]
floor_heater1_1 = floor_heater1.value_counts()[1]
floor_heatert_1 = floor_heater0_1 + floor_heater1_1
per_floor_heater0_1 = floor_heater0_1/floor_heatert_1
per_floor_heater1_1 = floor_heater1_1/floor_heatert_1




heater2 = data_bems_141.iloc[12532:13971,1]
heater0_2 = 0
heater1_2 = heater2.value_counts()[1]
print('The number ')
print(heater1_2)
heatert_2 = heater0_2 + heater1_2
print(heatert_2)
per_heater0_2 = heater0_2/heatert_2
per_heater1_2 = heater1_2/heatert_2
floor_heater2 = data_bems_141.iloc[12532:13971,2]
floor_heater0_2 = floor_heater2.value_counts()[0]
print('the number')
print(floor_heater0_2)
floor_heater1_2 = floor_heater2.value_counts()[1]
print(floor_heater1_2)
floor_heatert_2 = floor_heater0_2 + floor_heater1_2
print(floor_heatert_2)
per_floor_heater0_2 = floor_heater0_2/floor_heatert_2
per_floor_heater1_2 = floor_heater1_2/floor_heatert_2


heater3 = data_bems_141.iloc[13972:15411,1]
heater0_3 = 0
heater1_3 = heater3.value_counts()[1]
heatert_3 = heater0_3 + heater1_3
per_heater0_3 = heater0_3/heatert_3
per_heater1_3 = heater1_3/heatert_3
floor_heater3 = data_bems_141.iloc[13972:15411,2]
floor_heater0_3 = floor_heater3.value_counts()[0]
floor_heater1_3 = floor_heater3.value_counts()[1]
floor_heatert_3 = floor_heater0_3 + floor_heater1_3
per_floor_heater0_3 = floor_heater0_3/floor_heatert_3
per_floor_heater1_3 = floor_heater1_3/floor_heatert_3



heater4 = data_bems_141.iloc[18292:19731,1]
heater0_4 = 0
heater1_4 = heater4.value_counts()[1]
heatert_4 = heater0_4 + heater1_4
per_heater0_4 = heater0_4/heatert_4
per_heater1_4 = heater1_4/heatert_4
floor_heater4 = data_bems_141.iloc[18292:19731,2]
floor_heater0_4 = floor_heater4.value_counts()[0]
floor_heater1_4 = floor_heater4.value_counts()[1]
floor_heatert_4 = floor_heater0_4 + floor_heater1_4
per_floor_heater0_4 = floor_heater0_4/floor_heatert_4
per_floor_heater1_4 = floor_heater1_4/floor_heatert_4



heater5 = data_bems_141.iloc[19732:21171,1]
heater0_5 = 0
heater1_5 = heater5.value_counts()[1]
heatert_5 = heater0_5 + heater1_5
per_heater0_5 = heater0_5/heatert_5
per_heater1_5 = heater1_5/heatert_5
floor_heater5 = data_bems_141.iloc[19732:21171,1]
floor_heater0_5 = 0
floor_heater1_5 = floor_heater5.value_counts()[1]
floor_heatert_5 = floor_heater0_5 + floor_heater1_5
per_floor_heater0_5 = floor_heater0_5/floor_heatert_5
per_floor_heater1_5 = floor_heater1_5/floor_heatert_5



heater6 = data_bems_141.iloc[21172:22611,1]
heater0_6 = 0
heater1_6 = heater6.value_counts()[1]
heatert_6 = heater0_6 + heater1_6
per_heater0_6 = heater0_6/heatert_6
per_heater1_6 = heater1_6/heatert_6
floor_heater6 = data_bems_141.iloc[21172:22611,2]
floor_heater0_6 = floor_heater6.value_counts()[0]
print(floor_heater0_6)
floor_heater1_6 = 0
print(floor_heater1_6)
floor_heatert_6 = floor_heater0_6 + floor_heater1_6
print(floor_heatert_6)
per_floor_heater0_6 = floor_heater0_6/floor_heatert_6
print()
per_floor_heater1_6 = floor_heater1_6/floor_heatert_6




heater8 = data_bems_141.iloc[22612:24051,1]
heater0_8 = heater8.value_counts()[0]
heater1_8 = heater8.value_counts()[1]
heatert_8 = heater0_8 + heater1_8
per_heater0_8 = heater0_8/heatert_8
per_heater1_8 = heater1_8/heatert_8
floor_heater8 = data_bems_141.iloc[22612:24051,2]
floor_heater0_8 = floor_heater8.value_counts()[0]
floor_heater1_8 = 0
floor_heatert_8 = floor_heater0_8 + floor_heater1_8
per_floor_heater0_8 = floor_heater0_8/floor_heatert_8
per_floor_heater1_8 = floor_heater1_8/floor_heatert_8



heater9 = data_bems_141.iloc[24052:25491,1]
heater0_9 = heater9.value_counts()[0]
heater1_9 = heater9.value_counts()[1]
heatert_9 = heater0_9 + heater1_9
per_heater0_9 = heater0_9/heatert_9
per_heater1_9 = heater1_9/heatert_9
floor_heater9 = data_bems_141.iloc[24052:25491,2]
floor_heater0_9 = floor_heater9.value_counts()[0]
floor_heater1_9 = 0
floor_heatert_9 = floor_heater0_9 + floor_heater1_9
per_floor_heater0_9 = floor_heater0_9/floor_heatert_9
per_floor_heater1_9 = floor_heater1_9/floor_heatert_9




heater10 = data_bems_141.iloc[28312:29751,1]
heater0_10 = 0
heater1_10 = heater10.value_counts()[1]
heatert_10 = heater0_10 + heater1_10
per_heater0_10 = heater0_10/heatert_10
per_heater1_10 = heater1_10/heatert_10
floor_heater10 = data_bems_141.iloc[28312:29751,2]
floor_heater0_10 = floor_heater10.value_counts()[0]
floor_heater1_10 = 0
floor_heatert_10 = floor_heater0_10 + floor_heater1_10
per_floor_heater0_10 = floor_heater0_10/floor_heatert_10
per_floor_heater1_10 = floor_heater1_10/floor_heatert_10



heater11 = data_bems_141.iloc[29752:31191,1]
heater0_11 = 0
heater1_11 = heater11.value_counts()[1]
heatert_11 = heater0_11 + heater1_11
per_heater0_11 = heater0_11/heatert_11
per_heater1_11 = heater1_11/heatert_11
floor_heater11 = data_bems_141.iloc[29752:31191,2]
floor_heater0_11 = floor_heater11.value_counts()[0]
floor_heater1_11 = 0
floor_heatert_11 = floor_heater0_11 + floor_heater1_11
per_floor_heater0_11 = floor_heater0_11/floor_heatert_11
per_floor_heater1_11 = floor_heater1_11/floor_heatert_11




heater12 = data_bems_141.iloc[31192:32631,1]
heater0_12 = 0
heater1_12 = heater12.value_counts()[1]
heatert_12 = heater0_12 + heater1_12
per_heater0_12 = heater0_12/heatert_12
per_heater1_12 = heater1_12/heatert_12
floor_heater12 = data_bems_141.iloc[31192:32631,1]
floor_heater0_12 = floor_heater11.value_counts()[0]
floor_heater1_12 = 0
floor_heatert_12 = floor_heater0_12 + floor_heater1_12
per_floor_heater0_12 = floor_heater0_12/floor_heatert_12
per_floor_heater1_12 = floor_heater1_12/floor_heatert_12



heater15 = data_bems_141.iloc[32632:34071,1]
heater0_15 = 0
heater1_15 = heater15.value_counts()[1]
heatert_15 = heater0_15 + heater1_15
per_heater0_15 = heater0_15/heatert_15
per_heater1_15 = heater1_15/heatert_15
floor_heater15 = data_bems_141.iloc[32632:34071,2]
floor_heater0_15 = floor_heater15.value_counts()[0]
floor_heater1_15 = floor_heater15.value_counts()[1]
floor_heatert_15 = floor_heater0_15 + floor_heater1_15
per_floor_heater0_15 = floor_heater0_15/floor_heatert_15
per_floor_heater1_15 = floor_heater1_15/floor_heatert_15


heater16 = data_bems_141.iloc[34072:35511,1]
heater0_16 = 0
heater1_16 = heater16.value_counts()[1]
heatert_16 = heater0_16 + heater1_16
per_heater0_16 = heater0_16/heatert_16
per_heater1_16 = heater1_16/heatert_16
floor_heater16 = data_bems_141.iloc[34072:35511,2]
floor_heater0_16 = floor_heater16.value_counts()[0]
floor_heater1_16 = floor_heater16.value_counts()[1]
floor_heatert_16 = floor_heater0_16 + floor_heater1_16
per_floor_heater0_16 = floor_heater0_16/floor_heatert_16
per_floor_heater1_16 = floor_heater1_16/floor_heatert_16


heater17 = data_bems_141.iloc[49913:51344,1]
heater0_17 = heater17.value_counts()[0]
heater1_17 = heater17.value_counts()[1]
heatert_17 = heater0_17 + heater1_17
per_heater0_17 = heater0_17/heatert_17
per_heater1_17 = heater1_17/heatert_17
floor_heater17 = data_bems_141.iloc[49913:51344,2]
floor_heater0_17 = floor_heater17.value_counts()[0]
floor_heater1_17 = floor_heater17.value_counts()[1]
floor_heatert_17 = floor_heater0_17 + floor_heater1_17
per_floor_heater0_17 = floor_heater0_17/floor_heatert_17
per_floor_heater1_17 = floor_heater1_17/floor_heatert_17


heater18 = data_bems_141.iloc[51345:52780,1]
heater0_18 = heater18.value_counts()[0]
heater1_18 = 0
heatert_18 = heater0_18 + heater1_18
per_heater0_18 = heater0_18/heatert_18
per_heater1_18 = heater1_18/heatert_18
floor_heater18 = data_bems_141.iloc[51345:52780,2]
floor_heater0_18 = floor_heater18.value_counts()[0]
floor_heater1_18 = 0
floor_heatert_18 = floor_heater0_18 + floor_heater1_18
per_floor_heater0_18 = floor_heater0_18/floor_heatert_18
per_floor_heater1_18 = floor_heater1_18/floor_heatert_18

heater19 = data_bems_141.iloc[51345:52780,1]
heater0_19 = heater19.value_counts()[0]
heater1_19 = 0
heatert_19 = heater0_19 + heater1_19
per_heater0_19 = heater0_19/heatert_19
per_heater1_19 = heater1_19/heatert_19
floor_heater19 = data_bems_141.iloc[51345:52780,2]
floor_heater0_19 = floor_heater19.value_counts()[0]
floor_heater1_19 = 0
floor_heatert_19 = floor_heater0_19 + floor_heater1_19
per_floor_heater0_19 = floor_heater0_19/floor_heatert_19
per_floor_heater1_19 = floor_heater1_19/floor_heatert_19


p11 = [per_heater0_1,per_heater0_2,per_heater0_3,per_heater0_4,per_heater0_5,per_heater0_6,per_heater0_8,per_heater0_9,per_heater0_10,per_heater0_11,per_heater0_12,per_heater0_15,per_heater0_16,per_heater0_17,per_heater0_18,per_heater0_19] 
print(p11)
p22 = [per_heater1_1,per_heater1_2,per_heater1_3,per_heater1_4,per_heater1_5,per_heater1_6,per_heater1_8,per_heater1_9,per_heater1_10,per_heater1_11,per_heater1_12,per_heater1_15,per_heater1_16,per_heater1_17,per_heater1_18,per_heater1_19] 
print(p22)
p33 = [per_floor_heater0_1,per_floor_heater0_2,per_floor_heater0_3,per_floor_heater0_4,per_floor_heater0_5,per_floor_heater0_6,per_floor_heater0_8,per_floor_heater0_9,per_floor_heater0_10,per_floor_heater0_11,per_floor_heater0_12,per_floor_heater0_15,per_floor_heater0_16,per_floor_heater0_17,per_floor_heater0_18,per_floor_heater0_19]
print(p33)
p44 = [per_floor_heater1_1,per_floor_heater1_2,per_floor_heater1_3,per_floor_heater1_4,per_floor_heater1_5,per_floor_heater1_6,per_floor_heater1_8,per_floor_heater1_9,per_floor_heater1_10,per_floor_heater1_11,per_floor_heater1_12,per_floor_heater1_15,per_floor_heater1_16,per_floor_heater1_17,per_floor_heater1_18,floor_heater1_19]
print(p44)


x_1 = np.array([p11])
y_1 = np.array([po3])
r_1 = np.corrcoef(x_1,y_1)
print('Percentage of partially dissatisfied and Percentage of time heater is not functioning ')
print(r_1[0,1])



x_2 = np.array([p11])
y_2 = np.array([po4])
r_2 = np.corrcoef(x_2,y_2)
print('Percentage of fully dissatisfied and Percentage of time heater is not functioning ')
print(r_2[0,1])

x_3 = np.array([p11])
y_3 = np.array([pt])
r_3 = np.corrcoef(x_3,y_3)
print('Percentage of total dissatisfied and Percentage of time heater is not functioning ')
print(r_3[0,1])

x_4 = np.array([p22])
y_4 = np.array([pt])
r_4 = np.corrcoef(x_4,y_4)
print('Percentage of total dissatisfied and Percentage of time heater is functioning ')
print(r_4[0,1])

x_5 = np.array([p22])
y_5 = np.array([po3])
r_5 = np.corrcoef(x_5,y_5)
print('Percentage of partially dissatisfied and Percentage of time heater is functioning ')
print(r_5[0,1])

x_6 = np.array([p22])
y_6 = np.array([po4])
r_6 = np.corrcoef(x_6,y_6)
print('Percentage of fully dissatisfied and Percentage of time heater is functioning ')
print(r_6[0,1])


x_7 = np.array([p33])
y_7 = np.array([po3])
r_7 = np.corrcoef(x_7,y_7)
print('Percentage of partially dissatisfied and Percentage of time floor heater is not functioning ')
print(r_7[0,1])

x_8 = np.array([p33])
y_8 = np.array([po4])
r_8 = np.corrcoef(x_8,y_8)
print('Percentage of fully dissatisfied and Percentage of time floor heater is not functioning')
print(r_8[0,1])

x_9 = np.array([p33])
y_9 = np.array([pt])
r_9 = np.corrcoef(x_9,y_9)
print('Percentage of total dissatisfied and Percentage of time floor heater is not functioning ')
print(r_9[0,1])


x_10 = np.array([p44])
y_10 = np.array([po3])
r_10 = np.corrcoef(x_10,y_10)
print('Percentage of partially dissatisfied and Percentage of time floor heater is functioning ')
print(r_10[0,1])

x_11 = np.array([p44])
y_11 = np.array([po4])
r_11 = np.corrcoef(x_11,y_11)
print('Percentage of fully dissatisfied and Percentage of time floor heater is functioning ')
print(r_11[0,1])

x_12 = np.array([p44])
y_12 = np.array([pt])
r_12 = np.corrcoef(x_12,y_12)
print('Percentage of total dissatisfied and Percentage of time floor heater is functioning')
print(r_12[0,1])

t = PrettyTable(['Variables', 'Correlation Coefficient'])
 
# To insert rows:
t.add_row(['Percentage of fully dissatisfied and Percentage of time heater is not functioning',r_2[0,1]])
t.add_row(['Percentage of fully dissatisfied and Percentage of time heater is functioning', r_6[0,1]])
t.add_row(['Percentage of fully dissatisfied and Percentage of time floor heater is not functioning',r_8[0,1]])
t.add_row(['Percentage of fully dissatisfied and Percentage of time floor heater is functioning ', r_11[0,1]])

print(t)




#fig, ax = plt.subplots(figsize = (12, 8))
#plt.title('Relative Humidity (%) vs Percentage Dissatisfied due to electric shock PD(%)',fontsize =20)

#ax2 = ax.twinx()
#ax.plot(Days, rhd, color = 'g')
#print(rhd)
#print(rhdn)
#ax2.plot(Days, ele_p, color = 'b')
#print(ele_p)

#ax.set_xlabel('Days', color = 'r',fontsize =20)
#ax.set_ylabel('Relative Humidity %', color = 'g',fontsize =20)
 

#ax2.set_ylabel('Percentage Dissatisfied due to electric shock PD (%)', color = 'b',fontsize =20)
 
#plt.tight_layout()
 
#plt.grid()
#plt.show()


#print('ppd measured and pd calculated')
#print(results1["ppd"])
#print(col_hot_p)
plt.figure(figsize=(10, 10))

plt.scatter(sorted(co2d),sorted(PDc),color='r',label = 'CO2(ppm) and Percentage Dissatisfied')
plt.plot(sorted(co2d),sorted(PDc),color='r')
plt.axvline(x = 950, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(950, 6),fontsize=12,rotation=90)
plt.axvline(x = 1200, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(1200, 6),fontsize=12,rotation=90)
plt.axvline(x = 1750, color = 'r', linestyle = '-')
plt.annotate('Category C&D ',
            xy=(1750, 6),fontsize=12,rotation=90)

plt.xlabel('CO2 (ppm)',fontsize=20)
plt.ylabel('Percentage Dissatisfied due to air quality',fontsize=20)
plt.title('Relationship between Percentage Dissatisfied due to air quality',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


# -*- coding: utf-8 -*-
"""
Created on Mon Nov  6 10:54:33 2023

@author: aayamc
"""

import pandas as pd 
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt 
import plotly.graph_objects as go
import plotly.offline as pyo
import statistics 
from pythermalcomfort.models import pmv_ppd 
from pythermalcomfort.utilities import v_relative, clo_dynamic
from scipy import stats as st




Øyra_i = pd.read_csv('øyra_302_230313_163800_nilu_noserialnumber.csv',encoding='latin1')
Øyra_i.info()
Øyra_i.head()




day1 = Øyra_i.iloc[3:61
, 10]

day1B = 0
print('Number of dissatisfied vote')
print(day1B)
day1P = day1.value_counts()[3]
print('Number of dissatisfied vote')
print(day1P)
t_1= 100
p_11 = (day1B/100) * 100
p_12 = (day1P/100) * 100
P_1 = p_11 + p_12

ACC1 = statistics.mean(Øyra_i.iloc[3:61
, 9])
print('The ACC is')
print(ACC1)
PD_air1 = (np.exp(-0.18 - 5.28 * ACC1))/(1 + np.exp(-0.18 - 5.28 * ACC1))  * 100
print('the pd air is ')
print(PD_air1)
decipol_1 = 112 * (np.log (PD_air1)- 5.98)**(-4)
print(decipol_1)
m_col_hot_1 = statistics.mean(Øyra_i.iloc[3:61
, 19])
PD_elec_1 = 0
PD_draw_1 = 0
PD_coldfloor_1 = 0
PD_heatsun_1 = 0
PD_heater_1 = 0
PPD_m_col_hot_1 = (100 - 95 * np.exp(-0.03353 * m_col_hot_1**4 - 0.2179 * m_col_hot_1**2))

PD_smell1 = (Øyra_i.iloc[3:61
, 14].value_counts()[1]/(Øyra_i.iloc[3:61
, 14].value_counts()[1]+Øyra_i.iloc[3:61
, 14].value_counts()[0]))*100
PD_heavy1 = (Øyra_i.iloc[3:61
, 15].value_counts()[1]/(Øyra_i.iloc[3:61
, 15].value_counts()[1]+Øyra_i.iloc[3:61
, 15].value_counts()[0]))*100
PD_dry1 = (Øyra_i.iloc[3:61
, 16].value_counts()[1]/(Øyra_i.iloc[3:61
, 16].value_counts()[1]+Øyra_i.iloc[3:61
, 16].value_counts()[0]))*100
PD_dust1 = 0


Per_t_1 = PD_elec_1 + PD_draw_1 + PD_coldfloor_1 + PD_heatsun_1 + PD_heater_1 + PPD_m_col_hot_1

Per_PD_elec_1 = PD_elec_1 / Per_t_1
Per_PD_draw_1 = PD_draw_1 / Per_t_1
Per_PD_coldfloor_1 = PD_coldfloor_1 / Per_t_1
Per_PD_heatsun_1 = 0 
Per_PD_heater_1 = PD_heater_1 / Per_t_1
Per_PPD_m_col_hot_1 = PPD_m_col_hot_1 / Per_t_1

Per_ta_1 = PD_smell1 + PD_heavy1 + PD_dry1 + PD_dust1
Per_PD_smell1 = PD_smell1 / Per_ta_1
Per_PD_heavy1 = PD_heavy1 / Per_ta_1
Per_PD_dry1 = PD_dry1 / Per_ta_1
Per_PD_dust1 = PD_dust1 / Per_ta_1


day2 = Øyra_i.iloc[63:88
, 10]
print('its here')
print(day2)

day2B = day2.value_counts()[4]
print('Number of dissatisfied vote')
print(day2B)
day2P = day2.value_counts()[3]
print('Number of dissatisfied vote')
print(day2P)
t_2= 50
p_21 = (day2B/50) * 100
p_22 = (day2P/50) * 100
P_2 = p_21 + p_22


ACC2 = statistics.mean(Øyra_i.iloc[63:88
, 9])
PD_air2 = (np.exp(-0.18 - 5.28 * ACC2))/(1 + np.exp(-0.18 - 5.28 * ACC2))  * 100
decipol_2 = 112 * (np.log (PD_air2)- 5.98)**(-4)

m_col_hot_2 = statistics.mean(Øyra_i.iloc[63:88
, 19])
print(m_col_hot_2)
PD_elec_2 = (Øyra_i.iloc[63:88
, 18].value_counts()[1]/(Øyra_i.iloc[63:88
, 18].value_counts()[1]+Øyra_i.iloc[63:88
, 18].value_counts()[0]))*100
PD_draw_2 = (Øyra_i.iloc[63:88
, 20].value_counts()[1]/(Øyra_i.iloc[63:88
, 20].value_counts()[1]+Øyra_i.iloc[63:88
, 20].value_counts()[0]))*100
PD_coldfloor_2 = (Øyra_i.iloc[63:88
, 21].value_counts()[1]/(Øyra_i.iloc[63:88
, 21].value_counts()[1]+Øyra_i.iloc[63:88
, 21].value_counts()[0]))*100
PD_heatsun_2 = (Øyra_i.iloc[63:88
, 22].value_counts()[1]/(Øyra_i.iloc[63:88
, 22].value_counts()[1]+Øyra_i.iloc[63:88
, 22].value_counts()[0]))*100
PD_heater_2 = (Øyra_i.iloc[63:88
, 23].value_counts()[1]/(Øyra_i.iloc[63:88
, 23].value_counts()[1]+Øyra_i.iloc[63:88
, 23].value_counts()[0]))*100
PPD_m_col_hot_2 = (100 - 95 * np.exp(-0.03353 * m_col_hot_2**4 - 0.2179 * m_col_hot_2**2))


PD_smell2 = 0
PD_heavy2 = (Øyra_i.iloc[63:88
, 15].value_counts()[1]/(Øyra_i.iloc[63:88
, 15].value_counts()[1]+Øyra_i.iloc[63:88
, 15].value_counts()[0]))*100
PD_dry2 = (Øyra_i.iloc[63:88
, 16].value_counts()[1]/(Øyra_i.iloc[63:88
, 16].value_counts()[1]+Øyra_i.iloc[63:88
, 16].value_counts()[0]))*100
PD_dust2 = (Øyra_i.iloc[63:88
, 17].value_counts()[1]/(Øyra_i.iloc[63:88
, 17].value_counts()[1]+Øyra_i.iloc[63:88
, 17].value_counts()[0]))*100



Per_t_2 = PD_elec_2 + PD_draw_2 + PD_coldfloor_2 + PD_heatsun_2 + PD_heater_2 + PPD_m_col_hot_2
Per_ta_2 = PD_smell2 + PD_heavy2 + PD_dry2 + PD_dust2
Per_PD_smell2 = PD_smell2 / Per_ta_2
Per_PD_heavy2 = PD_heavy2 / Per_ta_2
Per_PD_dry2 = PD_dry2 / Per_ta_2
Per_PD_dust2 = PD_dust2 / Per_ta_2

Per_PD_elec_2 = PD_elec_2 / Per_t_2
Per_PD_draw_2 = PD_draw_2 / Per_t_2
Per_PD_coldfloor_2 = PD_coldfloor_2 / Per_t_2
Per_PD_heatsun_2 = PD_heatsun_2 / Per_t_2
Per_PD_heater_2 = PD_heater_2 / Per_t_2
Per_PPD_m_col_hot_2 = PPD_m_col_hot_2 / Per_t_2

day3 = Øyra_i.iloc[89:123
, 10]

day3B = day3.value_counts()[4]
print('Number of dissatisfied vote')
print(day3B)
day3P = day3.value_counts()[3]
print('Number of dissatisfied vote')
print(day3P)
t_3= 205 - 152
p_31 = (day3B/t_3) * 100
p_32 = (day3P/t_3) * 100
P_3 = p_31 + p_32


ACC3 = statistics.mean(Øyra_i.iloc[89:123
, 9])
PD_air3 = (np.exp(-0.18 - 5.28 * ACC3))/(1 + np.exp(-0.18 - 5.28 * ACC3))  * 100
decipol_3 = 112 * (np.log (PD_air3)- 5.98)**(-4)


m_col_hot_3 = statistics.mean(Øyra_i.iloc[89:123
, 19])
print(m_col_hot_3)
PD_elec_3 = (Øyra_i.iloc[89:123
, 18].value_counts()[1]/(Øyra_i.iloc[89:123
, 18].value_counts()[1]+Øyra_i.iloc[89:123
, 18].value_counts()[0]))*100
PD_draw_3 = (Øyra_i.iloc[89:123
, 20].value_counts()[1]/(Øyra_i.iloc[89:123
, 20].value_counts()[1]+Øyra_i.iloc[89:123
, 20].value_counts()[0]))*100
PD_coldfloor_3 = (Øyra_i.iloc[89:123
, 21].value_counts()[1]/(Øyra_i.iloc[89:123
, 21].value_counts()[1]+Øyra_i.iloc[89:123
, 21].value_counts()[0]))*100
PD_heatsun_3 = (Øyra_i.iloc[89:123
, 22].value_counts()[1]/(Øyra_i.iloc[89:123
, 22].value_counts()[1]+Øyra_i.iloc[89:123
, 22].value_counts()[0]))*100
PD_heater_3 = (Øyra_i.iloc[89:123
, 23].value_counts()[1]/(Øyra_i.iloc[89:123
, 23].value_counts()[1]+Øyra_i.iloc[89:123
, 23].value_counts()[0]))*100
PPD_m_col_hot_3 = (100 - 95 * np.exp(-0.03353 * m_col_hot_3**4 - 0.2179 * m_col_hot_3**2))



PD_smell3 = (Øyra_i.iloc[89:123
, 14].value_counts()[1]/(Øyra_i.iloc[89:123
, 14].value_counts()[1]+Øyra_i.iloc[89:123
, 14].value_counts()[0]))*100
PD_heavy3 = (Øyra_i.iloc[89:123
, 15].value_counts()[1]/(Øyra_i.iloc[89:123
, 15].value_counts()[1]+Øyra_i.iloc[89:123
, 15].value_counts()[0]))*100
PD_dry3 = (Øyra_i.iloc[89:123
, 16].value_counts()[1]/(Øyra_i.iloc[89:123
, 16].value_counts()[1]+Øyra_i.iloc[89:123
, 16].value_counts()[0]))*100
PD_dust3 = (Øyra_i.iloc[89:123
, 17].value_counts()[1]/(Øyra_i.iloc[89:123
, 17].value_counts()[1]+Øyra_i.iloc[89:123
, 17].value_counts()[0]))*100


Per_t_3 = PD_elec_3 + PD_draw_3 + PD_coldfloor_3 + PD_heatsun_3 + PD_heater_3 + PPD_m_col_hot_3
Per_ta_3 = PD_smell3 + PD_heavy3 + PD_dry3 + PD_dust3
Per_PD_elec_3 = PD_elec_3 / Per_t_3
Per_PD_draw_3 = PD_draw_3 / Per_t_3
Per_PD_coldfloor_3 = PD_coldfloor_3 / Per_t_3
Per_PD_heatsun_3 = PD_heatsun_3 / Per_t_3
Per_PD_heater_3 = PD_heater_3 / Per_t_3
Per_PPD_m_col_hot_3 = PPD_m_col_hot_3 / Per_t_3


Per_ta_3 = PD_smell3 + PD_heavy3 + PD_dry3 + PD_dust3
Per_PD_smell3 = PD_smell3 / Per_ta_3
Per_PD_heavy3 = PD_heavy3 / Per_ta_3
Per_PD_dry3 = PD_dry3 / Per_ta_3
Per_PD_dust3 = PD_dust3 / Per_ta_3

day4 = Øyra_i.iloc[124:140
, 10]

day4B = 0
print('Number of dissatisfied vote')
print(day4B)
day4P = 0
print('Number of dissatisfied vote')
print(day4P)
t_4= 253 - 206
p_41 = (day4B/t_4) * 100
p_42 = (day4P/t_4) * 100
P_4 = p_41 + p_42

ACC4 = statistics.mean(Øyra_i.iloc[124:140
, 9])
PD_air4 = (np.exp(-0.18 - 5.28 * ACC4))/(1 + np.exp(-0.18 - 5.28 * ACC4))  * 100
decipol_4 = 112 * (np.log (PD_air4)- 5.98)**(-4)



PD_elec_4 = 0
PD_draw_4 = 0
PD_coldfloor_4 = 0
PD_heatsun_4 = 0
PD_heater_4 = 0


m_col_hot_4 = statistics.mean(Øyra_i.iloc[124:140
, 19])
print(m_col_hot_4)



PPD_m_col_hot_4 = (100 - 95 * np.exp(-0.03353 * m_col_hot_4**4 - 0.2179 * m_col_hot_4**2))

PD_smell4 = 0
PD_heavy4 = 0
PD_dry4 = 0
PD_dust4 = 0



Per_t_4 = PD_elec_4 + PD_draw_4 + PD_coldfloor_4 + PD_heatsun_4 + PD_heater_4 + PPD_m_col_hot_4

Per_PD_elec_4 = PD_elec_4 / Per_t_4
Per_PD_draw_4 = PD_draw_4 / Per_t_4
Per_PD_coldfloor_4 = PD_coldfloor_4 / Per_t_4
Per_PD_heatsun_4 = PD_heatsun_4 / Per_t_4
Per_PD_heater_4 = PD_heater_4 / Per_t_4
Per_PPD_m_col_hot_4 = PPD_m_col_hot_4 / Per_t_4


Per_ta_4 = PD_smell4 + PD_heavy4 + PD_dry4 + PD_dust4
Per_PD_smell4 = 0
Per_PD_heavy4 = 0
Per_PD_dry4 = 0
Per_PD_dust4 = 0

day5 = Øyra_i.iloc[141:146
, 10]

day5B = 0
print('Number of dissatisfied vote')
print(day5B)
day5P = day5.value_counts()[3]
print('Number of dissatisfied vote')
print(day5P)
t_5= 323 - 254
p_51 = (day5B/t_5) * 100
p_52 = (day5P/t_5) * 100
P_5 = p_51 + p_52

ACC5 = statistics.mean(Øyra_i.iloc[141:146
, 9])
PD_air5 = (np.exp(-0.18 - 5.28 * ACC5))/(1 + np.exp(-0.18 - 5.28 * ACC5))  * 100
decipol_5 = 112 * (np.log (PD_air5)- 5.98)**(-4)
m_col_hot_5 = statistics.mean(Øyra_i.iloc[141:146
, 19])
print(m_col_hot_5)


PD_elec_5 = 0
PD_draw_5 = 0
PD_coldfloor_5 = 0
PD_heatsun_5 = 0
PD_heater_5 = 0

PPD_m_col_hot_5 = (100 - 95 * np.exp(-0.03353 * m_col_hot_5**4 - 0.2179 * m_col_hot_5**2))


PD_smell5 = 0
PD_heavy5 = 0
PD_dry5 = 0
PD_dust5 = 0


Per_ta_5 = PD_smell5 + PD_heavy5 + PD_dry5 + PD_dust5
Per_PD_smell5 = 0
Per_PD_heavy5 = 0
Per_PD_dry5 = 0
Per_PD_dust5 = 0

Per_t_5 = PD_elec_5 + PD_draw_5 + PD_coldfloor_5 + PD_heatsun_5 + PD_heater_5 + PPD_m_col_hot_5
Per_PD_elec_5 = PD_elec_5 / Per_t_5
Per_PD_draw_5 = PD_draw_5 / Per_t_5
Per_PD_coldfloor_5 = PD_coldfloor_5 / Per_t_5
Per_PD_heatsun_5 = PD_heatsun_5 / Per_t_5
Per_PD_heater_5 = PD_heater_5 / Per_t_5
Per_PPD_m_col_hot_5 = PPD_m_col_hot_5 / Per_t_5

day6 = Øyra_i.iloc[147:178
, 10]

day6B = day6.value_counts()[4]
print('Number of dissatisfied vote')
print(day6B)
day6P = day6.value_counts()[3]
print('Number of dissatisfied vote')
print(day6P)
t_6= 370 - 324
p_61 = (day6B/t_6) * 100
p_62 = (day6P/t_6) * 100
P_6 = p_61 + p_62

ACC6 = statistics.mean(Øyra_i.iloc[147:178
, 9])
PD_air6 = (np.exp(-0.18 - 5.28 * ACC6))/(1 + np.exp(-0.18 - 5.28 * ACC6))  * 100
decipol_6 = 112 * (np.log (PD_air6)- 5.98)**(-4)


m_col_hot_6 = statistics.mean(Øyra_i.iloc[147:178
, 19])


PD_elec_6 = 0
PD_draw_6 = 0
PD_coldfloor_6 = (Øyra_i.iloc[147:178
, 21].value_counts()[1]/(Øyra_i.iloc[147:178
, 21].value_counts()[1]+Øyra_i.iloc[147:178
, 21].value_counts()[0]))*100
PD_heatsun_6 = 0
PD_heater_6 = 0
PPD_m_col_hot_6 = (100 - 95 * np.exp(-0.03353 * m_col_hot_6**4 - 0.2179 * m_col_hot_6**2))


PD_smell6 = (Øyra_i.iloc[147:178
, 14].value_counts()[1]/(Øyra_i.iloc[147:178
, 14].value_counts()[1]+Øyra_i.iloc[147:178
, 14].value_counts()[0]))*100
PD_heavy6 = (Øyra_i.iloc[147:178
, 15].value_counts()[1]/(Øyra_i.iloc[147:178
, 15].value_counts()[1]+Øyra_i.iloc[147:178
, 15].value_counts()[0]))*100
PD_dry6 = (Øyra_i.iloc[147:178
, 16].value_counts()[1]/(Øyra_i.iloc[147:178
, 16].value_counts()[1]+Øyra_i.iloc[147:178
, 16].value_counts()[0]))*100
PD_dust6 = (Øyra_i.iloc[147:178
, 17].value_counts()[1]/(Øyra_i.iloc[147:178
, 17].value_counts()[1]+Øyra_i.iloc[147:178
, 17].value_counts()[0]))*100


Per_t_6 = PD_elec_6 + PD_draw_6 + PD_coldfloor_6 + PD_heatsun_6 + PD_heater_6 + PPD_m_col_hot_6
Per_PD_elec_6 = PD_elec_6 / Per_t_6
Per_PD_draw_6 = PD_draw_6 / Per_t_6
Per_PD_coldfloor_6 = PD_coldfloor_6 / Per_t_6
Per_PD_heatsun_6 = PD_heatsun_6 / Per_t_6
Per_PD_heater_6 = PD_heater_6 / Per_t_6
Per_PPD_m_col_hot_6 = PPD_m_col_hot_6 / Per_t_6

Per_ta_6 = PD_smell6 + PD_heavy6 + PD_dry6 + PD_dust6
Per_PD_smell6 = PD_smell6 / Per_ta_6
Per_PD_heavy6 = PD_heavy6 / Per_ta_6
Per_PD_dry6 = PD_dry6 / Per_ta_6
Per_PD_dust6 = PD_dust6 / Per_ta_6


day7 = Øyra_i.iloc[179:209
, 10]

day7B = 0
print('Number of dissatisfied vote')
print(day7B)
day7P = day7.value_counts()[3]
print('Number of dissatisfied vote')
print(day7P)
t_7= 422 - 371
p_71 = (day7B/t_7) * 100
p_72 = (day7P/t_7) * 100
P_7 = p_71 + p_72

ACC7 = statistics.mean(Øyra_i.iloc[179:209
, 9])
PD_air7 = (np.exp(-0.18 - 5.28 * ACC7))/(1 + np.exp(-0.18 - 5.28 * ACC7))  * 100
decipol_7 = 112 * (np.log (PD_air7)- 5.98)**(-4)
m_col_hot_7 = statistics.mean(Øyra_i.iloc[179:209
, 19])
print(m_col_hot_7)



PD_elec_7 = 0
PD_draw_7 = 0
PD_coldfloor_7 = 0
PD_heatsun_7 = 0
PD_heater_7 = 0
PPD_m_col_hot_7 = (100 - 95 * np.exp(-0.03353 * m_col_hot_7 **4 - 0.2179 * m_col_hot_7 **2))

PD_smell7 = 0
PD_heavy7 = (Øyra_i.iloc[179:209
, 15].value_counts()[1]/(Øyra_i.iloc[179:209
, 15].value_counts()[1]+Øyra_i.iloc[179:209
, 15].value_counts()[0]))*100
PD_dry7 = (Øyra_i.iloc[179:209
, 16].value_counts()[1]/(Øyra_i.iloc[179:209
, 16].value_counts()[1]+Øyra_i.iloc[179:209
, 16].value_counts()[0]))*100
PD_dust7 = 0

Per_t_7 = PD_elec_7 + PD_draw_7 + PD_coldfloor_7 + PD_heatsun_7 + PD_heater_7 + PPD_m_col_hot_7
Per_PD_elec_7 = PD_elec_7 / Per_t_7
Per_PD_draw_7 = PD_draw_7 / Per_t_7
Per_PD_coldfloor_7 = PD_coldfloor_7 / Per_t_7
Per_PD_heatsun_7 = PD_heatsun_7 / Per_t_7
Per_PD_heater_7 = PD_heater_7 / Per_t_7
Per_PPD_m_col_hot_7 = PPD_m_col_hot_7 / Per_t_7

Per_ta_7 = PD_smell7 + PD_heavy7 + PD_dry7 + PD_dust7
Per_PD_smell7 = PD_smell7 / Per_ta_7
Per_PD_heavy7 = PD_heavy7 / Per_ta_7
Per_PD_dry7 = PD_dry7 / Per_ta_7
Per_PD_dust7 = PD_dust7 / Per_ta_7


day8 = Øyra_i.iloc[210:246
, 10]

day8B = day8.value_counts()[4]
print('Number of dissatisfied vote')
print(day8B)
day8P = day8.value_counts()[3]
print('Number of dissatisfied vote')
print(day8P)
t_8= 459 - 423
p_81 = (day8B/t_8) * 100
p_82 = (day8P/t_8) * 100
P_8 = p_81 + p_82


ACC8 = statistics.mean(Øyra_i.iloc[210:246
, 9])
PD_air8 = (np.exp(-0.18 - 5.28 * ACC8))/(1 + np.exp(-0.18 - 5.28 * ACC8))  * 100
decipol_8 = 112 * (np.log (PD_air8)- 5.98)**(-4)
PD_elec_8 = (Øyra_i.iloc[210:246
, 18].value_counts()[1]/(Øyra_i.iloc[210:246
, 18].value_counts()[1]+Øyra_i.iloc[210:246
, 18].value_counts()[0]))*100
PD_draw_8 = (Øyra_i.iloc[210:246
, 20].value_counts()[1]/(Øyra_i.iloc[210:246
, 20].value_counts()[1]+Øyra_i.iloc[210:246
, 20].value_counts()[0]))*100
PD_coldfloor_8 = (Øyra_i.iloc[210:246
, 21].value_counts()[1]/(Øyra_i.iloc[210:246
, 21].value_counts()[1]+Øyra_i.iloc[210:246
, 21].value_counts()[0]))*100
PD_heatsun_8 = (Øyra_i.iloc[210:246
, 22].value_counts()[1]/(Øyra_i.iloc[210:246
, 22].value_counts()[1]+Øyra_i.iloc[210:246
, 22].value_counts()[0]))*100
PD_heater_8 = (Øyra_i.iloc[210:246
, 23].value_counts()[1]/(Øyra_i.iloc[210:246
, 23].value_counts()[1]+Øyra_i.iloc[210:246
, 23].value_counts()[0]))*100



m_col_hot_8 = statistics.mean(Øyra_i.iloc[210:246
, 19])
print(m_col_hot_8)



PD_smell8 = (Øyra_i.iloc[210:246
, 14].value_counts()[1]/(Øyra_i.iloc[210:246
, 14].value_counts()[1]+Øyra_i.iloc[210:246
, 14].value_counts()[0]))*100
PD_heavy8 = (Øyra_i.iloc[210:246
, 15].value_counts()[1]/(Øyra_i.iloc[210:246
, 15].value_counts()[1]+Øyra_i.iloc[210:246
, 15].value_counts()[0]))*100
PD_dry8 = (Øyra_i.iloc[210:246
, 16].value_counts()[1]/(Øyra_i.iloc[210:246
, 16].value_counts()[1]+Øyra_i.iloc[210:246
, 16].value_counts()[0]))*100
PD_dust8 = (Øyra_i.iloc[210:246
, 17].value_counts()[1]/(Øyra_i.iloc[210:246
, 17].value_counts()[1]+Øyra_i.iloc[210:246
, 17].value_counts()[0]))*100




PPD_m_col_hot_8 = (100 - 95 * np.exp(-0.03353 * m_col_hot_8 **4 - 0.2179 * m_col_hot_8 **2))
Per_t_8 = PD_elec_8 + PD_draw_8 + PD_coldfloor_8 + PD_heatsun_8 + PD_heater_8 + PPD_m_col_hot_8
Per_PD_elec_8 = PD_elec_8 / Per_t_8
Per_PD_draw_8 = PD_draw_8 / Per_t_8
Per_PD_coldfloor_8 = PD_coldfloor_8 / Per_t_8
Per_PD_heatsun_8 = PD_heatsun_8 / Per_t_8
Per_PD_heater_8 = PD_heater_8 / Per_t_8
Per_PPD_m_col_hot_8 = PPD_m_col_hot_8 / Per_t_8

Per_ta_8 = PD_smell8 + PD_heavy8 + PD_dry8 + PD_dust8
Per_PD_smell8 = PD_smell8 / Per_ta_8
Per_PD_heavy8 = PD_heavy8 / Per_ta_8
Per_PD_dry8 = PD_dry8 / Per_ta_8
Per_PD_dust8 = PD_dust8 / Per_ta_8

day9 = Øyra_i.iloc[247:261
, 10]

day9B = day9.value_counts()[4]
print('Number of dissatisfied vote')
print(day9B)
day9P = day9.value_counts()[3]
print('Number of dissatisfied vote')
print(day9P)
t_9= 501 - 460
p_91 = (day9B/t_9) * 100
p_92 = (day9P/t_9) * 100
P_9 = p_91 + p_92


ACC9 = statistics.mean(Øyra_i.iloc[247:261
, 9])
PD_air9 = (np.exp(-0.18 - 5.28 * ACC9))/(1 + np.exp(-0.18 - 5.28 * ACC9))  * 100
decipol_9 = 112 * (np.log (PD_air9)- 5.98)**(-4)
PD_elec_9 = 0
PD_draw_9 = 0
PD_coldfloor_9 = 0
PD_heatsun_9 = 0
PD_heater_9 = (Øyra_i.iloc[247:261
, 23].value_counts()[1]/(Øyra_i.iloc[247:261
, 23].value_counts()[1]+Øyra_i.iloc[247:261
, 23].value_counts()[0]))*100



m_col_hot_9 = statistics.mean(Øyra_i.iloc[247:261
, 19])
print(m_col_hot_9)


PD_smell9 = 0
PD_heavy9 = 0
PD_dry9 = 0
PD_dust9 = 0




PPD_m_col_hot_9 = (100 - 95 * np.exp(-0.03353 * m_col_hot_9 **4 - 0.2179 * m_col_hot_9 **2))
Per_t_9 = PD_elec_9 + PD_draw_9 + PD_coldfloor_9 + PD_heatsun_9 + PD_heater_9 + PPD_m_col_hot_9
Per_PD_elec_9 = PD_elec_9 / Per_t_9
Per_PD_draw_9 = PD_draw_9 / Per_t_9
Per_PD_coldfloor_9 = PD_coldfloor_9 / Per_t_9
Per_PD_heatsun_9 = PD_heatsun_9 / Per_t_9
Per_PD_heater_9 = PD_heater_9 / Per_t_9
Per_PPD_m_col_hot_9 = PPD_m_col_hot_9 / Per_t_9

Per_ta_9 = PD_smell9 + PD_heavy9 + PD_dry9 + PD_dust9
Per_PD_smell9 = 0
Per_PD_heavy9 = 0
Per_PD_dry9 = 0
Per_PD_dust9 = 0

day10 = Øyra_i.iloc[262:294
, 10]

day10B = 0
print('Number of dissatisfied vote')
print(day10B)
day10P = day10.value_counts()[3]
print('Number of dissatisfied vote')
print(day10P)
t_10= 538 - 502
p_101 = (day10B/t_10) * 100
p_102 = (day10P/t_10) * 100
P_10 = p_101 + p_102

ACC10 = statistics.mean(Øyra_i.iloc[262:294
, 9])
PD_air10 = (np.exp(-0.18 - 5.28 * ACC10))/(1 + np.exp(-0.18 - 5.28 * ACC10))  * 100
decipol_10 = 112 * (np.log (PD_air10)- 5.98)**(-4)
m_col_hot_10 = statistics.mean(Øyra_i.iloc[262:294
, 19])
print(m_col_hot_10)


PD_elec_10 = 0
PD_draw_10 = 0
PD_coldfloor_10 = 0
PD_heatsun_10 = 0
PD_heater_10 = 0


PD_smell10 = 0
PD_heavy10 = 0
PD_dry10 = 0
PD_dust10 = 0




PPD_m_col_hot_10 = (100 - 95 * np.exp(-0.03353 * m_col_hot_10 **4 - 0.2179 * m_col_hot_10 **2))
Per_t_10 = PD_elec_10 + PD_draw_10 + PD_coldfloor_10 + PD_heatsun_10 + PD_heater_10 + PPD_m_col_hot_10
Per_PD_elec_10 = PD_elec_10 / Per_t_10
Per_PD_draw_10 = PD_draw_10 / Per_t_10
Per_PD_coldfloor_10 = PD_coldfloor_10 / Per_t_10
Per_PD_heatsun_10 = PD_heatsun_10 / Per_t_10
Per_PD_heater_10 = PD_heater_10 / Per_t_10
Per_PPD_m_col_hot_10 = PPD_m_col_hot_10 / Per_t_10


Per_ta_10 = PD_smell10 + PD_heavy10 + PD_dry10 + PD_dust10
Per_PD_smell10 = 0
Per_PD_heavy10 = 0
Per_PD_dry10 = 0
Per_PD_dust10 = 0

day11 = Øyra_i.iloc[295:317
, 10]

day11B = 0
print('Number of dissatisfied vote')
print(day11B)
day11P = day11.value_counts()[3]
print('Number of dissatisfied vote')
print(day11P)
t_11= 539-586
p_111 = (day11B/t_11) * 100
p_112 = (day11P/t_11) * 100
P_11 = p_111 + p_112


ACC11 = statistics.mean(Øyra_i.iloc[295:317
, 9])
PD_air11 = (np.exp(-0.18 - 5.28 * ACC11))/(1 + np.exp(-0.18 - 5.28 * ACC11))  * 100
decipol_11 = 112 * (np.log (PD_air11)- 5.98)**(-4)
PD_elec_11 = 0
PD_draw_11 = 0
PD_coldfloor_11 = 0
PD_heatsun_11 = 0
PD_heater_11 = 0



m_col_hot_11 = statistics.mean(Øyra_i.iloc[295:317
, 19])
print(m_col_hot_11)



PPD_m_col_hot_11 = (100 - 95 * np.exp(-0.03353 * m_col_hot_11 **4 - 0.2179 * m_col_hot_11 **2))

PD_smell11 = 0
PD_heavy11 = 0
PD_dry11 = 0
PD_dust11 = 0


Per_ta_11 = PD_smell11 + PD_heavy11 + PD_dry11 + PD_dust11
Per_PD_smell11 = 0
Per_PD_heavy11 = 0
Per_PD_dry11 = 0
Per_PD_dust11 = 0


PD_smell11 = 0
PD_heavy11 = 0
PD_dry11 = 0
PD_dust11 = 0



Per_t_11 = PD_elec_11 + PD_draw_11 + PD_coldfloor_11 + PD_heatsun_11 + PD_heater_11 + PPD_m_col_hot_11
Per_PD_elec_11 = PD_elec_11 / Per_t_11
Per_PD_draw_11 = PD_draw_11 / Per_t_11
Per_PD_coldfloor_11 = PD_coldfloor_11 / Per_t_11
Per_PD_heatsun_11 = PD_heatsun_11 / Per_t_11
Per_PD_heater_11 = PD_heater_11 / Per_t_11
Per_PPD_m_col_hot_11 = PPD_m_col_hot_11 / Per_t_11

day12 = Øyra_i.iloc[318:324
, 10]

day12B = 0
print('Number of dissatisfied vote')
print(day12B)
day12P = day12.value_counts()[3]
print('Number of dissatisfied vote')
print(day12P)
t_12 = 628 - 587
p_121 = (day12B/t_12) * 100
p_122 = (day12P/t_12) * 100
P_12 = p_121 + p_122

ACC12 = statistics.mean(Øyra_i.iloc[318:324
, 9])
PD_air12 = (np.exp(-0.18 - 5.28 * ACC12))/(1 + np.exp(-0.18 - 5.28 * ACC12))  * 100
decipol_12 = 112 * (np.log (PD_air12)- 5.98)**(-4)
PD_elec_12 = 0
PD_draw_12 = 0
PD_coldfloor_12 = 0
PD_heatsun_12 = 0
PD_heater_12 = 0


m_col_hot_12 = statistics.mean(Øyra_i.iloc[318:324
, 19])


PPD_m_col_hot_12 = (100 - 95 * np.exp(-0.03353 * m_col_hot_12 **4 - 0.2179 * m_col_hot_12 **2))


PD_smell12 = 0
PD_heavy12 = 0
PD_dry12 = 0
PD_dust12 = 0

Per_ta_12 = PD_smell12 + PD_heavy12 + PD_dry12 + PD_dust12
Per_PD_smell12 = 0
Per_PD_heavy12 = 0
Per_PD_dry12 = 0
Per_PD_dust12 = 0
Per_t_12 = PD_elec_12 + PD_draw_12 + PD_coldfloor_12 + PD_heatsun_12 + PD_heater_12 + PPD_m_col_hot_12
Per_PD_elec_12 = PD_elec_12 / Per_t_12
Per_PD_draw_12 = PD_draw_12 / Per_t_12
Per_PD_coldfloor_12 = PD_coldfloor_12 / Per_t_12
Per_PD_heatsun_12 = PD_heatsun_12 / Per_t_12
Per_PD_heater_12 = PD_heater_12 / Per_t_12
Per_PPD_m_col_hot_12 = PPD_m_col_hot_12 / Per_t_12

day13 = Øyra_i.iloc[325:356
, 10]

day13B = day13.value_counts()[4]
print('Number of dissatisfied vote')
print(day13B)
day13P = day13.value_counts()[3]
print('Number of dissatisfied vote')
print(day13P)
t_13 = 664 - 629
p_131 = (day13B/t_13) * 100
p_132 = (day13P/t_13) * 100
P_13 = p_131 + p_132


ACC13 = statistics.mean(Øyra_i.iloc[325:356
, 9])
PD_air13 = (np.exp(-0.18 - 5.28 * ACC13))/(1 + np.exp(-0.18 - 5.28 * ACC13))  * 100
decipol_13 = 112 * (np.log (PD_air13)- 5.98)**(-4)

PD_elec_13 = 0
PD_draw_13 = (Øyra_i.iloc[325:356
, 20].value_counts()[1]/(Øyra_i.iloc[325:356
, 20].value_counts()[1]+Øyra_i.iloc[325:356
, 20].value_counts()[0]))*100
PD_coldfloor_13 = 0
PD_heatsun_13 = 0
PD_heater_13 = 0

m_col_hot_13 = statistics.mean(Øyra_i.iloc[325:356
, 19])
print(m_col_hot_13)


PPD_m_col_hot_13 = (100 - 95 * np.exp(-0.03353 * m_col_hot_13 **4 - 0.2179 * m_col_hot_13 **2))


PD_smell13 = 0
PD_heavy13 = 0
PD_dry13 = 0
PD_dust13 = 0
Per_ta_13 = PD_smell13 + PD_heavy13 + PD_dry13 + PD_dust13
Per_PD_smell13 = 0
Per_PD_heavy13 = 0
Per_PD_dry13 = 0
Per_PD_dust13 = 0

Per_t_13 = PD_elec_13 + PD_draw_13 + PD_coldfloor_13 + PD_heatsun_13 + PD_heater_13 + PPD_m_col_hot_13
Per_PD_elec_13 = PD_elec_13 / Per_t_13
Per_PD_draw_13 = PD_draw_13 / Per_t_13
Per_PD_coldfloor_13 = PD_coldfloor_13 / Per_t_13
Per_PD_heatsun_13 = PD_heatsun_13 / Per_t_13
Per_PD_heater_13 = PD_heater_13 / Per_t_13
Per_PPD_m_col_hot_13 = PPD_m_col_hot_13 / Per_t_13

ele_p = [PD_elec_1,PD_elec_2,PD_elec_3,PD_elec_4,PD_elec_5,PD_elec_6,PD_elec_7,PD_elec_8,PD_elec_9,PD_elec_10,PD_elec_11,PD_elec_12,PD_elec_13]
col_hot_p = [PPD_m_col_hot_1, PPD_m_col_hot_2,PPD_m_col_hot_3,PPD_m_col_hot_4,PPD_m_col_hot_5,PPD_m_col_hot_6,PPD_m_col_hot_7,PPD_m_col_hot_8,PPD_m_col_hot_9,PPD_m_col_hot_10,PPD_m_col_hot_11,PPD_m_col_hot_12,PPD_m_col_hot_13]
draw_p = [PD_draw_1,PD_draw_2,PD_draw_3,PD_draw_4,PD_draw_5,PD_draw_6,PD_draw_7,PD_draw_8,PD_draw_9,PD_draw_10,PD_draw_11,PD_draw_12,PD_draw_13]
fcold_p = [PD_coldfloor_1,PD_coldfloor_2,PD_coldfloor_3,PD_coldfloor_4,PD_coldfloor_5,PD_coldfloor_6,PD_coldfloor_7,PD_coldfloor_8,PD_coldfloor_9,PD_coldfloor_10,PD_coldfloor_11,PD_coldfloor_12,PD_coldfloor_13]
t_sun_p = [PD_heatsun_1,PD_heatsun_2,PD_heatsun_3,PD_heatsun_4,PD_heatsun_5,PD_heatsun_6,PD_heatsun_7,PD_heatsun_8,PD_heatsun_9,PD_heatsun_10,PD_heatsun_11,PD_heatsun_12,PD_heatsun_13]
t_heater_p =[PD_heater_1,PD_heater_2,PD_heater_3,PD_heater_4,PD_heater_5,PD_heater_6,PD_heater_7,PD_heater_8,PD_heater_9,PD_heater_10,PD_heater_11,PD_heater_12, PD_heater_13]
PD_air = [PD_air1,PD_air2,PD_air3,PD_air4,PD_air5,PD_air6,PD_air7,PD_air8,PD_air9,PD_air10,PD_air11,PD_air12,PD_air13]
PD_smell = [PD_smell1, PD_smell2, PD_smell3, PD_smell4, PD_smell5, PD_smell6, PD_smell7, PD_smell8, PD_smell9, PD_smell10, PD_smell11, PD_smell12, PD_smell13]
PD_heavy = [PD_heavy1, PD_heavy2, PD_heavy3, PD_heavy4, PD_heavy5, PD_heavy6, PD_heavy7, PD_heavy8, PD_heavy9, PD_heavy10, PD_heavy11, PD_heavy12, PD_heavy13]
PD_dry = [PD_dry1, PD_dry2, PD_dry3, PD_dry4, PD_dry5, PD_dry6, PD_dry7, PD_dry8, PD_dry9, PD_dry10, PD_dry11, PD_dry12, PD_dry13]
PD_dust = [PD_dust1, PD_dust2, PD_dust3, PD_dust4, PD_dust5, PD_dust6, PD_dust7, PD_dust8, PD_dust9, PD_dust10, PD_dust11, PD_dust12, PD_dust13]






ele_p1 = [Per_PD_elec_1,Per_PD_elec_2,Per_PD_elec_3,Per_PD_elec_4,Per_PD_elec_5,Per_PD_elec_6,Per_PD_elec_7,Per_PD_elec_8,Per_PD_elec_9,Per_PD_elec_10,Per_PD_elec_11,Per_PD_elec_12,Per_PD_elec_13]
col_hot_p1 = [Per_PPD_m_col_hot_1, Per_PPD_m_col_hot_2,Per_PPD_m_col_hot_3,Per_PPD_m_col_hot_4,Per_PPD_m_col_hot_5,Per_PPD_m_col_hot_6,Per_PPD_m_col_hot_7,Per_PPD_m_col_hot_8,Per_PPD_m_col_hot_9,Per_PPD_m_col_hot_10,Per_PPD_m_col_hot_11,Per_PPD_m_col_hot_12,Per_PPD_m_col_hot_13]
draw_p1 = [Per_PD_draw_1,Per_PD_draw_2,Per_PD_draw_3,Per_PD_draw_4,Per_PD_draw_5,Per_PD_draw_6,Per_PD_draw_7,Per_PD_draw_8,Per_PD_draw_9,Per_PD_draw_10,Per_PD_draw_11,Per_PD_draw_12,Per_PD_draw_13]
fcold_p1 = [Per_PD_coldfloor_1,Per_PD_coldfloor_2,Per_PD_coldfloor_3,Per_PD_coldfloor_4,Per_PD_coldfloor_5,Per_PD_coldfloor_6,Per_PD_coldfloor_7,Per_PD_coldfloor_8,Per_PD_coldfloor_9,Per_PD_coldfloor_10,Per_PD_coldfloor_11,Per_PD_coldfloor_12,Per_PD_coldfloor_13]
t_sun_p1 = [Per_PD_heatsun_1,Per_PD_heatsun_2,Per_PD_heatsun_3,Per_PD_heatsun_4,Per_PD_heatsun_5,Per_PD_heatsun_6,Per_PD_heatsun_7,Per_PD_heatsun_8,Per_PD_heatsun_9,Per_PD_heatsun_10,Per_PD_heatsun_11,Per_PD_heatsun_12,Per_PD_heatsun_13]
t_heater_p1 =[Per_PD_heater_1,Per_PD_heater_2,Per_PD_heater_3,Per_PD_heater_4,Per_PD_heater_5,Per_PD_heater_6,Per_PD_heater_7,Per_PD_heater_8,Per_PD_heater_9,Per_PD_heater_10,Per_PD_heater_11,Per_PD_heater_12,Per_PD_heater_13]
decipol = [decipol_1,decipol_2,decipol_3,decipol_4,decipol_5,decipol_6,decipol_7,decipol_8,decipol_9,decipol_10,decipol_11,decipol_12,decipol_13]
P_PD_smell = [Per_PD_smell1,Per_PD_smell2,Per_PD_smell3,Per_PD_smell4,Per_PD_smell5,Per_PD_smell6,Per_PD_smell7,Per_PD_smell8,Per_PD_smell9,Per_PD_smell10,Per_PD_smell11,Per_PD_smell12,Per_PD_smell13]
P_PD_heavy = [Per_PD_heavy1,Per_PD_heavy2,Per_PD_heavy3,Per_PD_heavy4,Per_PD_heavy5,Per_PD_heavy6,Per_PD_heavy7,Per_PD_heavy8,Per_PD_heavy9,Per_PD_heavy10,Per_PD_heavy11,Per_PD_heavy12,Per_PD_heavy13]
P_PD_dry = [Per_PD_dry1,Per_PD_dry2,Per_PD_dry3,Per_PD_dry4,Per_PD_dry5,Per_PD_dry6,Per_PD_dry7,Per_PD_dry8,Per_PD_dry9,Per_PD_dry10,Per_PD_dry11,Per_PD_dry12,Per_PD_dry13]
P_PD_dust = [Per_PD_dust1,Per_PD_dust2,Per_PD_dust3,Per_PD_dust4,Per_PD_dust5,Per_PD_dust6,Per_PD_dust7,Per_PD_dust8,Per_PD_dust9,Per_PD_dust10,Per_PD_dust11,Per_PD_dust12,Per_PD_dust13]


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, ele_p1, color='r',hatch='/',label = 'Electric shock')
plt.bar(Days, col_hot_p1,bottom=ele_p1 ,color='b',hatch='O',label = 'Cold and hot')
plt.bar(Days, draw_p1,bottom = np.add(ele_p1,col_hot_p1),color='g',hatch='+',label = 'Draught')
plt.bar(Days, fcold_p1,bottom = np.add(np.add(ele_p1,col_hot_p1),draw_p1),color='k',hatch='x',label = 'Cold floor')
plt.bar(Days, t_sun_p1,bottom = np.add(np.add(np.add(ele_p1,col_hot_p1),draw_p1),fcold_p1),color='m',hatch='-',label = 'Heat from sun')
plt.bar(Days, t_heater_p1,bottom = np.add(np.add(np.add(np.add(ele_p1,col_hot_p1),draw_p1),fcold_p1),t_sun_p1),color='c',hatch='.',label = 'Heat from heater')
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied(%)',fontsize=20)
plt.title('Percentage distribution of dissatisfaction due to different aspects in temperature with respect to days',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()




plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, ele_p, color='r',hatch='/',label = 'Electric shock')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to electric shock',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, col_hot_p,color='b',hatch='O',label = 'Cold and hot')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 6, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(5, 6),fontsize=12)
plt.axhline(y = 10, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(5, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(5, 15),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to thermal state (cold/hot)',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, draw_p,color='g',hatch='+',label = 'Draught')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 10, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(0, 10),fontsize=12)
plt.axhline(y = 20, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(0, 20),fontsize=12)
plt.axhline(y = 30, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 30),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to draught',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, fcold_p,color='k',hatch='x',label = 'Cold floor')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 10, color = 'g', linestyle = '-')
plt.annotate('Category A&B',
            xy=(0, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 15),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to cold floor',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, t_sun_p,color='m',hatch='-',label = 'Heat from sun')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 5, color = 'g', linestyle = '-')
plt.annotate('Category A&B ',
            xy=(0, 5),fontsize=12)
plt.axhline(y = 10, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 10),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to sunlight',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, t_heater_p,color='c',hatch='.',label = 'Heat from heater')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 5, color = 'g', linestyle = '-')
plt.annotate('Category A&B ',
            xy=(0, 5),fontsize=12)
plt.axhline(y = 10, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(0, 10),fontsize=12)
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to heat from heater',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))

plt.scatter(sorted(decipol),sorted(PD_air),color='r',label = 'Decipol vs PD')
plt.plot(sorted(decipol),sorted(PD_air),color='r')
#add trendline to plot

plt.xlabel('Perceived air Quality (Ci)',fontsize=20)
plt.ylabel('Perceived Air Quality % Dissatisfied (PD)',fontsize=20)
plt.title('Relationship between perceived air quality dissatisfied (PD) % vs Perceived air quality',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, P_PD_smell, color='r',hatch='/',label = 'PD due to smell in air ')
plt.bar(Days, P_PD_heavy,bottom=P_PD_smell ,color='b',hatch='O',label = 'PD due to heavy air')
plt.bar(Days, P_PD_dry,bottom = np.add(P_PD_smell,P_PD_heavy),color='g',hatch='+',label = 'PD due to dry air')
plt.bar(Days, P_PD_dust,bottom = np.add(np.add(P_PD_smell,P_PD_heavy),P_PD_dry),color='k',hatch='x',label = 'PD due to dust in air')
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied(%)',fontsize=20)
plt.title('Percentage distribution of dissatisfaction due to different aspects in air with respect to days',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days, PD_smell, color='b',hatch='+',label = 'PD due to smell')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to smell in air',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days,PD_heavy , color='k',hatch='-',label = 'PD due to heavy air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to heavy air',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days,PD_dry, color='m',hatch='x',label = 'PD due to dry air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to dry air ',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()

plt.figure(figsize=(10, 10))
Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
plt.bar(Days,PD_dust, color='c',hatch='o',label = 'PD due to dust in air')
plt.yticks((0,5,10,15,20,25,30,35))
plt.xlabel('Days',fontsize=20)
plt.ylabel('Percentage Dissatisfied (%)',fontsize=20)
plt.title('Percentage dissatisfaction due to dust in air ',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()



Øyra_a = pd.read_csv('øyra_302_230224_133924_spacepro_2969034330.csv',encoding='latin1')
Øyra_a.info()
Øyra_a.head()

#Day1
temp_a1 = Øyra_a.iloc[10198:10317,8].mode().iloc[0]
print(temp_a1)
rh_a1 = Øyra_a.iloc[10198:10317, 11].mode().iloc[0]
print(rh_a1)
press_a1 = Øyra_a.iloc[10198:10317, 14].mode().iloc[0]
print(press_a1)
CO2_a1 = Øyra_a.iloc[10198:10317, 17].mode().iloc[0]
print(CO2_a1)
VOC_a1 = Øyra_a.iloc[10198:10317, 20].mode().iloc[0] 
print(VOC_a1)       
Lite_a1 = Øyra_a.iloc[10198:10317, 23].mode().iloc[0]
print(Lite_a1)
PM1_a1 = Øyra_a.iloc[10198:10317, 24].mode().iloc[0] 
print(PM1_a1)
PM25_a1 = Øyra_a.iloc[10198:10317, 25].mode().iloc[0]
print(PM25_a1)
Sound_a1 = Øyra_a.iloc[10198:10317, 28].mode().iloc[0]
print(Sound_a1)
PDc1 = 395 * np.exp(-15.15*(CO2_a1-400)**-0.25)
Draught1 = (34 - temp_a1)*0.4924


#Day2
temp_a2 = Øyra_a.iloc[11350:11493, 8].mode().iloc[0]
rh_a2 = Øyra_a.iloc[11350:11493, 11].mode().iloc[0]
press_a2 = Øyra_a.iloc[11350:11493, 14].mode().iloc[0]
CO2_a2 = Øyra_a.iloc[11350:11493, 17].mode().iloc[0]
VOC_a2 = Øyra_a.iloc[11350:11493, 20].mode().iloc[0]        
Lite_a2 = Øyra_a.iloc[11350:11493, 23].mode().iloc[0]
PM1_a2 = Øyra_a.iloc[11350:11493, 24].mode().iloc[0] 
PM25_a2 = Øyra_a.iloc[11350:11493, 25].mode().iloc[0]
Sound_a2 = Øyra_a.iloc[11350:11493, 28].mode().iloc[0]
PDc2 = 395 * np.exp(-15.15*(CO2_a2-400)**-0.25)
Draught2 = (34 - temp_a2)*0.4924 

 
#Day3
temp_a3 = Øyra_a.iloc[11926:12021, 8].mode().iloc[0]
rh_a3 = Øyra_a.iloc[11926:12021, 11].mode().iloc[0]
press_a3 = Øyra_a.iloc[11926:12021, 14].mode().iloc[0]
CO2_a3 = Øyra_a.iloc[11926:12021, 17].mode().iloc[0]
VOC_a3 = Øyra_a.iloc[11926:12021, 20].mode().iloc[0]        
Lite_a3 = Øyra_a.iloc[11926:12021, 23].mode().iloc[0]
PM1_a3 = Øyra_a.iloc[11926:12021, 24].mode().iloc[0] 
PM25_a3 = Øyra_a.iloc[11926:12021, 25].mode().iloc[0]
Sound_a3 = Øyra_a.iloc[11926:12021, 28].mode().iloc[0]
PDc3 = 395 * np.exp(-15.15*(CO2_a3-400)**-0.25)
Draught3 = (34 - temp_a3)*0.4924


#Day4
temp_a4 = Øyra_a.iloc[13654:13677, 8].mode().iloc[0]
rh_a4 = Øyra_a.iloc[13654:13677, 11].mode().iloc[0]
press_a4 = Øyra_a.iloc[13654:13677, 14].mode().iloc[0]
CO2_a4 = Øyra_a.iloc[13654:13677, 17].mode().iloc[0]
VOC_a4 = Øyra_a.iloc[13654:13677, 20].mode().iloc[0]        
Lite_a4 = Øyra_a.iloc[13654:13677, 23].mode().iloc[0]
PM1_a4 = Øyra_a.iloc[13654:13677, 24].mode().iloc[0] 
PM25_a4 = Øyra_a.iloc[13654:13677, 25].mode().iloc[0]
Sound_a4 = Øyra_a.iloc[13654:13677, 28].mode().iloc[0]
PDc4 = 395 * np.exp(-15.15*(CO2_a4-400)**-0.25)
Draught4 = (34 - temp_a4)*0.4924 


#Day5
temp_a5 = Øyra_a.iloc[14326:14349, 8].mode().iloc[0]
rh_a5 = Øyra_a.iloc[14326:14349, 11].mode().iloc[0]
press_a5 = Øyra_a.iloc[14326:14349, 14].mode().iloc[0]
CO2_a5 = Øyra_a.iloc[14326:14349, 17].mode().iloc[0]
VOC_a5 = Øyra_a.iloc[14326:14349, 20].mode().iloc[0]        
Lite_a5 = Øyra_a.iloc[14326:14349, 23].mode().iloc[0]
PM1_a5 = Øyra_a.iloc[14326:14349, 24].mode().iloc[0] 
PM25_a5 = Øyra_a.iloc[14326:14349, 25].mode().iloc[0]
Sound_a5 = Øyra_a.iloc[14326:14349, 28].mode().iloc[0]
PDc5 = 395 * np.exp(-15.15*(CO2_a5-400)**-0.25)
Draught5 = (34 - temp_a5)*0.4924

#Day6
temp_a6 = Øyra_a.iloc[14806:14949, 8].mode().iloc[0]
rh_a6 = Øyra_a.iloc[14806:14949, 11].mode().iloc[0]
press_a6 = Øyra_a.iloc[14806:14949, 14].mode().iloc[0]
CO2_a6 = Øyra_a.iloc[14806:14949, 17].mode().iloc[0]
VOC_a6 = Øyra_a.iloc[14806:14949, 20].mode().iloc[0]        
Lite_a6 = Øyra_a.iloc[14806:14949, 23].mode().iloc[0]
PM1_a6 = Øyra_a.iloc[14806:14949, 24].mode().iloc[0] 
PM25_a6 = Øyra_a.iloc[14806:14949, 25].mode().iloc[0]
Sound_a6 = Øyra_a.iloc[14806:14949, 28].mode().iloc[0]
PDc6 = 395 * np.exp(-15.15*(CO2_a6-400)**-0.25)
Draught6 = (34 - temp_a6)*0.4924

#Day7
temp_a7 = Øyra_a.iloc[15382:15525, 8].mode().iloc[0]
rh_a7 = Øyra_a.iloc[15382:15525, 11].mode().iloc[0]
press_a7 = Øyra_a.iloc[15382:15525, 14].mode().iloc[0]
CO2_a7 = Øyra_a.iloc[15382:15525, 17].mode().iloc[0]
VOC_a7 = Øyra_a.iloc[15382:15525, 20].mode().iloc[0]        
Lite_a7 = Øyra_a.iloc[15382:15525, 23].mode().iloc[0]
PM1_a7 = Øyra_a.iloc[15382:15525, 24].mode().iloc[0] 
PM25_a7 = Øyra_a.iloc[15382:15525, 25].mode().iloc[0]
Sound_a7 = Øyra_a.iloc[15382:15525, 28].mode().iloc[0]
PDc7 = 395 * np.exp(-15.15*(CO2_a7-400)**-0.25)
Draught7 = (34 - temp_a7)*0.4924


#Day8
temp_a8 = Øyra_a.iloc[15958:16077, 8].mode().iloc[0]
rh_a8 = Øyra_a.iloc[15958:16077, 11].mode().iloc[0]
press_a8 = Øyra_a.iloc[15958:16077, 14].mode().iloc[0]
CO2_a8 = Øyra_a.iloc[15958:16077, 17].mode().iloc[0]
VOC_a8 = Øyra_a.iloc[15958:16077, 20].mode().iloc[0]        
Lite_a8 = Øyra_a.iloc[15958:16077, 23].mode().iloc[0]
PM1_a8 = Øyra_a.iloc[15958:16077, 24].mode().iloc[0] 
PM25_a8 = Øyra_a.iloc[15958:16077, 25].mode().iloc[0]
Sound_a8 = Øyra_a.iloc[15958:16077, 28].mode().iloc[0]
PDc8 = 395 * np.exp(-15.15*(CO2_a8-400)**-0.25)
Draught8 = (34 - temp_a8)*0.4924


#Day9
temp_a9 = Øyra_a.iloc[17662:17685, 8].mode().iloc[0]
rh_a9 = Øyra_a.iloc[17662:17685, 11].mode().iloc[0]
press_a9 = Øyra_a.iloc[17662:17685, 14].mode().iloc[0]
CO2_a9 = Øyra_a.iloc[17662:17685, 17].mode().iloc[0]
VOC_a9 = Øyra_a.iloc[17662:17685, 20].mode().iloc[0]        
Lite_a9 = Øyra_a.iloc[17662:17685, 23].mode().iloc[0]
PM1_a9 = Øyra_a.iloc[17662:17685, 24].mode().iloc[0] 
PM25_a9 = Øyra_a.iloc[17662:17685, 25].mode().iloc[0]
Sound_a9 = Øyra_a.iloc[17662:17685, 28].mode().iloc[0]
PDc9 = 395 * np.exp(-15.15*(CO2_a9-400)**-0.25)
Draught9 = (34 - temp_a9)*0.4924

#Day10
temp_a10 = Øyra_a.iloc[18238:18357, 8].mode().iloc[0]
rh_a10 = Øyra_a.iloc[18238:18357, 11].mode().iloc[0]
press_a10 = Øyra_a.iloc[18238:18357, 14].mode().iloc[0]
CO2_a10 = Øyra_a.iloc[18238:18357, 17].mode().iloc[0]
VOC_a10 = Øyra_a.iloc[18238:18357, 20].mode().iloc[0]        
Lite_a10 = Øyra_a.iloc[18238:18357, 23].mode().iloc[0]
PM1_a10 = Øyra_a.iloc[18238:18357, 24].mode().iloc[0] 
PM25_a10 = Øyra_a.iloc[18238:18357, 25].mode().iloc[0]
Sound_a10 = Øyra_a.iloc[18238:18357, 28].mode().iloc[0]
PDc10 = 395 * np.exp(-15.15*(CO2_a10-400)**-0.25)
Draught10 = (34 - temp_a10)*0.4924

#Day11
temp_a11 = Øyra_a.iloc[18814:18957, 8].mode().iloc[0]
rh_a11 = Øyra_a.iloc[18814:18957, 11].mode().iloc[0]
press_a11 = Øyra_a.iloc[18814:18957, 14].mode().iloc[0]
CO2_a11 = Øyra_a.iloc[18814:18957, 17].mode().iloc[0]
VOC_a11 = Øyra_a.iloc[18814:18957, 20].mode().iloc[0]        
Lite_a11 = Øyra_a.iloc[18814:18957, 23].mode().iloc[0]
PM1_a11 = Øyra_a.iloc[18814:18957, 24].mode().iloc[0] 
PM25_a11 = Øyra_a.iloc[18814:18957, 25].mode().iloc[0]
Sound_a11 = Øyra_a.iloc[18814:18957, 28].mode().iloc[0]
PDc11 = 395 * np.exp(-15.15*(CO2_a11-400)**-0.25)
Draught11 = (34 - temp_a11)*0.4924

#Day12
temp_a12 = Øyra_a.iloc[19390:19413, 8].mode().iloc[0]
rh_a12 = Øyra_a.iloc[19390:19413, 11].mode().iloc[0]
press_a12 = Øyra_a.iloc[19390:19413, 14].mode().iloc[0]
CO2_a12 = Øyra_a.iloc[19390:19413, 17].mode().iloc[0]
VOC_a12 = Øyra_a.iloc[19390:19413, 20].mode().iloc[0]        
Lite_a12 = Øyra_a.iloc[19390:19413, 23].mode().iloc[0]
PM1_a12 = Øyra_a.iloc[19390:19413, 24].mode().iloc[0] 
PM25_a12 = Øyra_a.iloc[19390:19413, 25].mode().iloc[0]
Sound_a12 = Øyra_a.iloc[19390:19413, 28].mode().iloc[0]
PDc12 = 395 * np.exp(-15.15*(CO2_a12-400)**-0.25)
Draught12 = (34 - temp_a12)*0.4924


#Day13
temp_a13 = Øyra_a.iloc[19966:20085, 8].mode().iloc[0]
rh_a13 = Øyra_a.iloc[19966:20085, 11].mode().iloc[0]
press_a13 = Øyra_a.iloc[19966:20085, 14].mode().iloc[0]
CO2_a13 = Øyra_a.iloc[19966:20085, 17].mode().iloc[0]
VOC_a13 = Øyra_a.iloc[19966:20085, 20].mode().iloc[0]        
Lite_a13 = Øyra_a.iloc[19966:20085, 23].mode().iloc[0]
PM1_a13 = Øyra_a.iloc[19966:20085, 24].mode().iloc[0] 
PM25_a13 = Øyra_a.iloc[19966:20085, 25].mode().iloc[0]
Sound_a13 = Øyra_a.iloc[19966:20085, 28].mode().iloc[0]
PDc13 = 395 * np.exp(-15.15*(CO2_a13-400)**-0.25)
Draught13 = (34 - temp_a13)*0.4924


co2d = [CO2_a1,CO2_a2,CO2_a3,CO2_a4,CO2_a5,CO2_a6,CO2_a7,CO2_a8,CO2_a9,CO2_a10,CO2_a11,CO2_a12,CO2_a13]

PDc = [PDc1,PDc2,PDc3,PDc4,PDc5,PDc6,PDc7,PDc8,PDc9,PDc10,PDc11,PDc12,PDc13]

tempd = [temp_a1,temp_a2,temp_a3,temp_a4,temp_a5,temp_a6,temp_a7,temp_a8,temp_a9,temp_a10,temp_a11,temp_a12,temp_a13]
rhd = [rh_a1,rh_a2,rh_a3,rh_a4,rh_a5,rh_a6,rh_a7,rh_a8,rh_a9,rh_a10,rh_a11,rh_a12,rh_a13]
Draught = [Draught1,Draught2,Draught3,Draught4,Draught5,Draught6,Draught7,Draught8,Draught9,Draught10,Draught11,Draught12,Draught13]
tdb1 = tempd
tr1 = tdb1
rh1 = rhd
v1 = 0.1
met1 = 1.2
clo1 =1
  
#calculate relative air speed 
v_r1 = v_relative (v=v1, met=met1)

#calculate dynamic clothing
clo_d1 = clo_dynamic(clo=clo1, met=met1)
results1 = pmv_ppd(tdb=tdb1, tr=tr1, vr=v_r1, rh=rh1, met=met1, clo=clo_d1)

Days= ['D1','D2','D3','D4','D5','D6','D7','D8','D9','D10','D11','D12','D13']
#x_axisd = np.arange(len(Days))

#plt.figure(figsize=(10, 6))
#plt.plot(x_axisd,tempd,'g--')
#plt.axhline(y = 20, color = 'r', linestyle = '-') 
#plt.axhline(y = 22, color = 'g', linestyle = '-') 
#plt.axhline(y = 27, color = 'r', linestyle = '-') 
#plt.xlabel('Days',fontsize=20)
#plt.ylabel('Temperature (°C)',fontsize=20)
#plt.title('1st maximum occuring temperature (°C) with days',fontsize=20)
#plt.xticks(x_axisd,Days)
#plt.grid()
#plt.show()

#plt.figure(figsize=(10, 6))
#plt.plot(x_axisd,rhd,'g--')
#plt.axhline(y = 30, color = 'r', linestyle = '-')  
#plt.axhline(y = 70, color = 'r', linestyle = '-') 
#plt.xlabel('Days',fontsize=20)
#plt.ylabel('Relative Humidity (%)',fontsize=20)
#plt.title('1st maximum  occurring relative humidity (%) with days',fontsize=20)
#plt.xticks(x_axisd,Days)
#plt.grid()
#plt.show()

print('the pmv and ppd are')
print(results1["pmv"])
print(results1["ppd"])

PMVs = [-0.78,-0.78,-0.76,-0.76,-0.75,-0.74,-0.69,-0.69,-0.65,-0.64,-0.56,-0.55,-0.49]

PPDs = [17.8,17.7,17.3,17.1,16.9,16.4,15,14.9,13.8,13.6,11.5,11.4,10.1]

plt.figure(figsize=(10, 10))

plt.scatter(PMVs,PPDs,color='r',label = 'PMV vs PPD')
plt.plot(PMVs,PPDs,color='r')
plt.yticks((0,5,10,15,20,25,30,35))
plt.axhline(y = 6, color = 'g', linestyle = '-')
plt.annotate('Category A ',
            xy=(-0.65, 6),fontsize=12)
plt.axhline(y = 10, color = 'b', linestyle = '-')
plt.annotate('Category B ',
            xy=(-0.65, 10),fontsize=12)
plt.axhline(y = 15, color = 'r', linestyle = '-')
plt.annotate('Category C ',
            xy=(-0.65, 15),fontsize=12)
plt.xlabel('PMV',fontsize=20)
plt.ylabel('PPD (%)',fontsize=20)
plt.title('Relationship between Percentage Dissatisfied and PMV',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


plt.figure(figsize=(10, 10))

plt.scatter(sorted(co2d),sorted(PDc),color='r',label = 'CO2(ppm) and Percentage Dissatisfied')
plt.plot(sorted(co2d),sorted(PDc),color='r')
plt.axvline(x = 950, color = 'g', linestyle = '-')
plt.annotate('Category A',xy=(950, 6),fontsize=12,rotation=90)
plt.axvline(x = 1200, color = 'b', linestyle = '-')
plt.annotate('Category B',xy=(1200, 6),fontsize=12,rotation=90)
plt.axvline(x = 1750, color = 'r', linestyle = '-')
plt.annotate('Category C&D',xy=(1750, 6),fontsize=12,rotation=90)

plt.xlabel('CO2 (ppm)',fontsize=20)
plt.ylabel('Percentage Dissatisfied due to air quality',fontsize=20)
plt.title('Relationship between Percentage Dissatisfied due to air quality',fontsize=20)
plt.legend(loc='center left', bbox_to_anchor=(1.05, 0.8),fontsize=20)
plt.grid()
plt.show()


Øyra_b = pd.read_csv('øyra_302_230308_0006_sauter_noserialnumber.csv',encoding='latin1')
Øyra_b.info()
Øyra_b.head()

#Day1
temp_s1 = Øyra_b.iloc[8460:8760, 1].mode().iloc[0]
#Day2
temp_s2 = Øyra_b.iloc[11337:11697, 1].mode().iloc[0] 
#Day3
temp_s3 = Øyra_b.iloc[12777:13016, 1].mode().iloc[0]
#Day4
temp_s4 = Øyra_b.iloc[17097:17157, 1].mode().iloc[0]
#Day5
temp_s5 = Øyra_b.iloc[18777:18836, 1].mode().iloc[0]
#Day6
temp_s6 = Øyra_b.iloc[19977:20337, 1].mode().iloc[0]
#Day7
temp_s7 = Øyra_b.iloc[21417:21776, 1].mode().iloc[0]
#Day8
temp_s8 = Øyra_b.iloc[22857:23156, 1].mode().iloc[0]
#Day9
temp_s9 = Øyra_b.iloc[27057:27116, 1].mode().iloc[0]
#Day10
temp_s10 = Øyra_b.iloc[28497:28796, 1].mode().iloc[0]
#Day11
temp_s11 = Øyra_b.iloc[29937:30296, 1].mode().iloc[0]
#Day12
temp_s12 = Øyra_b.iloc[31377:31437, 1].mode().iloc[0]
#Day13
temp_s13 = Øyra_b.iloc[32817:33117, 1].mode().iloc[0]


print('PPD and cold hot ')
print(PPDs)
print(col_hot_p)



