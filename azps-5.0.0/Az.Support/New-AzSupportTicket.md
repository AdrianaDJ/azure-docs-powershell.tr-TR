---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278456"
---
# <span data-ttu-id="635af-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="635af-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="635af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635af-102">SYNOPSIS</span></span>
<span data-ttu-id="635af-103">Destek bileti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="635af-103">Creates a support ticket.</span></span>

## <span data-ttu-id="635af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="635af-104">SYNTAX</span></span>

### <span data-ttu-id="635af-105">Createsupportbilet Withcontactdetailparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="635af-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635af-106">Createsupportparameterwith, Tobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="635af-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635af-107">Createteknisyen Alsupportbilet with, Tobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="635af-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635af-108">Createquotasupportbilet with, Tobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="635af-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635af-109">Createteknisyen Alsupportbilet Withcontactdetailparameterset</span><span class="sxs-lookup"><span data-stu-id="635af-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635af-110">Createquotasupportbilet Withcontactdetailparameterset</span><span class="sxs-lookup"><span data-stu-id="635af-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635af-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="635af-111">DESCRIPTION</span></span>
<span data-ttu-id="635af-112">Bu cmdlet, faturalandırma, abonelik yönetimi, kota veya teknik sorunlar için destek bileti oluşturmak amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="635af-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="635af-113">Get-AzSupportService ve Get-AzSupportProblemClassification cmdlet 'lerini kullanarak Azure hizmetini tanımlar ve destek isteğinde bulunmasını istediğiniz sırayla buna karşılık gelen sorun sınıflandırmaları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="635af-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="635af-114">Aşağıdaki parametreleri belirtmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="635af-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="635af-115">CustomerContactDetail nesnesini oluşturmak için New-AzSupportContactProfileObject yardımcı cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="635af-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="635af-116">Bulut çözümü sağlayıcıları, müşterinin kiracısına oturum açıp *Csphometenantid* parametresini kullanarak kendi ev Kiracı kimliğini belirleyerek müşterinin abonelikleri için bir destek bileti oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="635af-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="635af-117">__Teknik biletler için:__</span><span class="sxs-lookup"><span data-stu-id="635af-117">__For technical tickets:__</span></span>

<span data-ttu-id="635af-118">Kaynak adını belirtmek için, teknisyen kaynak kimliğini, *teknisyen* kaynak kimliği parametresini kullanarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="635af-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="635af-119">Aşağıdaki örneğe bakın.</span><span class="sxs-lookup"><span data-stu-id="635af-119">See an example below.</span></span> 

<span data-ttu-id="635af-120">__Kota biletleri için:__</span><span class="sxs-lookup"><span data-stu-id="635af-120">__For quota tickets:__</span></span>

<span data-ttu-id="635af-121">**COMPUTE VM çekirdekleri** , **toplu Iş** , **SQL veritabanı** ve **SQL veri ambarına** kota artışı istemek için, *quotatıayrıntı* nesnesi altında ek ayrıntılar sağlayın.</span><span class="sxs-lookup"><span data-stu-id="635af-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="635af-122">Quotabilet ayrıntı nesnesi aşağıda açıklandığı gibi 3 özellikten oluşur.</span><span class="sxs-lookup"><span data-stu-id="635af-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="635af-123">Ayrıntılı belgeler için lütfen [buraya tıklayın.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="635af-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="635af-124">Çeşitli kota türleri için yük oluşturma hakkında ayrıntılı belgeler için lütfen [buraya tıklayın](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="635af-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="635af-125">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="635af-125">EXAMPLES</span></span>

### <span data-ttu-id="635af-126">Örnek 1: fatura veya abonelik yönetimi destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="635af-127">Destek istemek istediğiniz fatura veya abonelik yönetimi sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanma</span><span class="sxs-lookup"><span data-stu-id="635af-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-128">Örnek 2: Windows için sanal makine kaynağı için teknik destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="635af-129">Destek istemek istediğiniz Windows sorun sınıflandırması için sanal makinenin doğru GUID 'Lerini almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanma</span><span class="sxs-lookup"><span data-stu-id="635af-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-130">Örnek 3: belirli bir VM ailesi için sanal makine çekirdeğinin kotasını artıracak kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="635af-131">Kota işlemi VM çekirdeğinin sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-132">Örnek 4: bir toplu hesap için düşük öncelikli çekirdek kotasını artıracak kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="635af-133">Kota toplu Işlemi sorun sınıflandırmasını doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-134">Örnek 5: bir toplu hesap için belirli bir VM ailesi için VM çekirdek kotasını artıracak bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="635af-135">Kota toplu Işlemi sorun sınıflandırmasını doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-136">Örnek 6: bir toplu hesap için havuz kotasını yükseltmek amacıyla kota desteği bileti oluşturma.</span><span class="sxs-lookup"><span data-stu-id="635af-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="635af-137">Kota toplu Işlemi sorun sınıflandırmasını doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-138">Örnek 7: bir toplu hesap için etkin Işler ve iş zamanlamaları kotasını artıran bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="635af-139">Kota toplu Işlemi sorun sınıflandırmasını doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-140">Örnek 8: bir aboneliğin toplu Iş hesabı sayısını yükseltmek için bir kota destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="635af-141">Kota toplu Işlemi sorun sınıflandırmasını doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-142">Örnek 9: SQL veritabanında Vseçma kotasını yükseltmek için bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="635af-143">Kota SQL veritabanı sorun sınıflandırması 'nın doğru GUID 'Lerini almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-144">Örnek 10: SQL veritabanı için bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="635af-145">Kota SQL veritabanı sorun sınıflandırması 'nın doğru GUID 'Lerini almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-146">Örnek 11: SQL veri ambarına yönelik Vseçval kotasını yükseltmek için bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="635af-147">Kota SQL tarih ambarı sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-148">Örnek 12: SQL veri ambarı için sunucular kotasını yükseltmek amacıyla kota desteği bileti oluşturma.</span><span class="sxs-lookup"><span data-stu-id="635af-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="635af-149">Kota SQL veri ambarı sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-150">Örnek 13: makine öğrenme hizmeti için düşük öncelikli çekirdek kotasını yükseltmek amacıyla kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="635af-151">Kota makine Learning hizmeti sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-152">Örnek 14: makine öğrenme hizmeti için belirli bir VM ailesi için VM çekirdek kotasını artıracak kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="635af-153">Kota makine Learning hizmeti sorun sınıflandırması için doğru GUID 'Leri almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-154">Örnek 15: Azure SQL yönetilen örneğinin kotasını yükseltmek için bir kota desteği bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="635af-155">Kota SQL yönetilen örnek hizmeti sorun sınıflandırması 'nın doğru GUID 'Lerini almak için Get-AzSupportService ve Get-AzSupportProblemClassification kullanın.</span><span class="sxs-lookup"><span data-stu-id="635af-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-156">Örnek 16: Müştercontactdetail nesnesi yerine bireysel müşteri irtibat parametrelerini belirterek bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-157">Örnek 17: Azure 'dan 24 x 7 yanıtını içeren bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="635af-158">Örnek 18: bulut çözüm sağlayıcısı (CSP) kullanıyorsanız, müşterinizin adına bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="635af-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="635af-159">CSP ilk önce kiracılarında oturum açın ve aşağıdaki örnekte gösterildiği gibi müşterinin kiracısına oturum açın.</span><span class="sxs-lookup"><span data-stu-id="635af-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="635af-160">Böylece, destek bileti oluştururken kendi ev Kiracı kimliğini belirtmek için-CSPHomeTenantId parametresini kullanmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="635af-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="635af-161">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="635af-161">PARAMETERS</span></span>

### <span data-ttu-id="635af-162">-Adtionalemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="635af-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="635af-163">Ek e-posta adresleri.</span><span class="sxs-lookup"><span data-stu-id="635af-163">Additional email addresses.</span></span>
<span data-ttu-id="635af-164">Burada listelenen e-posta adresleri destek bileti hakkında herhangi bir yazışmadan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="635af-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-165">-Iş</span><span class="sxs-lookup"><span data-stu-id="635af-165">-AsJob</span></span>
<span data-ttu-id="635af-166">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="635af-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="635af-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="635af-168">Bu, bulut çözümü sağlayıcısı kullanıcısının, müşterilerine destek bileti oluşturmaya çalışan ev kiracı kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="635af-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-169">-Müştercontactdetail</span><span class="sxs-lookup"><span data-stu-id="635af-169">-CustomerContactDetail</span></span>
<span data-ttu-id="635af-170">SupportTicket kaynağıyla ilişkilendirilmiş müşteri iletişim bilgileri.</span><span class="sxs-lookup"><span data-stu-id="635af-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="635af-171">-CustomerCountry</span></span>
<span data-ttu-id="635af-172">Müşteri ülkesi.</span><span class="sxs-lookup"><span data-stu-id="635af-172">Customer country.</span></span>
<span data-ttu-id="635af-173">Bu, geçerli bir ISO Alpha-3 ülke kodu (ISO 3166) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="635af-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-174">-Müşteradı</span><span class="sxs-lookup"><span data-stu-id="635af-174">-CustomerFirstName</span></span>
<span data-ttu-id="635af-175">Müşteri adı.</span><span class="sxs-lookup"><span data-stu-id="635af-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-176">-Müşterlastname</span><span class="sxs-lookup"><span data-stu-id="635af-176">-CustomerLastName</span></span>
<span data-ttu-id="635af-177">Müşterinin soyadı.</span><span class="sxs-lookup"><span data-stu-id="635af-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-178">-Müştertelefonnumarası</span><span class="sxs-lookup"><span data-stu-id="635af-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="635af-179">Müşteri telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="635af-179">Customer phone number.</span></span>
<span data-ttu-id="635af-180">Tercih edilen kişi yöntemi telefon ise bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="635af-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-181">-Müşterpreferredsupportsupport</span><span class="sxs-lookup"><span data-stu-id="635af-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="635af-182">Özel.</span><span class="sxs-lookup"><span data-stu-id="635af-182">Peferred language of the custom.</span></span>
<span data-ttu-id="635af-183">Burada listelenen desteklenen dillerden birinin geçerli bir dil-Contry kodu olması gerekir https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="635af-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-184">-Müşterpreferredtimezone</span><span class="sxs-lookup"><span data-stu-id="635af-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="635af-185">Müşterinin tercih ettiği saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="635af-185">Customer preferred time zone.</span></span>
<span data-ttu-id="635af-186">Bu geçerli bir System.TimeZoneInfo.Id değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="635af-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-187">-Müştergunlubir Yemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="635af-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="635af-188">Müşteri birincil e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="635af-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635af-189">-DefaultProfile</span></span>
<span data-ttu-id="635af-190">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="635af-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-191">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="635af-191">-Description</span></span>
<span data-ttu-id="635af-192">Sorunun veya sorunun ayrıntılı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="635af-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-193">-Ad</span><span class="sxs-lookup"><span data-stu-id="635af-193">-Name</span></span>
<span data-ttu-id="635af-194">Bu cmdlet 'in oluşturduğu destek anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="635af-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="635af-195">-PreferredContactMethod</span></span>
<span data-ttu-id="635af-196">Tercih edilen kişi yöntemi.</span><span class="sxs-lookup"><span data-stu-id="635af-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="635af-197">-ProblemClassificationId</span></span>
<span data-ttu-id="635af-198">Her Azure hizmeti, karşılaştığınız sorun türüne karşılık gelen sorun sınıflandırması olarak bilinen bir sorun kategorisi kümesi içerir.</span><span class="sxs-lookup"><span data-stu-id="635af-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="635af-199">Bu parametre ProblemClassification kaynağının ARM kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="635af-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-200">-Problembaşlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="635af-200">-ProblemStartTime</span></span>
<span data-ttu-id="635af-201">Sorunun başladığı tarih ve saat.</span><span class="sxs-lookup"><span data-stu-id="635af-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-202">-Quotafdetail</span><span class="sxs-lookup"><span data-stu-id="635af-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="635af-203">Kota desteği anahtarının ek ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="635af-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="635af-204">-Require24X7Response</span></span>
<span data-ttu-id="635af-205">Bu destek biletinin Azure 'dan 7x24 bir yanıt gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="635af-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-206">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="635af-206">-Severity</span></span>
<span data-ttu-id="635af-207">Destek biletinin önem derecesi.</span><span class="sxs-lookup"><span data-stu-id="635af-207">Severity of the support ticket.</span></span>
<span data-ttu-id="635af-208">Bu, durumun ne olduğunu gösterir, bu da yanıt süresini, Azure 'daki teknik destek planının hizmet düzeyi sözleşmesine göre belirler.</span><span class="sxs-lookup"><span data-stu-id="635af-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-209">-Teknisyen</span><span class="sxs-lookup"><span data-stu-id="635af-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="635af-210">Bu, destek anahtarının oluşturulduğu Azure hizmet kaynağının kaynak kimliğidir (örneğin: bir sanal makine kaynağı veya HDInsight kaynağı).</span><span class="sxs-lookup"><span data-stu-id="635af-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-211">-Başlık</span><span class="sxs-lookup"><span data-stu-id="635af-211">-Title</span></span>
<span data-ttu-id="635af-212">Destek biletinin başlığı.</span><span class="sxs-lookup"><span data-stu-id="635af-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-213">-Onay</span><span class="sxs-lookup"><span data-stu-id="635af-213">-Confirm</span></span>
<span data-ttu-id="635af-214">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="635af-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635af-215">-WhatIf</span></span>
<span data-ttu-id="635af-216">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="635af-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="635af-217">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="635af-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635af-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635af-218">CommonParameters</span></span>
<span data-ttu-id="635af-219">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="635af-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635af-220">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="635af-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635af-221">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="635af-221">INPUTS</span></span>

### <span data-ttu-id="635af-222">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="635af-222">None</span></span>

## <span data-ttu-id="635af-223">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="635af-223">OUTPUTS</span></span>

### <span data-ttu-id="635af-224">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="635af-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="635af-225">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="635af-225">NOTES</span></span>

## <span data-ttu-id="635af-226">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="635af-226">RELATED LINKS</span></span>
