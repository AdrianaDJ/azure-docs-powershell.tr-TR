---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 74f531e48ca873d3853aba3312d6bb10edccdfaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098739"
---
# <span data-ttu-id="df189-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="df189-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="df189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df189-102">SYNOPSIS</span></span>
<span data-ttu-id="df189-103">Özel bağlantı hizmeti bağlantı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df189-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="df189-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df189-104">SYNTAX</span></span>

### <span data-ttu-id="df189-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df189-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df189-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="df189-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df189-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="df189-107">DESCRIPTION</span></span>
<span data-ttu-id="df189-108">**Yeni-AzPrivateLinkServiceConnection** cmdlet 'i özel bağlantı hizmeti bağlantı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df189-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="df189-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df189-109">EXAMPLES</span></span>

### <span data-ttu-id="df189-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df189-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="df189-111">Bu örnek, Özel uç nokta oluştururken kullanmak üzere bellekte özel bir bağlantı hizmeti bağlantı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df189-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="df189-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df189-112">PARAMETERS</span></span>

### <span data-ttu-id="df189-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df189-113">-DefaultProfile</span></span>
<span data-ttu-id="df189-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df189-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df189-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="df189-115">-GroupId</span></span>
<span data-ttu-id="df189-116">Grup Kimliği listesi.</span><span class="sxs-lookup"><span data-stu-id="df189-116">The list of group id.</span></span>

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

### <span data-ttu-id="df189-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="df189-117">-Name</span></span>
<span data-ttu-id="df189-118">Özel bağlantı hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="df189-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df189-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="df189-119">-PrivateLinkService</span></span>
<span data-ttu-id="df189-120">Özel bağlantı hizmeti.</span><span class="sxs-lookup"><span data-stu-id="df189-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df189-121">-Privatelinkserviceıd</span><span class="sxs-lookup"><span data-stu-id="df189-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="df189-122">Özel bağlantı hizmeti kimliği.</span><span class="sxs-lookup"><span data-stu-id="df189-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df189-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="df189-123">-RequestMessage</span></span>
<span data-ttu-id="df189-124">İstek iletisi.</span><span class="sxs-lookup"><span data-stu-id="df189-124">The request message.</span></span>

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

### <span data-ttu-id="df189-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df189-125">CommonParameters</span></span>
<span data-ttu-id="df189-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df189-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df189-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="df189-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df189-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df189-128">INPUTS</span></span>

### <span data-ttu-id="df189-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="df189-129">None</span></span>

## <span data-ttu-id="df189-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df189-130">OUTPUTS</span></span>

### <span data-ttu-id="df189-131">Microsoft. Azure. Commands. Network. model. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="df189-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="df189-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df189-132">NOTES</span></span>

## <span data-ttu-id="df189-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df189-133">RELATED LINKS</span></span>

[<span data-ttu-id="df189-134">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="df189-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)