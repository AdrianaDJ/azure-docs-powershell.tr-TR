---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760570"
---
# <span data-ttu-id="15ad7-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="15ad7-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="15ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="15ad7-103">ExpressRoutePort kaynaklarının kullanılabileceği konumları alır.</span><span class="sxs-lookup"><span data-stu-id="15ad7-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="15ad7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15ad7-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15ad7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="15ad7-106">ExpressRoutePort kaynaklarının kullanılabileceği konumları almak için **Get-AzExpressRoutePortsLocation** cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="15ad7-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="15ad7-107">Giriş olarak belirli bir konum verildiğinde cmdlet bu konumun (yani, bu konumda kullanılabilir bant genişlikleri listesi) ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="15ad7-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="15ad7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15ad7-108">EXAMPLES</span></span>

### <span data-ttu-id="15ad7-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15ad7-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="15ad7-110">ExpressRoutePort kaynaklarının kullanılabileceği konumları listeler.</span><span class="sxs-lookup"><span data-stu-id="15ad7-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="15ad7-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="15ad7-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="15ad7-112">$Loc konumunda bulunan ExpressRoutePort bant genişliklerini listeler.</span><span class="sxs-lookup"><span data-stu-id="15ad7-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="15ad7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15ad7-113">PARAMETERS</span></span>

### <span data-ttu-id="15ad7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ad7-114">-DefaultProfile</span></span>
<span data-ttu-id="15ad7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15ad7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15ad7-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="15ad7-116">-LocationName</span></span>
<span data-ttu-id="15ad7-117">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="15ad7-117">The name of the location.</span></span>

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

### <span data-ttu-id="15ad7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ad7-118">CommonParameters</span></span>
<span data-ttu-id="15ad7-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15ad7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ad7-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15ad7-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ad7-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15ad7-121">INPUTS</span></span>

### <span data-ttu-id="15ad7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="15ad7-122">System.String</span></span>

## <span data-ttu-id="15ad7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15ad7-123">OUTPUTS</span></span>

### <span data-ttu-id="15ad7-124">Microsoft. Azure. Commands. Network. model. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="15ad7-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="15ad7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15ad7-125">NOTES</span></span>

## <span data-ttu-id="15ad7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15ad7-126">RELATED LINKS</span></span>
