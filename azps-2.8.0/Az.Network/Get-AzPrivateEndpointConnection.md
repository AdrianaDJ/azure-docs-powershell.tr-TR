---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931720"
---
# <span data-ttu-id="a824f-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a824f-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a824f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a824f-102">SYNOPSIS</span></span>
<span data-ttu-id="a824f-103">Özel bir uç noktası bağlantı kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="a824f-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="a824f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a824f-104">SYNTAX</span></span>

### <span data-ttu-id="a824f-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a824f-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a824f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a824f-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a824f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a824f-107">DESCRIPTION</span></span>
<span data-ttu-id="a824f-108">**Get-AzPrivateEndpointConnection** cmdlet 'i özel bir uç noktası bağlantı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="a824f-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="a824f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a824f-109">EXAMPLES</span></span>

### <span data-ttu-id="a824f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a824f-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="a824f-111">Bu örnekte MyPrivateEndpointConnection1 adlı özel bir uç nokta bağlantısı alınır</span><span class="sxs-lookup"><span data-stu-id="a824f-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="a824f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a824f-112">PARAMETERS</span></span>

### <span data-ttu-id="a824f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a824f-113">-DefaultProfile</span></span>
<span data-ttu-id="a824f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a824f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a824f-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a824f-115">-Description</span></span>
<span data-ttu-id="a824f-116">Eylemin nedeni.</span><span class="sxs-lookup"><span data-stu-id="a824f-116">The reason of action.</span></span>

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

### <span data-ttu-id="a824f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a824f-117">-Name</span></span>
<span data-ttu-id="a824f-118">Özel uç noktası bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="a824f-118">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a824f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a824f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a824f-120">Özel uç noktası bağlantısının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a824f-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a824f-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a824f-121">-ResourceId</span></span>
<span data-ttu-id="a824f-122">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="a824f-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a824f-123">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="a824f-123">-ServiceName</span></span>
<span data-ttu-id="a824f-124">Özel uç noktası bağlantısına sahip özel bağlantı hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="a824f-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="a824f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a824f-125">CommonParameters</span></span>
<span data-ttu-id="a824f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a824f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a824f-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a824f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a824f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a824f-128">INPUTS</span></span>

### <span data-ttu-id="a824f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a824f-129">System.String</span></span>

## <span data-ttu-id="a824f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a824f-130">OUTPUTS</span></span>

### <span data-ttu-id="a824f-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a824f-131">System.Boolean</span></span>

## <span data-ttu-id="a824f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a824f-132">NOTES</span></span>

## <span data-ttu-id="a824f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a824f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a824f-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a824f-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
