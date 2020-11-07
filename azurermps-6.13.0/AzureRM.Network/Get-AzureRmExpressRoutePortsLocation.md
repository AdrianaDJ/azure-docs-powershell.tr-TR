---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764622"
---
# <span data-ttu-id="7fa72-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="7fa72-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="7fa72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fa72-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa72-103">ExpressRoutePort kaynaklarının kullanılabileceği konumları alır.</span><span class="sxs-lookup"><span data-stu-id="7fa72-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fa72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fa72-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fa72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fa72-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa72-106">**Get-AzureRmExpressRoutePortsLocation** cmdlet 'ı ExpressRoutePort kaynaklarının kullanılabileceği konumları almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7fa72-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="7fa72-107">Giriş olarak belirli bir konum verildiğinde cmdlet bu konumun (yani, bu konumda kullanılabilir bant genişlikleri listesi) ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7fa72-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="7fa72-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fa72-108">EXAMPLES</span></span>

### <span data-ttu-id="7fa72-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fa72-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="7fa72-110">ExpressRoutePort kaynaklarının kullanılabileceği konumları listeler.</span><span class="sxs-lookup"><span data-stu-id="7fa72-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="7fa72-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7fa72-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="7fa72-112">$Loc konumunda bulunan ExpressRoutePort bant genişliklerini listeler.</span><span class="sxs-lookup"><span data-stu-id="7fa72-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="7fa72-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fa72-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa72-114">-DefaultProfile</span></span>
<span data-ttu-id="7fa72-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fa72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa72-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="7fa72-116">-LocationName</span></span>
<span data-ttu-id="7fa72-117">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="7fa72-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa72-118">CommonParameters</span></span>
<span data-ttu-id="7fa72-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fa72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa72-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fa72-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa72-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fa72-121">INPUTS</span></span>

### <span data-ttu-id="7fa72-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7fa72-122">System.String</span></span>

## <span data-ttu-id="7fa72-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fa72-123">OUTPUTS</span></span>

### <span data-ttu-id="7fa72-124">Microsoft. Azure. Commands. Network. model. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="7fa72-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="7fa72-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fa72-125">NOTES</span></span>

## <span data-ttu-id="7fa72-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fa72-126">RELATED LINKS</span></span>
