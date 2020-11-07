---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751235"
---
# <span data-ttu-id="abcf1-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="abcf1-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="abcf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="abcf1-103">Azure Danışmanı yapılandırmasını güncelleştirir veya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abcf1-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="abcf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abcf1-104">SYNTAX</span></span>

### <span data-ttu-id="abcf1-105">Inputobjectrgexcludeparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abcf1-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abcf1-106">Inputobjectlowcpuexcludeparameterset</span><span class="sxs-lookup"><span data-stu-id="abcf1-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abcf1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="abcf1-107">DESCRIPTION</span></span>
<span data-ttu-id="abcf1-108">Azure Danışmanı 'nın yapılandırmasını güncelleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="abcf1-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="abcf1-109">İki tür yapılandırma vardır: abonelik düzeyi yapılandırması ve ResourceGroup düzeyi yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="abcf1-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="abcf1-110">Abonelik düzeyi yapılandırması: bir aboneliğe bu tür için yalnızca bir yapılandırma olabilir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="abcf1-111">LowCpuThreshold ve dışlama özellikleri bu cmdlet kullanılarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="abcf1-112">ResourceGroup düzey yapılandırması: her bir ResourceGroup için yalnızca bir yapılandırma olabilir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="abcf1-113">Yalnızca Exclude özelliği bu cmdlet kullanılarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="abcf1-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abcf1-114">EXAMPLES</span></span>

###  <span data-ttu-id="abcf1-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="abcf1-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="abcf1-116">Abonelik düzeyi yapılandırması için yapılandırmayı (lowCpuThreshold) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="abcf1-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="abcf1-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="abcf1-118">Abonelik düzeyi yapılandırması için yapılandırmayı (lowCpuThreshold, exclude) güncelleştirir ve öneri oluşumunu dışlar.</span><span class="sxs-lookup"><span data-stu-id="abcf1-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="abcf1-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="abcf1-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="abcf1-120">ResourceGroupName1 için, öneri oluşturmada dışarıda tutulacak yapılandırmayı (hariç tutma) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="abcf1-121">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="abcf1-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="abcf1-122">Ardışık düzene geçirilen belirli öneri için yapılandırmayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="abcf1-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abcf1-123">PARAMETERS</span></span>

### <span data-ttu-id="abcf1-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="abcf1-124">-Confirm</span></span>
<span data-ttu-id="abcf1-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abcf1-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcf1-126">-DefaultProfile</span></span>
<span data-ttu-id="abcf1-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abcf1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="abcf1-128">-Exclude</span></span>
<span data-ttu-id="abcf1-129">Öneri kuşak dışında tutma.</span><span class="sxs-lookup"><span data-stu-id="abcf1-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="abcf1-130">Belirtilmezse, Exclude özelliği false olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="abcf1-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abcf1-131">-InputObject</span></span>
<span data-ttu-id="abcf1-132">Get-AzAdvisorConfiguration çağrısı tarafından döndürülen PsAzureAdvisorConfigurationData türü.</span><span class="sxs-lookup"><span data-stu-id="abcf1-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-133">-Lowcpueşiği</span><span class="sxs-lookup"><span data-stu-id="abcf1-133">-LowCpuThreshold</span></span>
<span data-ttu-id="abcf1-134">Düşük CPU eşiği değeri.</span><span class="sxs-lookup"><span data-stu-id="abcf1-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abcf1-135">-ResourceGroupName</span></span>
<span data-ttu-id="abcf1-136">Yapılandırma için kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="abcf1-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abcf1-137">-WhatIf</span></span>
<span data-ttu-id="abcf1-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abcf1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abcf1-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abcf1-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcf1-140">CommonParameters</span></span>
<span data-ttu-id="abcf1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abcf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="abcf1-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcf1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcf1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abcf1-143">INPUTS</span></span>

### <span data-ttu-id="abcf1-144">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="abcf1-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="abcf1-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abcf1-145">OUTPUTS</span></span>

### <span data-ttu-id="abcf1-146">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="abcf1-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="abcf1-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abcf1-147">NOTES</span></span>

## <span data-ttu-id="abcf1-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abcf1-148">RELATED LINKS</span></span>
