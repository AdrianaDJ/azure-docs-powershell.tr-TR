---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325762"
---
# <span data-ttu-id="5e4b4-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5e4b4-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="5e4b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4b4-103">Özel bağlantı hizmetinde özel bir uç noktası bağlantı durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="5e4b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e4b4-104">SYNTAX</span></span>

### <span data-ttu-id="5e4b4-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e4b4-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e4b4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="5e4b4-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e4b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e4b4-107">DESCRIPTION</span></span>
<span data-ttu-id="5e4b4-108">**Set-AzPrivateEndpointConnection** cmdlet 'i özel bir bağlantı hizmetinde özel bir uç noktası bağlantı durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="5e4b4-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="5e4b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="5e4b4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e4b4-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="5e4b4-111">Bu örnek, özel bir uç noktası bağlantı durumunu Onaylandı olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="5e4b4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e4b4-112">PARAMETERS</span></span>

### <span data-ttu-id="5e4b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4b4-113">-DefaultProfile</span></span>
<span data-ttu-id="5e4b4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e4b4-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5e4b4-115">-Description</span></span>
<span data-ttu-id="5e4b4-116">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-116">The reason of action.</span></span>

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

### <span data-ttu-id="5e4b4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e4b4-117">-Name</span></span>
<span data-ttu-id="5e4b4-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-118">The resource name.</span></span>

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

### <span data-ttu-id="5e4b4-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="5e4b4-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="5e4b4-120">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-120">The private link resource type.</span></span>

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

### <span data-ttu-id="5e4b4-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="5e4b4-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="5e4b4-122">Kaynağı onayladı veya reddetti.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e4b4-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-124">The resource group name.</span></span>

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

### <span data-ttu-id="5e4b4-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5e4b4-125">-ResourceId</span></span>
<span data-ttu-id="5e4b4-126">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="5e4b4-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="5e4b4-127">-ServiceName</span></span>
<span data-ttu-id="5e4b4-128">Özel bağlantı hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-128">The private link service name.</span></span>

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

### <span data-ttu-id="5e4b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4b4-129">CommonParameters</span></span>
<span data-ttu-id="5e4b4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4b4-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e4b4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4b4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e4b4-132">INPUTS</span></span>

### <span data-ttu-id="5e4b4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5e4b4-133">System.String</span></span>

## <span data-ttu-id="5e4b4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e4b4-134">OUTPUTS</span></span>

### <span data-ttu-id="5e4b4-135">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5e4b4-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="5e4b4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e4b4-136">NOTES</span></span>

## <span data-ttu-id="5e4b4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e4b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="5e4b4-138">Onay-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5e4b4-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5e4b4-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5e4b4-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5e4b4-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5e4b4-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5e4b4-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5e4b4-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)