#sndacs

## Usage

### Try

    try {
        String access_key_id = "xxxxx";
        String access_key_secret = "xxxxxxxxxxxxxxxxxxx";
        ProviderCredentials cred = new SNDACredentials(access_key_id, 
                                                       access_key_secret);
        CSService service = new RestCSService(cred);
        StorageBucket bucket = service.createBucket("bucket_name");
        CSObject csObject = new CSObject(new File("filepath/file"));
        service.putObject(bucket.getName(), object);
    } catch (CSServiceException e) {
        System.out.println(e.getErrorCode());
        System.out.println(e.getErrorMessage());
        System.out.println(e.getErrorRequestId());
        System.out.println(e.getErrorResource());
    } catch (Exception e) {
        e.printStackTrace();
    }
