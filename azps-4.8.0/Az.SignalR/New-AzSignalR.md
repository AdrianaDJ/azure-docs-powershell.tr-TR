---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110268"
---
# <span data-ttu-id="a3601-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="a3601-101">New-AzSignalR</span></span>

## <span data-ttu-id="a3601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3601-102">SYNOPSIS</span></span>
<span data-ttu-id="a3601-103">Bir SignalR hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3601-103">Create a SignalR service.</span></span>

## <span data-ttu-id="a3601-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3601-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3601-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3601-105">DESCRIPTION</span></span>
<span data-ttu-id="a3601-106">Bir SignalR hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3601-106">Create a SignalR service.</span></span>
<span data-ttu-id="a3601-107">Aşağıdaki değerler belirtilmemişse parametreler için kullanılacaktır:</span><span class="sxs-lookup"><span data-stu-id="a3601-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="a3601-108">`ResourceGroupName`: varsayılan kaynak grubu `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="a3601-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="a3601-109">`Location`: kaynak grubunun konumu</span><span class="sxs-lookup"><span data-stu-id="a3601-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="a3601-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="a3601-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="a3601-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3601-111">EXAMPLES</span></span>

### <span data-ttu-id="a3601-112">SignalR hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3601-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="a3601-113">ServiceMode ve AllowedOrigin belirtme</span><span class="sxs-lookup"><span data-stu-id="a3601-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="a3601-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3601-114">PARAMETERS</span></span>

### <span data-ttu-id="a3601-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="a3601-115">-AllowedOrigin</span></span>
<span data-ttu-id="a3601-116">SignalR hizmeti için izin verilen çıkış.</span><span class="sxs-lookup"><span data-stu-id="a3601-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="a3601-117">Tümüne izin vermek için "\*" kullanın ve listeden diğer tüm kaynakları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a3601-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="a3601-118">Etki alanı veya TLD 'den sonra eğik çizgiler kullanılamaz</span><span class="sxs-lookup"><span data-stu-id="a3601-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="a3601-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="a3601-119">-AsJob</span></span>
<span data-ttu-id="a3601-120">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a3601-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="a3601-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3601-121">-DefaultProfile</span></span>
<span data-ttu-id="a3601-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3601-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3601-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3601-123">-Location</span></span>
<span data-ttu-id="a3601-124">SignalR hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="a3601-124">The SignalR service location.</span></span> <span data-ttu-id="a3601-125">Belirtilmemişse, kaynak grubu konumu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3601-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="a3601-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3601-126">-Name</span></span>
<span data-ttu-id="a3601-127">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="a3601-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3601-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3601-128">-ResourceGroupName</span></span>
<span data-ttu-id="a3601-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a3601-129">The resource group name.</span></span> <span data-ttu-id="a3601-130">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a3601-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="a3601-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="a3601-131">-ServiceMode</span></span>
<span data-ttu-id="a3601-132">SignalR hizmeti için hizmet modu.</span><span class="sxs-lookup"><span data-stu-id="a3601-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="a3601-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a3601-133">-Sku</span></span>
<span data-ttu-id="a3601-134">SignalR hizmeti SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="a3601-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3601-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a3601-135">-Tag</span></span>
<span data-ttu-id="a3601-136">SignalR hizmetinin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a3601-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="a3601-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="a3601-137">-UnitCount</span></span>
<span data-ttu-id="a3601-138">1 ila 10 arasında SignalR hizmeti birim sayısı.</span><span class="sxs-lookup"><span data-stu-id="a3601-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="a3601-139">Varsayılan 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="a3601-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3601-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3601-140">-Confirm</span></span>
<span data-ttu-id="a3601-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3601-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3601-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3601-142">-WhatIf</span></span>
<span data-ttu-id="a3601-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3601-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3601-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3601-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3601-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3601-145">CommonParameters</span></span>
<span data-ttu-id="a3601-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3601-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3601-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3601-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3601-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3601-148">INPUTS</span></span>

### <span data-ttu-id="a3601-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3601-149">System.String</span></span>

## <span data-ttu-id="a3601-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3601-150">OUTPUTS</span></span>

### <span data-ttu-id="a3601-151">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a3601-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="a3601-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3601-152">NOTES</span></span>

## <span data-ttu-id="a3601-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3601-153">RELATED LINKS</span></span>
