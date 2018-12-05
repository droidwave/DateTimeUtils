# DateTimeUtils
DateTime Formating and Parsing in Android. SimpleDateFormat is a extends DateFormat class used for formatting and parsing dates in Android locale-sensitive manner. It allows for formatting date to text and parsing text to date and normalization.

We built a plug and Solution for Date formatting and parsing in Android. for more details read here 
https://androidwave.com/format-datetime-in-android/ 

How to use these utilities.? 

/**
   * Date Format example 4
   */
  public static final String DATE_FORMAT = "yyyy-MM-dd HH:mm:ss";
  String mDateTimeString = "2018-12-05 10:37:43";
  try {
      long mTimestamp = DateUtils.getTimeStampFromDateTime(mDateTimeString, DATE_FORMAT);
  } catch (ParseException e) {
      e.printStackTrace();
  }
 
  /**
   * Get current datetime example 5
   */
  public static final String DATE_FORMAT = "yyyy-MM-dd HH:mm:ss";
  String mDateTime = DateUtils.formatDateTimeFromDate(DATE_FORMAT, Calendar.getInstance().getTime());
 
 
  
/**  Example 6
 * DateTime Input Format
 */
 public static final String DATE_INPUT_FORMAT = "yyyy-MM-dd HH:mm:ss";
 
/**
 * DateTime Output Format
 */
public static final String DATE_OUTPUT_FORMAT = "dd-MMM-yyyy";
 
 String mDateTimeString = "2018-12-05 10:37:43";
 
  String mDateTime = null;
  try {
      mDateTime = DateUtils.formatDateFromDateString(DATE_INPUT_FORMAT, DATE_OUTPUT_FORMAT, mDateTimeString);
  } catch (ParseException e) {
      e.printStackTrace();
  }
 
The output is - 05-Dec-2018;
