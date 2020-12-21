# Increase the plegde of 4G sector and support 16G sector

### Brief intro

- 1. Increase the plegde of 4G sector
- 2. support 16G sector

### Summary

We have accumulated much development experience in tech since the launch of FiIecash by active participation of many members. We believe that long-term network operation and ability to adapting to the changes and challenges of the market out-competes short-term speculation, so that we have added 4G and 16G sectors to continue network stabilization and further development.

### Reason for such adjustment

- 1.Filecash becomes more friendly to small miners by adding the 4G sector, which ensures a lowered threshold for continuous stability. Participants will benefit from this much stabilized FIC ecology development.
- 2.More and more miners desire a larger sector after the on-lining of the 4G sectors. While stabilizing the 4G sectors, we now add 16G sector for improved network storage capacity and healthier development of FIC ecological economy.

### Technical specifications

##### Adjustment of 4G sector

- 1.Commit2 pledge
$$
ipBase = 20 \times \frac{SectorPower}{networkPower} \times CurrEpochReward\times Epochslnday
$$

$$
additionalIP = \frac{30}{100} \times CircSupply \times \frac{SectorPower}{networkPower}
$$

$$
initialPledge=Min (ipBase + additionalIP , SpaceRaceInitialPledgeMaxPerByte \times 4G \times  \frac{InitialFactorof4G}{InitialFactorDenom}) \times  \frac{110}{100}
$$


##### 16G sector added

- 1.Precommit pre-pledge
$$
collateralpre = 20 \times \frac{Sector}{Network} \times CurrEpochReward \times Epochslnday \times \frac{110}{100}
$$

- 2.Commit2 pledge
$$
initialPledge=Min (ipBase + additionalIP , SpaceRaceInitialPledgeMaxPerByte \times 4G \times  \frac{InitialFactorof16G}{InitialFactorDenom}) \times  \frac{110}{100}
$$

- 3.Release

$$
collateralpre - initialPledge
$$
