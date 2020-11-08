---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266075"
---
# <span data-ttu-id="33882-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="33882-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="33882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33882-102">SYNOPSIS</span></span>
<span data-ttu-id="33882-103">Otomatik onaylanan özel bir uç noktasına bağlanabilen özel bağlantı hizmeti kimliği dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="33882-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="33882-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33882-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33882-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33882-105">DESCRIPTION</span></span>
<span data-ttu-id="33882-106">**Get-Azautoapproma Privatelinkservice** , otomatik onaylı olarak özel bir uç noktasına bağlanabilen özel bir hizmet kimliği dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="33882-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="33882-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33882-107">EXAMPLES</span></span>

### <span data-ttu-id="33882-108">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="33882-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="33882-109">Bu örnekte, otomatik onaylı olarak özel bir uç noktasına bağlanabilen özel bir hizmet kimliği dizisi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="33882-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="33882-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33882-110">PARAMETERS</span></span>

### <span data-ttu-id="33882-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33882-111">-DefaultProfile</span></span>
<span data-ttu-id="33882-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33882-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33882-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="33882-113">-Location</span></span>
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

### <span data-ttu-id="33882-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33882-114">-ResourceGroupName</span></span>
<span data-ttu-id="33882-115">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33882-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="33882-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33882-116">CommonParameters</span></span>
<span data-ttu-id="33882-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33882-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33882-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33882-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33882-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33882-119">INPUTS</span></span>

### <span data-ttu-id="33882-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33882-120">None</span></span>

## <span data-ttu-id="33882-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33882-121">OUTPUTS</span></span>

### <span data-ttu-id="33882-122">Microsoft. Azure. Commands. Network. model. Psautoapprolerlerlinkservice</span><span class="sxs-lookup"><span data-stu-id="33882-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="33882-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33882-123">NOTES</span></span>

## <span data-ttu-id="33882-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33882-124">RELATED LINKS</span></span>
