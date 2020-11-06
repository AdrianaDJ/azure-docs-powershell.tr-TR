---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 860b58ce3be37eb2ef2277b627971adb301a02af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591997"
---
# <span data-ttu-id="4bd93-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4bd93-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4bd93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd93-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd93-103">Belirli bir AAD varlığı için Data Lake Analytics COMPUTE ilke kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bd93-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bd93-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd93-106">**Güncelleştirme-AzureRmDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4bd93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bd93-107">EXAMPLES</span></span>

### <span data-ttu-id="4bd93-108">Örnek 1: işlem ilkesindeki bir kuralı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4bd93-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="4bd93-109">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan hiçbir işi gönderememesini sağlamak için "contosoadla" hesabında "myPolicy" adlı bir ilke güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="4bd93-110">Örnek 2: her iki kuralla de bir COMPUTE ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bd93-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="4bd93-111">Bu komut, kullanıcının 5 ' ten fazla analitik birimi olan veya önceliği 100 dışında bir iş gönderememesini sağlamak için "contosoadla" hesabında "" adlı bir ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="4bd93-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="4bd93-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bd93-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd93-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4bd93-113">-Account</span></span>
<span data-ttu-id="4bd93-114">Hesaplama ilkesini güncelleştirilecek hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="4bd93-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="4bd93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd93-115">-DefaultProfile</span></span>
<span data-ttu-id="4bd93-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4bd93-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bd93-117">-Maxanalyzer Ticsunesperjob</span><span class="sxs-lookup"><span data-stu-id="4bd93-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="4bd93-118">Bu ilke için iş başına desteklenen en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="4bd93-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="4bd93-119">Bu, Minpriorityi veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4bd93-120">-Minpriorityi</span><span class="sxs-lookup"><span data-stu-id="4bd93-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="4bd93-121">Bu ilke için iş başına desteklenen en düşük öncelik.</span><span class="sxs-lookup"><span data-stu-id="4bd93-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="4bd93-122">Bu, Maxanalyzer Ticsunesperjob veya her iki parametre de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4bd93-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bd93-123">-Name</span></span>
<span data-ttu-id="4bd93-124">Güncelleştirilecek işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4bd93-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="4bd93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd93-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bd93-126">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4bd93-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4bd93-127">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="4bd93-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4bd93-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bd93-128">-Confirm</span></span>
<span data-ttu-id="4bd93-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bd93-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd93-130">-WhatIf</span></span>
<span data-ttu-id="4bd93-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bd93-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bd93-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bd93-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bd93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd93-133">CommonParameters</span></span>
<span data-ttu-id="4bd93-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bd93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd93-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd93-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd93-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bd93-136">INPUTS</span></span>

### <span data-ttu-id="4bd93-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd93-137">System.String</span></span>

### <span data-ttu-id="4bd93-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4bd93-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4bd93-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bd93-139">OUTPUTS</span></span>

### <span data-ttu-id="4bd93-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4bd93-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4bd93-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bd93-141">NOTES</span></span>

## <span data-ttu-id="4bd93-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bd93-142">RELATED LINKS</span></span>
