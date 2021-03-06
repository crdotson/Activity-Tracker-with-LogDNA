---

copyright:
  years: 2019
lastupdated: "2019-04-04"

keywords: IBM Cloud, LogDNA, Activity Tracker, iam, manage user access

subcollection: logdnaat

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}

 
# IAM으로 사용자 액세스 관리
{: #iam}

{{site.data.keyword.iamlong}}(IAM)를 사용하여 사용자를 안전하게 인증하고 {{site.data.keyword.cloud_notm}}에서 모든 클라우드 리소스에 대한 액세스를 일관되게 제어할 수 있습니다.
{:shortdesc}

**계정의 {{site.data.keyword.at_full_notm}} 서비스에 액세스하는 모든 사용자에게 IAM 사용자 역할이 정의된 액세스 정책을 지정해야 합니다.** 정책에 따라 선택한 서비스 또는 인스턴스의 컨텍스트 내에서 사용자가 수행할 수 있는 조치가 판별됩니다. 허용 가능한 조치는 사용자 정의되며 서비스에서 수행될 수 있는 오퍼레이션으로 정의됩니다. 그런 다음 조치가 IAM 사용자 역할에 맵핑됩니다.

*정책*을 사용하면 다양한 레벨에 액세스를 부여할 수 있습니다. 일부 옵션에는 다음이 포함됩니다. 

* 계정의 모든 IAM 사용 서비스에 대한 액세스
* 사용자 계정의 단일 지역에 있는 서비스의 모든 인스턴스에 대한 액세스
* 사용자 계정의 개별 서비스 인스턴스에 대한 액세스
* 리소스 그룹의 컨텍스트 내 서비스의 모든 인스턴스에 대한 액세스
* 리소스 그룹의 컨텍스트 내 단일 지역에 있는 서비스의 모든 인스턴스에 대한 액세스
* 리소스 그룹의 컨텍스트 내 모든 IAM 사용 서비스에 대한 액세스

*역할*은 사용자 또는 서비스 ID가 실행할 수 있는 조치를 정의합니다. {{site.data.keyword.cloud_notm}}에는 여러 유형의 역할이 있습니다.

* *플랫폼 관리 역할*을 사용하면 사용자가 플랫폼 레벨에서 서비스 리소스에 대한 태스크를 수행할 수 있습니다(예: 서비스에 대한 사용자 액세스 지정, 서비스 ID 작성 또는 삭제, 인스턴스 작성, 다른 사용자에게 서비스에 대한 정책 지정 및 인스턴스를 애플리케이션에 바인드).
* *서비스 액세스 역할*을 사용하면 사용자에게 서비스의 API를 호출하기 위한 다양한 레벨의 권한을 지정할 수 있습니다.

**사용자 및 서비스 ID 세트를 IAM 권한의 관리를 용이하게 하는 단일 엔티티로 구성하려면 *액세스 그룹*을 사용하십시오.** 개별 사용자 또는 서비스 ID마다 동일한 액세스를 여러 번 지정하는 대신 그룹에 단일 정책을 지정할 수 있습니다.
{: tip}

다음 튜토리얼을 통해 자세히 알아보십시오.
* [사용자 또는 서비스 ID에 관리 권한 부여](/docs/services/Activity-Tracker-with-LogDNA?topic=logdnaat-iam_manage_events#iam_manage_events)
* [사용자 또는 서비스 ID에 사용자 권한 부여](/docs/services/Activity-Tracker-with-LogDNA?topic=logdnaat-iam_view_events#iam_view_events)

## 액세스 그룹을 사용하여 액세스 관리
{: #groups}

액세스 그룹을 사용하여 사용자에 대한 액세스를 관리하거나 새 액세스를 지정하려면 계정의 모든 ID 및 액세스 사용 서비스에 대한 계정 소유자, 관리자 또는 편집자이거나 IAM 액세스 그룹 서비스에 대해 지정된 관리자 또는 편집자여야 합니다. 

{{site.data.keyword.cloud_notm}}에서 액세스 그룹을 관리하려면 다음 조치 중 하나를 선택하십시오.

* [액세스 그룹 작성](/docs/iam?topic=iam-groups#create_ag)
* [그룹에 액세스 지정](/docs/iam?topic=iam-groups#access_ag)


## 사용자에게 직접 정책을 지정하여 액세스 관리
{: #users}

IAM 정책을 사용하여 사용자에 대한 액세스를 관리하거나 새 액세스를 지정하려면 계정 소유자, 계정의 모든 서비스에 대한 관리자 또는 특정 서비스나 서비스 인스턴스의 관리자여야 합니다. 

{{site.data.keyword.cloud_notm}}에서 IAM 정책을 관리하려면 다음 조치 중 하나를 선택하십시오.

* 사용자의 권한을 수정하려면 [기존 액세스 권한 편집](/docs/iam?topic=iam-iammanidaccser#edit_existing)을 참조하십시오.
* 사용자에게 권한을 부여하려면 [새 액세스 지정](/docs/iam?topic=iam-iammanidaccser#assign_new_access)을 참조하십시오.
* 권한을 취소하려면 [액세스 제거](/docs/iam?topic=iam-iammanidaccser#removing_access)를 참조하십시오.
* 사용자 권한을 검토하려면 [지정된 액세스 검토](/docs/iam?topic=iam-iammanidaccser#review_your_access)를 참조하십시오.



## {{site.data.keyword.cloud_notm}} 플랫폼 역할
{: #platform}

다음 플랫폼 조치 중 하나를 실행할 수 있도록 {{site.data.keyword.cloud_notm}}의 사용자에게 부여할 수 있는 플랫폼 역할을 식별하려면 다음 표를 사용하십시오.

|플랫폼 조치                                                        |{{site.data.keyword.cloud_notm}} 플랫폼 역할    | 
|-------------------------------------------------------------------------|------------------------------------------------------|
|`다른 계정 구성원에게 서비스에 대해 작업할 수 있는 액세스 권한 부여`           |관리자                                        | 
|`서비스 인스턴스 프로비저닝`                                          |편집자                            | 
|`서비스 인스턴스 삭제`                                             |관리자 </br>편집자                            | 
|`서비스 ID 작성`                                                   |관리자 </br>편집자                            |
|`서비스 인스턴스의 세부사항 보기`                                    |관리자 </br>편집자 </br>운영자 </br>뷰어  | 
|`관찰 가능성 Activity Tracker 대시보드에서 서비스 인스턴스 보기`   |관리자 </br>편집자 </br>운영자 </br>뷰어  | 
{: caption="표 1. IAM 사용자 역할 및 조치" caption-side="top"}



## {{site.data.keyword.cloud_notm}} 서비스 역할
{: #service}

다음 서비스 조치 중 하나를 실행할 수 있도록 사용자에게 부여할 수 있는 서비스 역할을 식별하려면 다음 표를 사용하십시오.

|조치                                                                 |{{site.data.keyword.cloud_notm}} 서비스 역할     | 
|-------------------------------------------------------------------------|------------------------------------------------------|
|`이벤트 아카이브`                                                |관리자                                              |
|`경보 구성`                                                      |관리자 </br>독자                                    | 
|`데이터 필터링 및 검색`                                          |관리자 </br>독자                                    |
|`보기 작성`                                                      |관리자 </br>독자                                    |
|`이벤트 내보내기`                                                |관리자 </br>독자                                    |
|`LogDNA 웹 UI에서 사용자 환경 설정 구성`                         |관리자 </br>독자                                    |
|`LogDNA 웹 UI를 통해 이벤트 보기`                                |관리자 </br>독자                                    | 
{: caption="표 2. IAM 사용자 역할 및 조치" caption-side="top"}


**참고:** **관리자** 서비스 역할이 LogDNA 관리자 역할에 직접 맵핑됩니다.






