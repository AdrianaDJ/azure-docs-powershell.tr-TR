---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098781"
---
# <span data-ttu-id="fd15e-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fd15e-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="fd15e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd15e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd15e-103">Özel bir bağlantı kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="fd15e-103">Gets a private link resource.</span></span>

## <span data-ttu-id="fd15e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd15e-104">SYNTAX</span></span>

### <span data-ttu-id="fd15e-105">Byprivatelinkresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd15e-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd15e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd15e-106">DESCRIPTION</span></span>
<span data-ttu-id="fd15e-107">**Get-AzPrivateLinkResource** cmdlet 'i tüm bağlantı kaynaklarını alır privatelinkresource.</span><span class="sxs-lookup"><span data-stu-id="fd15e-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="fd15e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd15e-108">EXAMPLES</span></span>

### <span data-ttu-id="fd15e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd15e-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="fd15e-110">Bu örnekte, tüm özel bağlantı kaynakları e-mySql adlı SQL Server 'a aittir.</span><span class="sxs-lookup"><span data-stu-id="fd15e-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="fd15e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd15e-111">PARAMETERS</span></span>

### <span data-ttu-id="fd15e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd15e-112">-DefaultProfile</span></span>
<span data-ttu-id="fd15e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd15e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd15e-114">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="fd15e-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="fd15e-115">Özel bağlantı kaynağının Azure Resource Manager kimliği.</span><span class="sxs-lookup"><span data-stu-id="fd15e-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="fd15e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd15e-116">CommonParameters</span></span>
<span data-ttu-id="fd15e-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd15e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd15e-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd15e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd15e-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd15e-119">INPUTS</span></span>

### <span data-ttu-id="fd15e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="fd15e-120">System.String</span></span>

## <span data-ttu-id="fd15e-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd15e-121">OUTPUTS</span></span>

### <span data-ttu-id="fd15e-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd15e-122">System.Boolean</span></span>

## <span data-ttu-id="fd15e-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd15e-123">NOTES</span></span>

## <span data-ttu-id="fd15e-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd15e-124">RELATED LINKS</span></span>
