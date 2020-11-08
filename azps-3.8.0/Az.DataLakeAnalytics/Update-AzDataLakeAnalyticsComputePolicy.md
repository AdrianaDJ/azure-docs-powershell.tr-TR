---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096010"
---
# <span data-ttu-id="c9bb5-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c9bb5-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c9bb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bb5-103">Belirli bir AAD varlığı için Data Lake Analytics COMPUTE ilke kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="c9bb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9bb5-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="c9bb5-106">**Güncelleştirme-AzDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c9bb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9bb5-107">EXAMPLES</span></span>

### <span data-ttu-id="c9bb5-108">Örnek 1: işlem ilkesindeki bir kuralı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c9bb5-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="c9bb5-109">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan hiçbir işi gönderememesini sağlamak için "contosoadla" hesabında "myPolicy" adlı bir ilke güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="c9bb5-110">Örnek 2: her iki kuralla de bir COMPUTE ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9bb5-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="c9bb5-111">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan veya önceliği 100 dışında bir iş gönderememesini sağlamak için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="c9bb5-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="c9bb5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9bb5-112">PARAMETERS</span></span>

### <span data-ttu-id="c9bb5-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c9bb5-113">-Account</span></span>
<span data-ttu-id="c9bb5-114">Hesaplama ilkesini güncelleştirilecek hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="c9bb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bb5-115">-DefaultProfile</span></span>
<span data-ttu-id="c9bb5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c9bb5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9bb5-117">-Maxanalyzer Ticsunesperjob</span><span class="sxs-lookup"><span data-stu-id="c9bb5-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="c9bb5-118">Bu ilke için iş başına desteklenen en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="c9bb5-119">Bu, Minpriorityi veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="c9bb5-120">-Minpriorityi</span><span class="sxs-lookup"><span data-stu-id="c9bb5-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="c9bb5-121">Bu ilke için iş başına desteklenen en düşük öncelik.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="c9bb5-122">Bu, Maxanalyzer Ticsunesperjob veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="c9bb5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9bb5-123">-Name</span></span>
<span data-ttu-id="c9bb5-124">Güncelleştirilecek işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="c9bb5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bb5-125">-ResourceGroupName</span></span>
<span data-ttu-id="c9bb5-126">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="c9bb5-127">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="c9bb5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9bb5-128">-Confirm</span></span>
<span data-ttu-id="c9bb5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9bb5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bb5-130">-WhatIf</span></span>
<span data-ttu-id="c9bb5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9bb5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9bb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bb5-133">CommonParameters</span></span>
<span data-ttu-id="c9bb5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9bb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bb5-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9bb5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bb5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9bb5-136">INPUTS</span></span>

### <span data-ttu-id="c9bb5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c9bb5-137">System.String</span></span>

### <span data-ttu-id="c9bb5-138">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c9bb5-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c9bb5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9bb5-139">OUTPUTS</span></span>

### <span data-ttu-id="c9bb5-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c9bb5-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c9bb5-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9bb5-141">NOTES</span></span>

## <span data-ttu-id="c9bb5-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9bb5-142">RELATED LINKS</span></span>
