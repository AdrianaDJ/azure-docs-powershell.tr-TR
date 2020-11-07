---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 39c13bd7dd85f15edf1521ef372196b6c7472512
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916924"
---
# <span data-ttu-id="8ea53-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8ea53-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8ea53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea53-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea53-103">Belirli bir AAD varlığı için Data Lake Analytics COMPUTE ilke kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="8ea53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ea53-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ea53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ea53-105">DESCRIPTION</span></span>
<span data-ttu-id="8ea53-106">**Güncelleştirme-AzDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8ea53-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ea53-107">EXAMPLES</span></span>

### <span data-ttu-id="8ea53-108">Örnek 1: işlem ilkesindeki bir kuralı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8ea53-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="8ea53-109">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan hiçbir işi gönderememesini sağlamak için "contosoadla" hesabında "myPolicy" adlı bir ilke güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="8ea53-110">Örnek 2: her iki kuralla de bir COMPUTE ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8ea53-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="8ea53-111">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan veya önceliği 100 dışında bir iş gönderememesini sağlamak için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="8ea53-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="8ea53-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ea53-112">PARAMETERS</span></span>

### <span data-ttu-id="8ea53-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="8ea53-113">-Account</span></span>
<span data-ttu-id="8ea53-114">Hesaplama ilkesini güncelleştirilecek hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="8ea53-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="8ea53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea53-115">-DefaultProfile</span></span>
<span data-ttu-id="8ea53-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8ea53-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ea53-117">-Maxanalyzer Ticsunesperjob</span><span class="sxs-lookup"><span data-stu-id="8ea53-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="8ea53-118">Bu ilke için iş başına desteklenen en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="8ea53-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="8ea53-119">Bu, Minpriorityi veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="8ea53-120">-Minpriorityi</span><span class="sxs-lookup"><span data-stu-id="8ea53-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="8ea53-121">Bu ilke için iş başına desteklenen en düşük öncelik.</span><span class="sxs-lookup"><span data-stu-id="8ea53-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="8ea53-122">Bu, Maxanalyzer Ticsunesperjob veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="8ea53-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ea53-123">-Name</span></span>
<span data-ttu-id="8ea53-124">Güncelleştirilecek işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="8ea53-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="8ea53-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea53-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ea53-126">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8ea53-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8ea53-127">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="8ea53-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="8ea53-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ea53-128">-Confirm</span></span>
<span data-ttu-id="8ea53-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ea53-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ea53-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea53-130">-WhatIf</span></span>
<span data-ttu-id="8ea53-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ea53-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ea53-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ea53-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ea53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea53-133">CommonParameters</span></span>
<span data-ttu-id="8ea53-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ea53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea53-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea53-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea53-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ea53-136">INPUTS</span></span>

### <span data-ttu-id="8ea53-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea53-137">System.String</span></span>

### <span data-ttu-id="8ea53-138">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ea53-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ea53-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ea53-139">OUTPUTS</span></span>

### <span data-ttu-id="8ea53-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8ea53-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8ea53-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ea53-141">NOTES</span></span>

## <span data-ttu-id="8ea53-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ea53-142">RELATED LINKS</span></span>
