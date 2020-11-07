---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 3fbf0d09b2307d96512c04e13521544a69fcde8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761092"
---
# <span data-ttu-id="5082c-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5082c-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5082c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5082c-102">SYNOPSIS</span></span>
<span data-ttu-id="5082c-103">Belirli bir AAD varlığı için bir Data Lake Analytics COMPUTE ilke kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5082c-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="5082c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5082c-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5082c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5082c-105">DESCRIPTION</span></span>
<span data-ttu-id="5082c-106">**New-AzDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5082c-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5082c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5082c-107">EXAMPLES</span></span>

### <span data-ttu-id="5082c-108">Örnek 1: tek bir kuralla bir işlem ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5082c-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="5082c-109">Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="5082c-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="5082c-110">Örnek 2: her iki kuralın de ayarlandığı bir işlem ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5082c-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="5082c-111">Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3 100" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="5082c-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="5082c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5082c-112">PARAMETERS</span></span>

### <span data-ttu-id="5082c-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5082c-113">-Account</span></span>
<span data-ttu-id="5082c-114">İşlem ilkesinin ekleneceği hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="5082c-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="5082c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5082c-115">-DefaultProfile</span></span>
<span data-ttu-id="5082c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5082c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5082c-117">-Maxanalyzer Ticsunesperjob</span><span class="sxs-lookup"><span data-stu-id="5082c-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="5082c-118">Bu ilke için iş başına desteklenen en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="5082c-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="5082c-119">Bu, Minpriorityi veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5082c-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5082c-120">-Minpriorityi</span><span class="sxs-lookup"><span data-stu-id="5082c-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="5082c-121">Bu ilke için iş başına desteklenen en düşük öncelik.</span><span class="sxs-lookup"><span data-stu-id="5082c-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="5082c-122">Bu, Maxanalyzer Ticsunesperjob veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5082c-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="5082c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="5082c-123">-Name</span></span>
<span data-ttu-id="5082c-124">Oluşturulacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5082c-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="5082c-125">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5082c-125">-ObjectId</span></span>
<span data-ttu-id="5082c-126">İlkenin uygulanacağı Kullanıcı veya grubun Azure Active Directory nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="5082c-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="5082c-127">-NesneTürü</span><span class="sxs-lookup"><span data-stu-id="5082c-127">-ObjectType</span></span>
<span data-ttu-id="5082c-128">İçeri aktarılan nesne KIMLIĞI için Azure Active Directory nesne türü.</span><span class="sxs-lookup"><span data-stu-id="5082c-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="5082c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5082c-129">-ResourceGroupName</span></span>
<span data-ttu-id="5082c-130">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5082c-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="5082c-131">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="5082c-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="5082c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5082c-132">-Confirm</span></span>
<span data-ttu-id="5082c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5082c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5082c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5082c-134">-WhatIf</span></span>
<span data-ttu-id="5082c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5082c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5082c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5082c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5082c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5082c-137">CommonParameters</span></span>
<span data-ttu-id="5082c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5082c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5082c-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5082c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5082c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5082c-140">INPUTS</span></span>

### <span data-ttu-id="5082c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5082c-141">System.String</span></span>

### <span data-ttu-id="5082c-142">System. Guid</span><span class="sxs-lookup"><span data-stu-id="5082c-142">System.Guid</span></span>

### <span data-ttu-id="5082c-143">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5082c-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5082c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5082c-144">OUTPUTS</span></span>

### <span data-ttu-id="5082c-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5082c-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5082c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5082c-146">NOTES</span></span>

## <span data-ttu-id="5082c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5082c-147">RELATED LINKS</span></span>