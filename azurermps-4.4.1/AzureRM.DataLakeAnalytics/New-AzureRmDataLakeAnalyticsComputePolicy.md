---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587958"
---
# <span data-ttu-id="08fbb-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="08fbb-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="08fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="08fbb-103">Belirli bir AAD varlığı için bir Data Lake Analytics COMPUTE ilke kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08fbb-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08fbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08fbb-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08fbb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="08fbb-106">**New-AzureRmDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08fbb-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="08fbb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="08fbb-108">Örnek 1: tek bir kuralla bir işlem ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="08fbb-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="08fbb-109">Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur ve 5 paralellik ile hiçbir işi gönderemezler.</span><span class="sxs-lookup"><span data-stu-id="08fbb-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="08fbb-110">Örnek 2: her iki kuralın de ayarlandığı bir işlem ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="08fbb-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="08fbb-111">Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3 100" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="08fbb-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="08fbb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08fbb-112">PARAMETERS</span></span>

### <span data-ttu-id="08fbb-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="08fbb-113">-Account</span></span>
<span data-ttu-id="08fbb-114">İşlem ilkesinin ekleneceği hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="08fbb-114">Name of the account to add the compute policy to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-115">-Maxdegreeofparallelizmperjob</span><span class="sxs-lookup"><span data-stu-id="08fbb-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="08fbb-116">Bu ilke için iş başına desteklenen en yüksek paralellik derecesi.</span><span class="sxs-lookup"><span data-stu-id="08fbb-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="08fbb-117">Bu, Minpriorityi veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="08fbb-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-118">-Minpriorityi</span><span class="sxs-lookup"><span data-stu-id="08fbb-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="08fbb-119">Bu ilke için iş başına desteklenen en düşük öncelik.</span><span class="sxs-lookup"><span data-stu-id="08fbb-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="08fbb-120">Bu, Maxdegreeofparallelizmperjob veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="08fbb-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="08fbb-121">-Name</span></span>
<span data-ttu-id="08fbb-122">Oluşturulacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="08fbb-122">Name of the compute policy to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-123">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="08fbb-123">-ObjectId</span></span>
<span data-ttu-id="08fbb-124">İlkenin uygulanacağı Kullanıcı veya grubun Azure Active Directory nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="08fbb-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-125">-NesneTürü</span><span class="sxs-lookup"><span data-stu-id="08fbb-125">-ObjectType</span></span>
<span data-ttu-id="08fbb-126">İçeri aktarılan nesne KIMLIĞI için Azure Active Directory nesne türü.</span><span class="sxs-lookup"><span data-stu-id="08fbb-126">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08fbb-127">-ResourceGroupName</span></span>
<span data-ttu-id="08fbb-128">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08fbb-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="08fbb-129">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="08fbb-129">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="08fbb-130">-Confirm</span></span>
<span data-ttu-id="08fbb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08fbb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08fbb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08fbb-132">-WhatIf</span></span>
<span data-ttu-id="08fbb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08fbb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08fbb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08fbb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08fbb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08fbb-135">-DefaultProfile</span></span>
<span data-ttu-id="08fbb-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08fbb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fbb-137">CommonParameters</span></span>
<span data-ttu-id="08fbb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08fbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fbb-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08fbb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fbb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08fbb-140">INPUTS</span></span>

### <span data-ttu-id="08fbb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="08fbb-141">System.String</span></span>
<span data-ttu-id="08fbb-142">System. Guid System. Int32</span><span class="sxs-lookup"><span data-stu-id="08fbb-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="08fbb-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08fbb-143">OUTPUTS</span></span>

### <span data-ttu-id="08fbb-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="08fbb-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="08fbb-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08fbb-145">NOTES</span></span>

## <span data-ttu-id="08fbb-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08fbb-146">RELATED LINKS</span></span>

