---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931817"
---
# <span data-ttu-id="2fcd4-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fcd4-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2fcd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcd4-103">Özel uç noktası bağlantısını reddeder.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="2fcd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fcd4-104">SYNTAX</span></span>

### <span data-ttu-id="2fcd4-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2fcd4-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fcd4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2fcd4-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fcd4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fcd4-107">DESCRIPTION</span></span>
<span data-ttu-id="2fcd4-108">**Deny-AzPrivateEndpointConnection** cmdlet 'i özel uç nokta bağlantısını reddeder.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="2fcd4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fcd4-109">EXAMPLES</span></span>

### <span data-ttu-id="2fcd4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2fcd4-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="2fcd4-111">Bu örnekte özel uç nokta bağlantısı reddeder.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="2fcd4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fcd4-112">PARAMETERS</span></span>

### <span data-ttu-id="2fcd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcd4-113">-DefaultProfile</span></span>
<span data-ttu-id="2fcd4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fcd4-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2fcd4-115">-Description</span></span>
<span data-ttu-id="2fcd4-116">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-116">The reason of action.</span></span>

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

### <span data-ttu-id="2fcd4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fcd4-117">-Name</span></span>
<span data-ttu-id="2fcd4-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-118">The resource name.</span></span>

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

### <span data-ttu-id="2fcd4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fcd4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fcd4-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-120">The resource group name.</span></span>

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

### <span data-ttu-id="2fcd4-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2fcd4-121">-ResourceId</span></span>
<span data-ttu-id="2fcd4-122">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2fcd4-123">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="2fcd4-123">-ServiceName</span></span>
<span data-ttu-id="2fcd4-124">Özel bağlantı hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-124">The private link service name.</span></span>

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

### <span data-ttu-id="2fcd4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcd4-125">CommonParameters</span></span>
<span data-ttu-id="2fcd4-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcd4-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcd4-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fcd4-128">INPUTS</span></span>

### <span data-ttu-id="2fcd4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2fcd4-129">System.String</span></span>

## <span data-ttu-id="2fcd4-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fcd4-130">OUTPUTS</span></span>

### <span data-ttu-id="2fcd4-131">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fcd4-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2fcd4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fcd4-132">NOTES</span></span>

## <span data-ttu-id="2fcd4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fcd4-133">RELATED LINKS</span></span>

[<span data-ttu-id="2fcd4-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fcd4-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2fcd4-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fcd4-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2fcd4-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fcd4-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)