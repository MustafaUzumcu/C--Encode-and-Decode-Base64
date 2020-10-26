# C--Encode-and-Decode-Base64
C# - Encode and Decode Base64 Strings

# Extension
public static class ExtensionMethods
{
        public static string EncodeBase64(this string value)
        {
            var valueBytes = Encoding.UTF8.GetBytes(value);
            return Convert.ToBase64String(valueBytes);
        }

        public static string DecodeBase64(this string value)
        {
            var valueBytes = System.Convert.FromBase64String(value);
            return Encoding.UTF8.GetString(valueBytes);
        }
}
  
# Usage
 
# Encoding a Base64 String in C#
var base64EncodedString = "Sample Data".EncodeBase64();

# Decoding a Base64 String in C#
var normalString = base64EncodedString.DecodeBase64();
