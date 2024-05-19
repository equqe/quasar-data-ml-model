# quasar-data-ml-model
model based on an opensource astronomical dataset 
# still raw!!!

astroml+astropy, jupyter, numpy, matplotlib, scipy ... (the list is not full still)

the model uses SDSS quasars dataset, which includes right ascension, declination, redshift, the magnitude and its error(u+g+r+i+z, 2MASS J+H+K) and spectral object identifier of the quasar

dataset: https://classic.sdss.org/dr7/products/value_added/qsocat_dr7.php


## working with the data

first of all i wanted to take a look at the info about data: type, size and etc.

![image](https://github.com/equqe/quasar-data-ml-model/assets/145790372/32ed5d60-422f-42a4-96b8-e27ca0b57873)

as we see:

- there's 105783 rows and 21 columns, each corresponding to one feature of the quasar
- 80.95% of the features have the float32 type, 9.52% have the float64 type, 4.76% have the int64 type and another 4.76% have the object type
- there are no missing values, all columns have 105783 non-empty values

now let's look at the distribution of features (how many unique values there are in each feature):

![image](https://github.com/equqe/quasar-data-ml-model/assets/145790372/4b8e3718-d4e5-4859-9c40-7f048f1334d8)

tabular data analyses based on all of the info:

| Variable name        | Type           | Role       | Description                                                                                  | Values                   |
|----------------------|----------------|------------|----------------------------------------------------------------------------------------------|--------------------------|
| sdssID               | Categorical    | Identifier |  The identifier of the quasar in the SDSS                                                    | Strings of length 14     |
| RA                   | Numerical      | Feature    |  The right ascension of the quasar in degrees                                                | 0.027228-359.997675      |
| dec                  | Numerical      | Feature    |  The declination of the quasar in degrees                                                    | -17.520442-84.431413     |
| redshift             | Numerical      | Feature    |  The redshift of the quasar                                                                  | 0.064500-5.460800        |
| mag_u & err_u        | Numerical      | Feature    |  The magnitude and its error, measured in the u (ultraviolet) filter of the SDSS             | 0.000000-26.778999       |
| mag_g & err_g        | Numerical      | Feature    |  The magnitude and its error, measured in the g (green) filter of the SDSS                   | 0.000000-26.420000       |
| mag_r & err_r        | Numerical      | Feature    |  The magnitude and its error, measured in the r (red) filter of the SDSS                     | 0.000000-22.879000       |
| mag_i & err_i        | Numerical      | Feature    |  The magnitude and its error, measured in the i (infrared) filter of the SDSS                | 0.000000-17.465000       |
| mag_z & err_z        | Numerical      | Feature    |  The magnitude and its error, measured in the z (long-wavelength region) filter of the SDSS  | 0.000000-8.373411e+17    |
| mag_J & err_J        | Numerical      | Feature    |  The magnitude and its error, measured in the J (infrared) filter of the 2MASS system        | 0.000000-18.802000       |
| mag_H & err_H        | Numerical      | Feature    |  The magnitude and its error, measured in the H (infrared) filter of the 2MASS system        | 0.000000-17.886999       |
| mag_K & err_K        | Numerical      | Feature    |  The magnitude and its error, measured in the K (infrared) filter of the 2MASS system        | 0.000000-17.465000       |
| specobjid            | Categorical    | Identifier |  The spectral object identifier in the SDSS database                                         | 7.509409e+16-8.373411e+17|


## the magnitude and its error in SDSS and 2MASS filters(50 bins)

![image](https://github.com/equqe/astronomical-data-ml-model/assets/145790372/fb85f16f-2ab0-44e9-be6a-9f1146a93e13)





