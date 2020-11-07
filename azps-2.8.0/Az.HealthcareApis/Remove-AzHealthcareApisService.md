---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 6905e16667fd2a4378474950d928ef730ed1786e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751786"
---
# <span data-ttu-id="0be99-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0be99-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="0be99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be99-102">SYNOPSIS</span></span>
<span data-ttu-id="0be99-103">Hizmet örneği siler.</span><span class="sxs-lookup"><span data-stu-id="0be99-103">Deletes a service instance.</span></span>

## <span data-ttu-id="0be99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0be99-104">SYNTAX</span></span>

### <span data-ttu-id="0be99-105">ServiceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0be99-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0be99-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="0be99-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0be99-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0be99-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be99-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0be99-108">DESCRIPTION</span></span>
<span data-ttu-id="0be99-109">Hizmet örneği siler.</span><span class="sxs-lookup"><span data-stu-id="0be99-109">Deletes a service instance.</span></span>

## <span data-ttu-id="0be99-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0be99-110">EXAMPLES</span></span>

### <span data-ttu-id="0be99-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0be99-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0be99-112">Sağlanan bir kaynak grubundaki sağlanan ada sahip mevcut Healthsapı hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="0be99-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="0be99-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0be99-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="0be99-114">Sağlanan RESOURCEID ile mevcut Healthgelişme API 'lerini siler.</span><span class="sxs-lookup"><span data-stu-id="0be99-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="0be99-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0be99-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="0be99-116">Sağlanan Healthgelişme API 'leri hizmet nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="0be99-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="0be99-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0be99-117">PARAMETERS</span></span>

### <span data-ttu-id="0be99-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="0be99-118">-AsJob</span></span>
<span data-ttu-id="0be99-119">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="0be99-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="0be99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be99-120">-DefaultProfile</span></span>
<span data-ttu-id="0be99-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0be99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be99-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0be99-122">-InputObject</span></span>
<span data-ttu-id="0be99-123">Healthumapı hizmet nesnesi</span><span class="sxs-lookup"><span data-stu-id="0be99-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0be99-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0be99-124">-Name</span></span>
<span data-ttu-id="0be99-125">Healthgelişme API 'leri hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="0be99-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be99-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0be99-126">-PassThru</span></span>
<span data-ttu-id="0be99-127">Sağlanmışsa, işlem başarılı olduysa doğru döndürür</span><span class="sxs-lookup"><span data-stu-id="0be99-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="0be99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be99-128">-ResourceGroupName</span></span>
<span data-ttu-id="0be99-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0be99-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be99-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0be99-130">-ResourceId</span></span>
<span data-ttu-id="0be99-131">Healthgelişme API 'leri hizmet RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0be99-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0be99-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0be99-132">-Confirm</span></span>
<span data-ttu-id="0be99-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0be99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be99-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be99-134">-WhatIf</span></span>
<span data-ttu-id="0be99-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0be99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0be99-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0be99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0be99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be99-137">CommonParameters</span></span>
<span data-ttu-id="0be99-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0be99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be99-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0be99-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be99-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0be99-140">INPUTS</span></span>

### <span data-ttu-id="0be99-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0be99-141">System.String</span></span>

### <span data-ttu-id="0be99-142">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="0be99-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="0be99-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0be99-143">OUTPUTS</span></span>

### <span data-ttu-id="0be99-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0be99-144">System.Boolean</span></span>

## <span data-ttu-id="0be99-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0be99-145">NOTES</span></span>

## <span data-ttu-id="0be99-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0be99-146">RELATED LINKS</span></span>
