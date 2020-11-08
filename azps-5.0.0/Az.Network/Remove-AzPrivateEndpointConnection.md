---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278106"
---
# <span data-ttu-id="553cd-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="553cd-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="553cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553cd-102">SYNOPSIS</span></span>
<span data-ttu-id="553cd-103">Özel uç nokta bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="553cd-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="553cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="553cd-104">SYNTAX</span></span>

### <span data-ttu-id="553cd-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="553cd-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553cd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="553cd-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="553cd-107">DESCRIPTION</span></span>
<span data-ttu-id="553cd-108">**Remove-AzPrivateEndpointConnection** cmdlet 'i özel uç nokta bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="553cd-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="553cd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="553cd-109">EXAMPLES</span></span>

### <span data-ttu-id="553cd-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="553cd-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="553cd-111">Bu örnekte MyPrivateEndpointConnection1 adlı özel bir uç nokta bağlantısı kaldırılsın</span><span class="sxs-lookup"><span data-stu-id="553cd-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="553cd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="553cd-112">PARAMETERS</span></span>

### <span data-ttu-id="553cd-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="553cd-113">-AsJob</span></span>
<span data-ttu-id="553cd-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="553cd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="553cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553cd-115">-DefaultProfile</span></span>
<span data-ttu-id="553cd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="553cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="553cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="553cd-117">-Force</span></span>
<span data-ttu-id="553cd-118">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="553cd-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="553cd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="553cd-119">-Name</span></span>
<span data-ttu-id="553cd-120">Özel uç noktası bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="553cd-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="553cd-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="553cd-121">-PassThru</span></span>
<span data-ttu-id="553cd-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="553cd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="553cd-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="553cd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="553cd-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="553cd-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="553cd-125">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="553cd-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="553cd-127">Özel uç noktası bağlantısının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="553cd-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="553cd-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="553cd-128">-ResourceId</span></span>
<span data-ttu-id="553cd-129">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="553cd-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="553cd-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="553cd-130">-ServiceName</span></span>
<span data-ttu-id="553cd-131">Özel uç noktası bağlantısının ait olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="553cd-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="553cd-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="553cd-132">-Confirm</span></span>
<span data-ttu-id="553cd-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="553cd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553cd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553cd-134">-WhatIf</span></span>
<span data-ttu-id="553cd-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="553cd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553cd-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="553cd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553cd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553cd-137">CommonParameters</span></span>
<span data-ttu-id="553cd-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="553cd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553cd-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="553cd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553cd-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="553cd-140">INPUTS</span></span>

### <span data-ttu-id="553cd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="553cd-141">System.String</span></span>

## <span data-ttu-id="553cd-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="553cd-142">OUTPUTS</span></span>

### <span data-ttu-id="553cd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="553cd-143">System.Boolean</span></span>

## <span data-ttu-id="553cd-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="553cd-144">NOTES</span></span>

## <span data-ttu-id="553cd-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="553cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="553cd-146">Onay-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="553cd-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="553cd-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="553cd-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="553cd-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="553cd-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="553cd-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="553cd-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
