---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098786"
---
# <span data-ttu-id="9ed37-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ed37-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9ed37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ed37-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed37-103">Özel bir uç noktası bağlantı kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="9ed37-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="9ed37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ed37-104">SYNTAX</span></span>

### <span data-ttu-id="9ed37-105">Byprivatelinkresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ed37-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed37-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9ed37-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed37-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="9ed37-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ed37-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed37-109">**Get-AzPrivateEndpointConnection** cmdlet 'i özel bir uç noktası bağlantı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="9ed37-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="9ed37-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ed37-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed37-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ed37-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="9ed37-112">Bu örnekte, tüm özel uç nokta bağlantılarının listesi MySQL adlı SQL Server 'a aittir.</span><span class="sxs-lookup"><span data-stu-id="9ed37-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="9ed37-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9ed37-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="9ed37-114">Bu örnek, MyPrivateEndpointConnection1 adlı özel bir uç noktası bağlantısını MyPrivateLinkService adlı özel bağlantı hizmetine aittir</span><span class="sxs-lookup"><span data-stu-id="9ed37-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="9ed37-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ed37-115">PARAMETERS</span></span>

### <span data-ttu-id="9ed37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed37-116">-DefaultProfile</span></span>
<span data-ttu-id="9ed37-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ed37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed37-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ed37-118">-Name</span></span>
<span data-ttu-id="9ed37-119">Özel uç noktası bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="9ed37-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed37-120">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="9ed37-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="9ed37-121">Özel uç noktası bağlantısının ait olduğu özel bağlantı kaynağının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="9ed37-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed37-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9ed37-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9ed37-123">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="9ed37-123">The private link resource type.</span></span>

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

### <span data-ttu-id="9ed37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed37-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ed37-125">Özel uç noktası bağlantısının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9ed37-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9ed37-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ed37-126">-ResourceId</span></span>
<span data-ttu-id="9ed37-127">Özel uç noktası bağlantısının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="9ed37-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9ed37-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9ed37-128">-ServiceName</span></span>
<span data-ttu-id="9ed37-129">Özel uç noktası bağlantısının ait olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="9ed37-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="9ed37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed37-130">CommonParameters</span></span>
<span data-ttu-id="9ed37-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ed37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed37-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ed37-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed37-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ed37-133">INPUTS</span></span>

### <span data-ttu-id="9ed37-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed37-134">System.String</span></span>

## <span data-ttu-id="9ed37-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ed37-135">OUTPUTS</span></span>

### <span data-ttu-id="9ed37-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ed37-136">System.Boolean</span></span>

## <span data-ttu-id="9ed37-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ed37-137">NOTES</span></span>

## <span data-ttu-id="9ed37-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ed37-138">RELATED LINKS</span></span>

[<span data-ttu-id="9ed37-139">Onay-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ed37-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ed37-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ed37-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ed37-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ed37-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ed37-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ed37-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
