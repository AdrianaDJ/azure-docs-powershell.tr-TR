---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103824"
---
# <span data-ttu-id="e21cc-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="e21cc-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="e21cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e21cc-103">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e21cc-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="e21cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e21cc-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e21cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e21cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e21cc-106">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e21cc-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="e21cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e21cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e21cc-108">Örnek 1 kota ölçülerini alın</span><span class="sxs-lookup"><span data-stu-id="e21cc-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e21cc-109">"Myiothub" adındaki IotHub için kota ölçümü bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="e21cc-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e21cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e21cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e21cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21cc-111">-DefaultProfile</span></span>
<span data-ttu-id="e21cc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e21cc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e21cc-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e21cc-113">-Name</span></span>
<span data-ttu-id="e21cc-114">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="e21cc-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21cc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21cc-115">-ResourceGroupName</span></span>
<span data-ttu-id="e21cc-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e21cc-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21cc-117">CommonParameters</span></span>
<span data-ttu-id="e21cc-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e21cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21cc-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e21cc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21cc-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e21cc-120">INPUTS</span></span>

### <span data-ttu-id="e21cc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e21cc-121">System.String</span></span>

## <span data-ttu-id="e21cc-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e21cc-122">OUTPUTS</span></span>

### <span data-ttu-id="e21cc-123">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubquotametric</span><span class="sxs-lookup"><span data-stu-id="e21cc-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="e21cc-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e21cc-124">NOTES</span></span>

## <span data-ttu-id="e21cc-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e21cc-125">RELATED LINKS</span></span>
