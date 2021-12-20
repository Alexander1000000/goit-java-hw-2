class NameEncoderDecoder {
    public String encode(String name) {
    String encode = 
              "NOTFORYOU" + name
                    .replace ("e","1")
                    .replace ("u","2")
                    .replace ("i","3")
                    .replace ("o","4")
                    .replace ("a","5")
                    + "YESNOTFORYOU";
      return encode;
    }
  
    public String decode(String name) {
    String decodeCutNOT = name.replace ("NOTFORYOU","");
      String decodeCutYES = decodeCutNOT.replace ("YES","");
        String decode = decodeCutYES
                    .replace ("1","e")
                    .replace ("2","u")
                    .replace ("3","i")
                    .replace ("4","o")
                    .replace ("5","a");
      return decode;
    }
}
