# CloudFormation Template for Website Hosting

## CloudFront and S3 Setup for UI Applications

For creating any website or app that needs to be hosted on AWS, use CloudFront with a private S3 bucket.

## CloudFormation Template

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: S3 and CloudFront CDN Template

Resources:
  WebsiteBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub '${AWS::StackName}-frontend-${AWS::AccountId}'
      PublicAccessBlockConfiguration:
        BlockPublicAcls: true
        BlockPublicPolicy: true
        IgnorePublicAcls: true
        RestrictPublicBuckets: true

  OriginAccessControl:
    Type: AWS::CloudFront::OriginAccessControl
    Properties:
      OriginAccessControlConfig:
        Name: !Sub '${AWS::StackName}-OAC'
        OriginAccessControlOriginType: s3
        SigningBehavior: always
        SigningProtocol: sigv4

  CloudFrontDistribution:
    Type: AWS::CloudFront::Distribution
    Properties:
      DistributionConfig:
        Origins:
          - Id: S3Origin
            DomainName: !GetAtt WebsiteBucket.RegionalDomainName
            S3OriginConfig:
              OriginAccessIdentity: ''
            OriginAccessControlId: !Ref OriginAccessControl
        Enabled: true
        DefaultRootObject: index.html
        DefaultCacheBehavior:
          TargetOriginId: S3Origin
          ViewerProtocolPolicy: redirect-to-https
          AllowedMethods: [GET, HEAD, OPTIONS]
          CachedMethods: [GET, HEAD]
          Compress: true
          CachePolicyId: 4135ea2d-6df8-44a3-9df3-4b5a84be39ad
        CustomErrorResponses:
          - ErrorCode: 403
            ResponseCode: 200
            ResponsePagePath: /index.html
          - ErrorCode: 404
            ResponseCode: 200
            ResponsePagePath: /index.html
        PriceClass: PriceClass_100

  WebsiteBucketPolicy:
    Type: AWS::S3::BucketPolicy
    Properties:
      Bucket: !Ref WebsiteBucket
      PolicyDocument:
        Statement:
          - Effect: Allow
            Principal:
              Service: cloudfront.amazonaws.com
            Action: s3:GetObject
            Resource: !Sub '${WebsiteBucket}/*'
            Condition:
              StringEquals:
                'AWS:SourceArn': !Sub 'arn:aws:cloudfront::${AWS::AccountId}:distribution/${CloudFrontDistribution}'

Outputs:
  WebsiteURL:
    Description: CloudFront Distribution URL
    Value: !Sub 'https://${CloudFrontDistribution.DomainName}'
  
  WebsiteBucket:
    Description: S3 Website Bucket
    Value: !Ref WebsiteBucket
```

## Template Features

This simplified template includes:
- S3 bucket with secure configuration
- CloudFront distribution with Origin Access Control
- Bucket policy for CloudFront access
- Essential outputs for the CDN URL and bucket name

## Security Features

- Private S3 bucket with public access blocked
- CloudFront Origin Access Control (OAC) for secure access
- HTTPS-only viewer protocol
- Proper IAM policies for least privilege access
