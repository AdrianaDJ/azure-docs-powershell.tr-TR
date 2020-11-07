---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932258"
---
# <span data-ttu-id="25f15-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25f15-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="25f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f15-102">SYNOPSIS</span></span>
<span data-ttu-id="25f15-103">Özel uç nokta bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25f15-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="25f15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25f15-104">SYNTAX</span></span>

### <span data-ttu-id="25f15-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25f15-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25f15-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="25f15-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f15-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="25f15-107">DESCRIPTION</span></span>
<span data-ttu-id="25f15-108">**Remove-AzPrivateEndpointConnection** cmdlet 'i özel uç nokta bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25f15-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="25f15-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25f15-109">EXAMPLES</span></span>

### <span data-ttu-id="25f15-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25f15-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="25f15-111">Bu örnekte MyPrivateEndpointConnection1 adlı özel bir uç nokta bağlantısı kaldırılsın</span><span class="sxs-lookup"><span data-stu-id="25f15-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="25f15-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25f15-112">PARAMETERS</span></span>

### <span data-ttu-id="25f15-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="25f15-113">-AsJob</span></span>
<span data-ttu-id="25f15-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="25f15-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25f15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f15-115">-DefaultProfile</span></span>
<span data-ttu-id="25f15-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25f15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25f15-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="25f15-117">-Description</span></span>
<span data-ttu-id="25f15-118">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="25f15-118">The reason of action.</span></span>

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

### <span data-ttu-id="25f15-119">-Force</span><span class="sxs-lookup"><span data-stu-id="25f15-119">-Force</span></span>
<span data-ttu-id="25f15-120">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="25f15-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="25f15-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="25f15-121">-Name</span></span>
<span data-ttu-id="25f15-122">Özel uç noktası bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="25f15-122">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="25f15-123">-PassThru</span></span>
<span data-ttu-id="25f15-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="25f15-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25f15-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="25f15-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25f15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f15-126">-ResourceGroupName</span></span>
<span data-ttu-id="25f15-127">Özel uç noktası bağlantısının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="25f15-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="25f15-128">-ResourceId</span></span>
<span data-ttu-id="25f15-129">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="25f15-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="25f15-130">-ServiceName</span></span>
<span data-ttu-id="25f15-131">Özel uç noktası bağlantısına sahip özel bağlantı hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="25f15-131">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f15-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="25f15-132">-Confirm</span></span>
<span data-ttu-id="25f15-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25f15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f15-134">-WhatIf</span></span>
<span data-ttu-id="25f15-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25f15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f15-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25f15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f15-137">CommonParameters</span></span>
<span data-ttu-id="25f15-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25f15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f15-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="25f15-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f15-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25f15-140">INPUTS</span></span>

### <span data-ttu-id="25f15-141">System. String</span><span class="sxs-lookup"><span data-stu-id="25f15-141">System.String</span></span>

## <span data-ttu-id="25f15-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25f15-142">OUTPUTS</span></span>

### <span data-ttu-id="25f15-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25f15-143">System.Boolean</span></span>

## <span data-ttu-id="25f15-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25f15-144">NOTES</span></span>

## <span data-ttu-id="25f15-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25f15-145">RELATED LINKS</span></span>

[<span data-ttu-id="25f15-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25f15-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
