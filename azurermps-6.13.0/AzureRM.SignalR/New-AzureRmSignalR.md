---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590842"
---
# <span data-ttu-id="11cf3-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="11cf3-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="11cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="11cf3-103">Bir SignalR hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="11cf3-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11cf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11cf3-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11cf3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="11cf3-106">Bir SignalR hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="11cf3-106">Create a SignalR service.</span></span>
<span data-ttu-id="11cf3-107">Aşağıdaki değerler belirtilmemişse parametreler için kullanılacaktır:</span><span class="sxs-lookup"><span data-stu-id="11cf3-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="11cf3-108">`ResourceGroupName`: varsayılan kaynak grubu `Set-AzureRmDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="11cf3-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="11cf3-109">`Location`: kaynak grubunun konumu</span><span class="sxs-lookup"><span data-stu-id="11cf3-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="11cf3-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="11cf3-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="11cf3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11cf3-111">EXAMPLES</span></span>

### <span data-ttu-id="11cf3-112">Bir Signall seri oluşturma</span><span class="sxs-lookup"><span data-stu-id="11cf3-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="11cf3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="11cf3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="11cf3-114">-AsJob</span></span>
<span data-ttu-id="11cf3-115">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="11cf3-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="11cf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cf3-116">-DefaultProfile</span></span>
<span data-ttu-id="11cf3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11cf3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11cf3-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="11cf3-118">-Location</span></span>
<span data-ttu-id="11cf3-119">SignalR hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="11cf3-119">The SignalR service location.</span></span> <span data-ttu-id="11cf3-120">Belirtilmemişse, kaynak grubu konumu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="11cf3-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="11cf3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="11cf3-121">-Name</span></span>
<span data-ttu-id="11cf3-122">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="11cf3-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="11cf3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cf3-123">-ResourceGroupName</span></span>
<span data-ttu-id="11cf3-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="11cf3-124">The resource group name.</span></span> <span data-ttu-id="11cf3-125">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="11cf3-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="11cf3-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="11cf3-126">-Sku</span></span>
<span data-ttu-id="11cf3-127">SignalR hizmeti SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="11cf3-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="11cf3-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="11cf3-128">-Tag</span></span>
<span data-ttu-id="11cf3-129">SignalR hizmetinin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="11cf3-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="11cf3-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="11cf3-130">-UnitCount</span></span>
<span data-ttu-id="11cf3-131">1 ila 10 arasında SignalR hizmeti birim sayısı.</span><span class="sxs-lookup"><span data-stu-id="11cf3-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="11cf3-132">Varsayılan 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="11cf3-132">Default to 1.</span></span>

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

### <span data-ttu-id="11cf3-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="11cf3-133">-Confirm</span></span>
<span data-ttu-id="11cf3-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11cf3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11cf3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11cf3-135">-WhatIf</span></span>
<span data-ttu-id="11cf3-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11cf3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11cf3-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11cf3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11cf3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cf3-138">CommonParameters</span></span>
<span data-ttu-id="11cf3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11cf3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cf3-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cf3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cf3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11cf3-141">INPUTS</span></span>

### <span data-ttu-id="11cf3-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="11cf3-142">None</span></span>

## <span data-ttu-id="11cf3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11cf3-143">OUTPUTS</span></span>

### <span data-ttu-id="11cf3-144">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="11cf3-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="11cf3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11cf3-145">NOTES</span></span>

## <span data-ttu-id="11cf3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11cf3-146">RELATED LINKS</span></span>
