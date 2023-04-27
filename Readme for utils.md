# README for eICU Data Preprocessing Functions
This README provides an overview of the functions used to preprocess the eICU dataset for further analysis.

# Functions
## dataframe_from_csv(path, header=0, index_col=False)
Reads a CSV file and returns a pandas DataFrame.

## filter_patients_on_columns_model(patients)
Filters the patients DataFrame by selecting specific columns.

## cohort_stay_id(patients)
Extracts a list of unique patientunitstayid values from the patients DataFrame.

## transform_gender(gender_series)
Transforms the gender values in the given pandas Series to numerical values.

## transform_ethnicity(ethnicity_series)
Transforms the ethnicity values in the given pandas Series to numerical values.

## transform_hospital_discharge_status(status_series)
Transforms the hospital discharge status values in the given pandas Series to numerical values.

## transform_unit_discharge_status(status_series)
Transforms the unit discharge status values in the given pandas Series to numerical values.

## transform_dx_into_id(df)
Transforms the apacheadmissiondx column in the given DataFrame to unique numerical identifiers.

## read_patients_table(eicu_path, output_path)
Reads the patient.csv file from eICU dataset and preprocesses the patient data, then saves it to a CSV file.

## cohort_stay_id(patients)
Returns a list of unique patientunitstayid values from the patients DataFrame.

## filter_patients_on_age(patient, min_age=18, max_age=89)
Filters the patients DataFrame based on the age range specified.

## ilter_one_unit_stay(patients)
Filters the patients DataFrame to include only patients with one unit stay.

## filter_patients_on_columns(patients)
Filters the patients DataFrame by selecting specific columns.

## break_up_stays_by_unit_stay(pats, output_path, stayid=None, verbose=1)
Splits the patients DataFrame into individual files based on patientunitstayid.

## dataframe_from_csv(path, index_col=None)
Reads a CSV file and returns a pandas DataFrame.

## filter_lab_on_columns(lab)
Filters the lab DataFrame by selecting specific columns.

## rename_lab_columns(lab)
Renames columns in the lab DataFrame to have unified column names.

## item_name_selected_from_lab(lab, items)
Filters the lab DataFrame to include only the specified items.

## check_itemvalue(df)
Checks and converts itemvalue column in the given DataFrame to float.

## read_lab_table(eicu_path)
Reads the lab.csv file from eICU dataset and preprocesses the lab data.

## break_up_lab_by_unit_stay(lab, output_path, stayid=None, verbose=1)
Splits the lab DataFrame into individual files based on patientunitstayid.

## filter_nc_on_columns(nc)
Filters the nurseCharting DataFrame by selecting specific columns.

## rename_nc_columns(nc)
Renames columns in the nurseCharting DataFrame to have unified column names.

## item_name_selected_from_nc(nc, label, name)
Filters the nurseCharting DataFrame based on specified label and name values.

## conv_far_cel(nc)
Converts temperature values in the nurseCharting DataFrame from Fahrenheit to Celsius.

## replace_itemname_value(nc)
Replaces itemname values in the nurseCharting DataFrame for better consistency.

## read_nc_table(eicu_path)
Reads the nurseCharting.csv file from eICU dataset and preprocesses the nurseCharting data.

## extract_time_series_from_subject(t_path)
Extracts time series data for each patient from the preprocessed CSV files.

## check_in_range(df)
Clips the range of values for certain columns in the DataFrame.

## convert_events_to_timeseries(events, variable_column='itemname', variables=[])
Converts event data into time series format.