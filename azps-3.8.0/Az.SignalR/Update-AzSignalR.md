---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 52e422f6c86f17c6620c58c1034b45250d4edf08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096760"
---
# <span data-ttu-id="7eda3-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="7eda3-101">Update-AzSignalR</span></span>

## <span data-ttu-id="7eda3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eda3-102">SYNOPSIS</span></span>
<span data-ttu-id="7eda3-103">Bir SignalR hizmetini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="7eda3-103">Update a SignalR service.</span></span>

## <span data-ttu-id="7eda3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eda3-104">SYNTAX</span></span>

### <span data-ttu-id="7eda3-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7eda3-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eda3-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7eda3-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eda3-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="7eda3-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eda3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eda3-108">DESCRIPTION</span></span>
<span data-ttu-id="7eda3-109">Bir SignalR hizmetini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="7eda3-109">Update a SignalR service.</span></span>
<span data-ttu-id="7eda3-110">Aşağıdaki değerler belirtilmemişse parametreler için kullanılacaktır:</span><span class="sxs-lookup"><span data-stu-id="7eda3-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="7eda3-111">`ResourceGroupName`: varsayılan kaynak grubu `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="7eda3-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="7eda3-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="7eda3-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="7eda3-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eda3-113">EXAMPLES</span></span>

### <span data-ttu-id="7eda3-114">Belirli bir SignalR hizmetini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="7eda3-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="7eda3-115">ServiceMode ve AllowedOrigin belirtme</span><span class="sxs-lookup"><span data-stu-id="7eda3-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="7eda3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eda3-116">PARAMETERS</span></span>

### <span data-ttu-id="7eda3-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="7eda3-117">-AllowedOrigin</span></span>
<span data-ttu-id="7eda3-118">SignalR hizmeti için izin verilen çıkış.</span><span class="sxs-lookup"><span data-stu-id="7eda3-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="7eda3-119">Tümüne izin vermek için "\*" kullanın ve listeden diğer tüm kaynakları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7eda3-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="7eda3-120">Etki alanı veya TLD 'den sonra eğik çizgiler kullanılamaz</span><span class="sxs-lookup"><span data-stu-id="7eda3-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="7eda3-121">-AsJob</span></span>
<span data-ttu-id="7eda3-122">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7eda3-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="7eda3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eda3-123">-DefaultProfile</span></span>
<span data-ttu-id="7eda3-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7eda3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eda3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eda3-125">-InputObject</span></span>
<span data-ttu-id="7eda3-126">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7eda3-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="7eda3-127">-Name</span></span>
<span data-ttu-id="7eda3-128">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="7eda3-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eda3-129">-ResourceGroupName</span></span>
<span data-ttu-id="7eda3-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7eda3-130">The resource group name.</span></span>
<span data-ttu-id="7eda3-131">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7eda3-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7eda3-132">-ResourceId</span></span>
<span data-ttu-id="7eda3-133">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7eda3-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="7eda3-134">-ServiceMode</span></span>
<span data-ttu-id="7eda3-135">SignalR hizmeti için hizmet modu.</span><span class="sxs-lookup"><span data-stu-id="7eda3-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="7eda3-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="7eda3-136">-Sku</span></span>
<span data-ttu-id="7eda3-137">SignalR hizmeti SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="7eda3-137">The SignalR service SKU.</span></span>
<span data-ttu-id="7eda3-138">Varsayılan "Standard_S1" olarak.</span><span class="sxs-lookup"><span data-stu-id="7eda3-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="7eda3-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7eda3-139">-Tag</span></span>
<span data-ttu-id="7eda3-140">SignalR hizmetinin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="7eda3-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="7eda3-141">-UnitCount</span></span>
<span data-ttu-id="7eda3-142">SignalR hizmeti birim sayısı, yalnızca {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="7eda3-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="7eda3-143">Varsayılan 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="7eda3-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eda3-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="7eda3-144">-Confirm</span></span>
<span data-ttu-id="7eda3-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7eda3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eda3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eda3-146">-WhatIf</span></span>
<span data-ttu-id="7eda3-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7eda3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eda3-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7eda3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eda3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eda3-149">CommonParameters</span></span>
<span data-ttu-id="7eda3-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eda3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eda3-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7eda3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eda3-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eda3-152">INPUTS</span></span>

### <span data-ttu-id="7eda3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7eda3-153">System.String</span></span>

### <span data-ttu-id="7eda3-154">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7eda3-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="7eda3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eda3-155">OUTPUTS</span></span>

### <span data-ttu-id="7eda3-156">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7eda3-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="7eda3-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eda3-157">NOTES</span></span>

## <span data-ttu-id="7eda3-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eda3-158">RELATED LINKS</span></span>