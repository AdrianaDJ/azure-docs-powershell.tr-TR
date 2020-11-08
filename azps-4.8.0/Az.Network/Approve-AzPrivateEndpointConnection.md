---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274406"
---
# <span data-ttu-id="8d1fc-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d1fc-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8d1fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1fc-103">Özel uç noktası bağlantısını onaylar.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d1fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d1fc-104">SYNTAX</span></span>

### <span data-ttu-id="8d1fc-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d1fc-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d1fc-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="8d1fc-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1fc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d1fc-107">DESCRIPTION</span></span>
<span data-ttu-id="8d1fc-108">**Onay-AzPrivateEndpointConnection** cmdlet 'i özel uç nokta bağlantısını onaylar.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d1fc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d1fc-109">EXAMPLES</span></span>

### <span data-ttu-id="8d1fc-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d1fc-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="8d1fc-111">Bu örnekte özel uç nokta bağlantısı onaylanır.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d1fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d1fc-112">PARAMETERS</span></span>

### <span data-ttu-id="8d1fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1fc-113">-DefaultProfile</span></span>
<span data-ttu-id="8d1fc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d1fc-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8d1fc-115">-Description</span></span>
<span data-ttu-id="8d1fc-116">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-116">The reason of action.</span></span>

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

### <span data-ttu-id="8d1fc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d1fc-117">-Name</span></span>
<span data-ttu-id="8d1fc-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-118">The resource name.</span></span>

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

### <span data-ttu-id="8d1fc-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8d1fc-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8d1fc-120">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-120">The private link resource type.</span></span>

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

### <span data-ttu-id="8d1fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d1fc-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-122">The resource group name.</span></span>

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

### <span data-ttu-id="8d1fc-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8d1fc-123">-ResourceId</span></span>
<span data-ttu-id="8d1fc-124">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8d1fc-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="8d1fc-125">-ServiceName</span></span>
<span data-ttu-id="8d1fc-126">Özel bağlantı hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-126">The private link service name.</span></span>

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


### <span data-ttu-id="8d1fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1fc-127">CommonParameters</span></span>
<span data-ttu-id="8d1fc-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1fc-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1fc-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d1fc-130">INPUTS</span></span>

### <span data-ttu-id="8d1fc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8d1fc-131">System.String</span></span>

## <span data-ttu-id="8d1fc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d1fc-132">OUTPUTS</span></span>

### <span data-ttu-id="8d1fc-133">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d1fc-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="8d1fc-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d1fc-134">NOTES</span></span>

## <span data-ttu-id="8d1fc-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d1fc-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d1fc-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d1fc-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d1fc-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d1fc-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d1fc-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d1fc-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d1fc-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d1fc-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)