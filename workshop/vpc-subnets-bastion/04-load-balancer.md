# Load Balancer

At this point, we need to create a Load Balancer to be able to route request from the web to our instances.

## Create a new Load Balancer
1. Go to EC2 under Computer section.
2. Click on Load Balancers.
3. Click Create Load Balancer.
4. Click Create on Application Load Balancer.
5. As Name put: `aws-workshop-load-balancer-vpc`.
6. On Availability Zones, on VPC select `awsworkshopvpc`.
7. Click on `us-east-1a`.
8. Click on `10.0.1.0-us-east-1a`.
9. Repeat steps 7 and 8 for `us-east-1b` and `10.0.3.0-us-east-1b`.
10. Click Next: Configure Security Settings.
11. Click Next: Configure Security Groups.
12. Select Create a **new** security group and then click Next: Configure Routing.
13. As name put: `aws-workshop-target-group-vpc`.
14. As Port: `9000`.
15. As path: `/api/tags`.
16. Click Next: Register Targets.
17. Click Next: Review.
18. Click: Create.
19. Click: Close.
20. Select the new load balancer.
21. Go to Description on bottom and find Security.
22. Click Edit Security Groups.
23. Select default (so that both security groups are selected).
24. Click Save.
25. Delete old Load Balancer.

## Modify API_URL
Repeat the steps outlined in [this section](/workshop/elb-auto-scaling-group/03-finishing-up.md).

---
**Next:** [move RDS into your VPC](/workshop/vpc-subnets-bastion/05-RDS.md).

# Load Balancer

이 시점에서 웹에서 인스턴스로 요청을 라우팅 할 수 있도록 로드밸런서를 만들어야합니다.

## Create a new Load Balancer
1. AWS Management Console 에서 Computre 의 EC2 Dashboard 로 이동하세요.
2. **Load Balancers** 를 Click 하세요.
3. Load Balancer Create 를 Click 하세요.
4. Application Load Balancer 생성을 Click 하세요.
5. Name 입력: `aws-workshop-load-balancer-vpc` 을 입력하거나 원하는 것을 입력하세요.
6. Availability Zones, VPC 를 선택하고 `awsworkshopvpc` 입력하거나 원하시는 것을 입력하세요.
7. `ap-northeast-1a` Click 하세요.
8. `10.0.1.0-ap-northeast-1a` Click 하세요.
9. 반복, 7번에서 8번까지 반복하여 `ap-northeast-1b` 와 `10.0.3.0-ap-northeast-1b` 를 입력하거나 원하시는 것을 입력하세요.
10. Next: Configure Security 를 Click 하여 Settings 하세요.
11. Next: Configure Security Groups 를 Click 하세요.
12. 생성한 **new** security group 을 선택하고 그 다음 Next: Configure Routing click 하세요.
13. name 입력: `aws-workshop-target-group-vpc` 을 입력하거나 원하시는 것을 입력하세요.
14. Port: `9000`.
15. path: `/api/tags`.
16. Next: Register Targets Click 하세요.
17. Next: Review 를 Click 하세요.
18. Click: Create.
19. Click: Close.
20. New load balancer 를 선택하세요.
21. 아래 Description 으로 이동하여 Security 를 찾으세요.
22. Security Groups 에서 Edit 를 Click 하세요.
23. default (so that both security groups are selected) 를 선택하세요.
24. Save 를 Click 하세요.
25. Old Load Balancer 를 삭제하세요.

## Modify API_URL
반복, 이 단계를 반복하세요 [this section](/workshop/elb-auto-scaling-group/03-finishing-up.md).

---
**다음:** [move RDS into your VPC](/workshop/vpc-subnets-bastion/05-RDS.md).