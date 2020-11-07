---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751748"
---
# <span data-ttu-id="07295-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="07295-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="07295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07295-102">SYNOPSIS</span></span>
<span data-ttu-id="07295-103">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="07295-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="07295-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07295-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07295-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07295-105">DESCRIPTION</span></span>
<span data-ttu-id="07295-106">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="07295-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="07295-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07295-107">EXAMPLES</span></span>

### <span data-ttu-id="07295-108">Örnek 1 kota ölçülerini alın</span><span class="sxs-lookup"><span data-stu-id="07295-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="07295-109">"Myiothub" adındaki IotHub için kota ölçümü bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="07295-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="07295-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07295-110">PARAMETERS</span></span>

### <span data-ttu-id="07295-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07295-111">-DefaultProfile</span></span>
<span data-ttu-id="07295-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="07295-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07295-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="07295-113">-Name</span></span>
<span data-ttu-id="07295-114">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="07295-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="07295-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07295-115">-ResourceGroupName</span></span>
<span data-ttu-id="07295-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="07295-116">Resource Group Name</span></span>

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

### <span data-ttu-id="07295-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07295-117">CommonParameters</span></span>
<span data-ttu-id="07295-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07295-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07295-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07295-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07295-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07295-120">INPUTS</span></span>

### <span data-ttu-id="07295-121">System. String</span><span class="sxs-lookup"><span data-stu-id="07295-121">System.String</span></span>

## <span data-ttu-id="07295-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07295-122">OUTPUTS</span></span>

### <span data-ttu-id="07295-123">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubquotametric</span><span class="sxs-lookup"><span data-stu-id="07295-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="07295-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07295-124">NOTES</span></span>

## <span data-ttu-id="07295-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07295-125">RELATED LINKS</span></span>
