---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109520"
---
# <span data-ttu-id="9b907-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b907-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9b907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b907-102">SYNOPSIS</span></span>
<span data-ttu-id="9b907-103">Özel uç noktası bağlantısını reddeder.</span><span class="sxs-lookup"><span data-stu-id="9b907-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="9b907-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b907-104">SYNTAX</span></span>

### <span data-ttu-id="9b907-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b907-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b907-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9b907-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b907-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b907-107">DESCRIPTION</span></span>
<span data-ttu-id="9b907-108">**Deny-AzPrivateEndpointConnection** cmdlet 'i özel uç nokta bağlantısını reddeder.</span><span class="sxs-lookup"><span data-stu-id="9b907-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="9b907-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b907-109">EXAMPLES</span></span>

### <span data-ttu-id="9b907-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b907-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="9b907-111">Bu örnekte özel uç nokta bağlantısı reddeder.</span><span class="sxs-lookup"><span data-stu-id="9b907-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="9b907-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b907-112">PARAMETERS</span></span>

### <span data-ttu-id="9b907-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b907-113">-DefaultProfile</span></span>
<span data-ttu-id="9b907-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b907-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b907-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9b907-115">-Description</span></span>
<span data-ttu-id="9b907-116">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="9b907-116">The reason of action.</span></span>

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

### <span data-ttu-id="9b907-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b907-117">-Name</span></span>
<span data-ttu-id="9b907-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9b907-118">The resource name.</span></span>

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

### <span data-ttu-id="9b907-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9b907-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9b907-120">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="9b907-120">The private link resource type.</span></span>

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

### <span data-ttu-id="9b907-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b907-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b907-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9b907-122">The resource group name.</span></span>

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

### <span data-ttu-id="9b907-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9b907-123">-ResourceId</span></span>
<span data-ttu-id="9b907-124">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="9b907-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9b907-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9b907-125">-ServiceName</span></span>
<span data-ttu-id="9b907-126">Özel uç noktası bağlantısının ait olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="9b907-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="9b907-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b907-127">CommonParameters</span></span>
<span data-ttu-id="9b907-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b907-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b907-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b907-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b907-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b907-130">INPUTS</span></span>

### <span data-ttu-id="9b907-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9b907-131">System.String</span></span>

## <span data-ttu-id="9b907-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b907-132">OUTPUTS</span></span>

### <span data-ttu-id="9b907-133">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9b907-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9b907-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b907-134">NOTES</span></span>

## <span data-ttu-id="9b907-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b907-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b907-136">Onay-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b907-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b907-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b907-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b907-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b907-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9b907-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9b907-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)