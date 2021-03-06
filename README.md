# AWS Workshop

이 워크숍에서는 여러분에게 [Amazon Web Services](https://aws.amazon.com/) (AWS) 을 이용하여 인프라를 관리하는 방법을 소개하고자 합니다.

우리는 실제 애플리케이션을 배포하는 방법을 배웁니다.
데모 애플리케이션으로는 Conduit라 불리는 [오픈소스 테스트 애플리케이션](https://github.com/gothinkster/realworld)을 사용합니다.
이는 같은 애플리케이션이 여러 가지 백엔드와 프런트엔드 프레임워크에 구현되어 있어,
새로운 프레임워크를 배울 때 편리하기 때문입니다.
특히, 우리는 [React](https://reactjs.org/)와 [Django](https://www.djangoproject.com/) + [Django-Rest-Framework](http://www.django-rest-framework.org/) 백엔드로 작성된 버전을 사용할 예정입니다.

이 레포지토리에서, 
여러분은 앞으로 사용할 인프라에 맞게 설정이 수정된,
백엔드와 프론트엔드 컴포넌트를 찾을 수 있습니다.

# 전제조건

여러분은 AWS account가 꼭 필요합니다.
여러분 대부분이 free tier를 사용하겠지만, Elastic Load Balancers(ELB), Encryption Keys 및 기타 등등,
일부 서비스에서 비용이 발생할 수 있습니다.
따라서 여러분은 이 워크숍을 끝내기 위해 몇 달러(US 5달러 미만)를 쓸 준비가 되어 있어야 합니다.

원하신다면,
만일의 경우를 대비하여
[AWS 예산을 사용한 AWS 프리 티어 사용 알림](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-alarms.html)을 이용하여 이러한 상황을 회피할 수 있습니다.


# 목차

이 워크숍의 섹션은 다음과 같습니다:

1. [Set up users](/workshop/set-up-users.md).
2. [S3, RDS and EC2](/workshop/s3-web-ec2-api-rds/introduction.md). 
    여기에서 여러분은 S3에 웹사이트를 배포하고, 백엔드는 RDS에 데이터를 저장하며, API는 EC2에 배포됩니다.
3. [Load Balancer and Auto Scaling Group](/workshop/elb-auto-scaling-group/introduction.md).
4. [VPC configuration and Bastion instance](/workshop/vpc-subnets-bastion/introduction.md).
    여기에서 여러분은 
    공개 및 개인 서브넷를 가진 VPC 설정하고,
    이에 맞게 Auto Scaling Group(ASG) 및 Load Balancer(ELB)를 수정하며,
    SSH를 통하여 API 인스턴스에 접근하기 위한 **접속 호스트**(Bastion Host)를 추가합니다.
5. [Beanstalk](/workshop/beanstalk/introduction.md). 
    여기에서 여러분은
    모든 상세한 설정을 수작업으로 작성하지 않고,
    백엔드(EC2 + ASG + ELB)를 설정하고 관리하기 위한 Beanstalk 사용법을 배웁니다.

---

**Next:** AWS account를 가지고 계시면, 바로 [시작합시다](/workshop/set-up-users.md).
