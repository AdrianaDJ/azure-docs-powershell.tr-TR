---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097317"
---
# <span data-ttu-id="14c4c-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="14c4c-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="14c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="14c4c-103">Verilen Yuva adı için bir yönlendirme kuralı edinin.</span><span class="sxs-lookup"><span data-stu-id="14c4c-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="14c4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14c4c-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="14c4c-106">**Get-AzWebAppTrafficRouting** cmdlet 'ı bir Azure Web App yuvasından yönlendirme kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="14c4c-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="14c4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="14c4c-108">Örnek 1, WebApp yuvasından özel yönlendirme kuralını alır</span><span class="sxs-lookup"><span data-stu-id="14c4c-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="14c4c-109">Bu komut, belirli bir WebApp yuvasının yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="14c4c-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="14c4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14c4c-110">PARAMETERS</span></span>

### <span data-ttu-id="14c4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c4c-111">-DefaultProfile</span></span>
<span data-ttu-id="14c4c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14c4c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c4c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c4c-113">-ResourceGroupName</span></span>
<span data-ttu-id="14c4c-114">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="14c4c-114">Resource Group Name</span></span>

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

### <span data-ttu-id="14c4c-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="14c4c-115">-RuleName</span></span>
<span data-ttu-id="14c4c-116">Kural adı</span><span class="sxs-lookup"><span data-stu-id="14c4c-116">Rule Name</span></span>
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

### <span data-ttu-id="14c4c-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="14c4c-117">-WebAppName</span></span>
<span data-ttu-id="14c4c-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="14c4c-118">WebApp Name</span></span>

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

### <span data-ttu-id="14c4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c4c-119">CommonParameters</span></span>
<span data-ttu-id="14c4c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14c4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c4c-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14c4c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c4c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14c4c-122">INPUTS</span></span>

### <span data-ttu-id="14c4c-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14c4c-123">None</span></span>

## <span data-ttu-id="14c4c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14c4c-124">OUTPUTS</span></span>

### <span data-ttu-id="14c4c-125">Microsoft. Azure. Management. Web sitesi. modeller. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="14c4c-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="14c4c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14c4c-126">NOTES</span></span>

## <span data-ttu-id="14c4c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14c4c-127">RELATED LINKS</span></span>

[<span data-ttu-id="14c4c-128">Güncelleştirme-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="14c4c-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="14c4c-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="14c4c-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="14c4c-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="14c4c-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)