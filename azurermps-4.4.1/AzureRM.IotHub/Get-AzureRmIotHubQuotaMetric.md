---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: f0a3b446c6d40ff07efc35ca51cdf7f422491f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593113"
---
# <span data-ttu-id="2a400-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="2a400-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="2a400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a400-102">SYNOPSIS</span></span>
<span data-ttu-id="2a400-103">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a400-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a400-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a400-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a400-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a400-105">DESCRIPTION</span></span>
<span data-ttu-id="2a400-106">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a400-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="2a400-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a400-107">EXAMPLES</span></span>

### <span data-ttu-id="2a400-108">Örnek 1 kota ölçülerini alın</span><span class="sxs-lookup"><span data-stu-id="2a400-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2a400-109">"Myiothub" adındaki IotHub için kota ölçümü bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="2a400-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2a400-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a400-110">PARAMETERS</span></span>

### <span data-ttu-id="2a400-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a400-111">-Name</span></span>
<span data-ttu-id="2a400-112">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="2a400-112">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2a400-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a400-113">-ResourceGroupName</span></span>
<span data-ttu-id="2a400-114">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2a400-114">Resource Group Name</span></span>

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

### <span data-ttu-id="2a400-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a400-115">-DefaultProfile</span></span>
<span data-ttu-id="2a400-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a400-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a400-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a400-117">CommonParameters</span></span>
<span data-ttu-id="2a400-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a400-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a400-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a400-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a400-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a400-120">INPUTS</span></span>

### <span data-ttu-id="2a400-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2a400-121">System.String</span></span>

## <span data-ttu-id="2a400-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a400-122">OUTPUTS</span></span>

### <span data-ttu-id="2a400-123">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubquotametric, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2a400-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2a400-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a400-124">NOTES</span></span>

## <span data-ttu-id="2a400-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a400-125">RELATED LINKS</span></span>

