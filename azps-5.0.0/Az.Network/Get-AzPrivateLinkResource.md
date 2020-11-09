---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323848"
---
# <span data-ttu-id="285d3-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="285d3-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="285d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285d3-102">SYNOPSIS</span></span>
<span data-ttu-id="285d3-103">Özel bir bağlantı kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="285d3-103">Gets a private link resource.</span></span>

## <span data-ttu-id="285d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="285d3-104">SYNTAX</span></span>

### <span data-ttu-id="285d3-105">Byprivatelinkresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="285d3-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="285d3-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="285d3-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="285d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="285d3-107">DESCRIPTION</span></span>
<span data-ttu-id="285d3-108">**Get-AzPrivateLinkResource** cmdlet 'i tüm bağlantı kaynaklarını alır privatelinkresource.</span><span class="sxs-lookup"><span data-stu-id="285d3-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="285d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="285d3-109">EXAMPLES</span></span>

### <span data-ttu-id="285d3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="285d3-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="285d3-111">Bu örnekte, tüm özel bağlantı kaynakları e-mySql adlı SQL Server 'a aittir.</span><span class="sxs-lookup"><span data-stu-id="285d3-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="285d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="285d3-112">PARAMETERS</span></span>

### <span data-ttu-id="285d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d3-113">-DefaultProfile</span></span>
<span data-ttu-id="285d3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="285d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="285d3-115">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="285d3-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="285d3-116">Özel bağlantı kaynağının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="285d3-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="285d3-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="285d3-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="285d3-118">Özel bağlantı kaynağı türü.</span><span class="sxs-lookup"><span data-stu-id="285d3-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="285d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="285d3-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="285d3-120">The resource group name.</span></span>

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

### <span data-ttu-id="285d3-121">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="285d3-121">-ServiceName</span></span>
<span data-ttu-id="285d3-122">Özel bağlantı hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="285d3-122">The private link service name.</span></span>

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

### <span data-ttu-id="285d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d3-123">CommonParameters</span></span>
<span data-ttu-id="285d3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="285d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d3-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="285d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="285d3-126">INPUTS</span></span>

### <span data-ttu-id="285d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="285d3-127">System.String</span></span>

## <span data-ttu-id="285d3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="285d3-128">OUTPUTS</span></span>

### <span data-ttu-id="285d3-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="285d3-129">System.Boolean</span></span>

## <span data-ttu-id="285d3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="285d3-130">NOTES</span></span>

## <span data-ttu-id="285d3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="285d3-131">RELATED LINKS</span></span>
