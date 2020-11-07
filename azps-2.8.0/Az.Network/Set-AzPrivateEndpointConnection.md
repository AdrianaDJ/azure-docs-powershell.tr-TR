---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932757"
---
# <span data-ttu-id="06713-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="06713-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="06713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06713-102">SYNOPSIS</span></span>
<span data-ttu-id="06713-103">Özel bağlantı hizmetinde özel bir uç noktası bağlantı durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06713-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="06713-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06713-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06713-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06713-105">DESCRIPTION</span></span>
<span data-ttu-id="06713-106">**Set-AzPrivateEndpointConnection** cmdlet 'i özel bir bağlantı hizmetinde özel bir uç noktası bağlantı durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="06713-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="06713-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06713-107">EXAMPLES</span></span>

### <span data-ttu-id="06713-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06713-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="06713-109">Bu örnek, özel bir uç noktası bağlantı durumunu Onaylandı olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06713-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="06713-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06713-110">PARAMETERS</span></span>

### <span data-ttu-id="06713-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06713-111">-DefaultProfile</span></span>
<span data-ttu-id="06713-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06713-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06713-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="06713-113">-Description</span></span>
<span data-ttu-id="06713-114">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="06713-114">The reason of action.</span></span>

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

### <span data-ttu-id="06713-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="06713-115">-Name</span></span>
<span data-ttu-id="06713-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="06713-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06713-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="06713-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="06713-118">Kaynağı onayladı veya reddetti.</span><span class="sxs-lookup"><span data-stu-id="06713-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="06713-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06713-119">-ResourceGroupName</span></span>
<span data-ttu-id="06713-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="06713-120">The resource group name.</span></span>

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

### <span data-ttu-id="06713-121">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="06713-121">-ServiceName</span></span>
<span data-ttu-id="06713-122">Özel bağlantı hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="06713-122">The private link service name.</span></span>

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

### <span data-ttu-id="06713-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06713-123">CommonParameters</span></span>
<span data-ttu-id="06713-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06713-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06713-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06713-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06713-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06713-126">INPUTS</span></span>

### <span data-ttu-id="06713-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06713-127">System.String</span></span>

## <span data-ttu-id="06713-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06713-128">OUTPUTS</span></span>

### <span data-ttu-id="06713-129">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06713-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="06713-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06713-130">NOTES</span></span>

## <span data-ttu-id="06713-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06713-131">RELATED LINKS</span></span>
