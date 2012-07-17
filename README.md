#sndacs

## Usage

### Try

    try {
        String access_key_id = "xxxxx";
        String access_key_secret = "xxxxxxxxxxxxxxxxxxx";
        ProviderCredentials cred = new SNDACredentials(access_key_id, 
                                                       access_key_secret);
        CSService service = new RestCSService(cred);
        CSBucket csBucket = service.createBucket("bucket_name");
        CSObject csObject = new CSObject(new File("filepath/file"));
        service.putObject(csBucket.getName(), csObject);
    } catch (CSServiceException e) {
        System.out.println(e.getErrorCode());
        System.out.println(e.getErrorMessage());
        System.out.println(e.getErrorRequestId());
        System.out.println(e.getErrorResource());
    } catch (Exception e) {
        e.printStackTrace();
    }

### commons-lang

    <dependency>
        <groupId>commons-lang</groupId>
        <artifactId>commons-lang</artifactId>
        <version>2.5</version>
    </dependency>
    
### commons-codec

    <dependency>
        <groupId>commons-codec</groupId>
        <artifactId>commons-codec</artifactId>
        <version>1.5</version>
    </dependency>

### commons-pool

    <dependency>
        <groupId>commons-pool</groupId>
        <artifactId>commons-pool</artifactId>
        <version>1.5.6</version>
    </dependency>
    
### guava

    <dependency>
        <groupId>com.google.guava</groupId>
        <artifactId>guava</artifactId>
        <version>11.0.1</version>
    </dependency>
    
### log4j

    <dependency>
    	<groupId>log4j</groupId>
        <artifactId>log4j</artifactId>
        <version>1.2.16</version>
    </dependency>
    
### slf4j-log4j12

    <dependency>
    	<groupId>org.slf4j</groupId>
        <artifactId>slf4j-log4j12</artifactId>
        <version>1.6.4</version>
    </dependency>
    
### slf4j-api

    <dependency>
    	<groupId>org.slf4j</groupId>
        <artifactId>slf4j-api</artifactId>
        <version>1.6.4</version>
    </dependency>

### log4j-over-slf4j

    <dependency>
    	<groupId>org.slf4j</groupId>
        <artifactId>log4j-over-slf4j</artifactId>
        <version>1.6.4</version>
    </dependency>
    
### bcprov-jdk16

    <dependency>
        <groupId>org.bouncycastle</groupId>
        <artifactId>bcprov-jdk16</artifactId>
        <version>1.46</version>
    </dependency>
    
### java-xmlbuilder

    <dependency>
        <groupId>com.jamesmurty.utils</groupId>
    	<artifactId>java-xmlbuilder</artifactId>
        <version>0.4</version>
    </dependency>
    
### joda-time

    <dependency>
        <groupId>joda-time</groupId>
        <artifactId>joda-time</artifactId>
        <version>2.0</version>
    </dependency>

### httpclient

    <dependency>
        <groupId>org.apache.httpcomponents</groupId>
        <artifactId>httpclient</artifactId>
        <version>4.1.3</version>
    </dependency>

### junit

    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.8.2</version>
        <scope>test</scope>
    </dependency>
    
### mockito-all
    
    <dependency>
        <groupId>org.mockito</groupId>
        <artifactId>mockito-all</artifactId>
        <version>1.8.5</version>
        <scope>test</scope>
    </dependency>

