Steps to run the script
	1. Set Up the Treon sensors and Sql Database 
	Setting up: 
		1. Create MSQL database and insert the database details in the parameters
            	2. Create the following tables in the database:
                	a. treon_vibration_raw_data_1 (data_time, message)
                	b. treon_vibration_test_data (Date_time, Sensor_id, Temperature, Battery_voltage, X_P2P, X_RMS, X_Z2P, X_Kurtosis, Y_P2P, Y_RMS, Y_Z2P, Y_Kurtosis, Z_P2P, Z_RMS, Z_Z2P, Z_Kurtosis, FFT_X, FFT_Y, FFT_Z)
                	c. treon_vibration_test_fft_data (Sensor_id, Datetime, FFT_dictionary)
            	3. Create an MQQT server account on https://www.emqx.io/ 
            	4. Enter the account details on the Main function
    2. Set up the motor condition.
    3. Change the set number and brake current in the script.
	1. Run the command 'python Treon_export_Mac.py' or 'python Treon_export_Rest.py'
	3. The data will be collected in the foler 'SETXX_BCXXX' where xx represents Set number and brake current given and the script will start collecting the next dataset with automatically updated set number.

Enviroment - 
	paho-mqtt 1.6.1
	DateTime 5.5
	jsons 1.6.3
	pymysql 1.1.0
	threaded 4.2.0
	matplotlib 3.7.1
	python-csv 0.0.13
	numpy 1.25.2
	tensorflow 2.15.0
	os-sys 2.1.4
	jsons 1.6.3
