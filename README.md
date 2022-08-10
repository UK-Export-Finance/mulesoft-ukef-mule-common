# Introduction 

Compiling and deploying to Github (Not to the Runtime).

You might need to increase version number to make deployment work (or delete old package in Github)

mvn clean -DdecryptionKey=DECRYPTION_KEY  
mvn validate -DdecryptionKey=DECRYPTION_KEY  
mvn clean test -DdecryptionKey=DECRYPTION_KEY  
mvn clean install -DskipMunitTests -DdecryptionKey=DECRYPTION_KEY  
**You might need to disconnect from GlobalProtectVPN to push to github**  
mvn deploy -DskipMunitTests -DdecryptionKey=DECRYPTION_KEY
