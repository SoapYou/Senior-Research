# Senior-Research
# For CSC450, The code to test encryption time


import java.io.BufferedReader;
import java.io.FileReader;
import java.security.MessageDigest;
import java.sql.Date;
import java.text.SimpleDateFormat;

import com.berry.BCrypt;


public class EncryptionTime
{
	
	long startTime = System.currentTimeMillis();
	public static String line;
	
	
    public static void main(String[] args)throws Exception
    {
        
    	System.out.println("MD5:");        
    	long startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-100.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 100 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-500.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 500 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-1000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 1000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-10000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 10000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-100000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 100000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
 
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-1000000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
              MessageDigest md = MessageDigest.getInstance("MD5");
              md.update(line.getBytes());

              byte byteData[] = md.digest();

              StringBuffer sb = new StringBuffer();
              for (int i = 0; i < byteData.length; i++) {
               sb.append(Integer.toString((byteData[i] & 0xff) + 0x100, 16).substring(1));
              }
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 1000000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }  
    	
    	
    	System.out.println("Bcrypt:");  
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-100.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 100 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-500.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 500 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-1000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 1000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-10000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 10000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-100000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 100000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
    	
    	startTime = System.currentTimeMillis();
    	try{
          
            FileReader inputFile = new FileReader("/Users/ye/Documents/workspace/EncryptTime/src/password-1000000.txt");

            BufferedReader bufferReader = new BufferedReader(inputFile);

            while ((line = bufferReader.readLine()) != null)   {
            	String password = BCrypt.hashpw(line, BCrypt.gensalt(12));
          	
            }
            long endTime = System.currentTimeMillis();
            
            System.out.println("Encryption 1000000 Password: " + (endTime -startTime) + "ms");
            bufferReader.close();
         }catch(Exception e){
            System.out.println("Error while reading file line by line:" + e.getMessage());                      
         }
        
    }
}
