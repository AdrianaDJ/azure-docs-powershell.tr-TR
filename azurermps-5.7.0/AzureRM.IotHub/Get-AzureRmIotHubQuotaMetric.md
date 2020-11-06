---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 952cf5d9f0eff288a65df2dd2917d341582237db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594080"
---
# <span data-ttu-id="4423a-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="4423a-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="4423a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4423a-102">SYNOPSIS</span></span>
<span data-ttu-id="4423a-103">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4423a-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4423a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4423a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4423a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4423a-105">DESCRIPTION</span></span>
<span data-ttu-id="4423a-106">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4423a-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="4423a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4423a-107">EXAMPLES</span></span>

### <span data-ttu-id="4423a-108">Örnek 1 kota ölçülerini alın</span><span class="sxs-lookup"><span data-stu-id="4423a-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4423a-109">"Myiothub" adındaki IotHub için kota ölçümü bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="4423a-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4423a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4423a-110">PARAMETERS</span></span>

### <span data-ttu-id="4423a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4423a-111">-DefaultProfile</span></span>
<span data-ttu-id="4423a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4423a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4423a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4423a-113">-Name</span></span>
<span data-ttu-id="4423a-114">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="4423a-114">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4423a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4423a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4423a-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4423a-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4423a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4423a-117">CommonParameters</span></span>
<span data-ttu-id="4423a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4423a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4423a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4423a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4423a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4423a-120">INPUTS</span></span>

### <span data-ttu-id="4423a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4423a-121">System.String</span></span>

## <span data-ttu-id="4423a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4423a-122">OUTPUTS</span></span>

### <span data-ttu-id="4423a-123">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubquotametric, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4423a-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4423a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4423a-124">NOTES</span></span>

## <span data-ttu-id="4423a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4423a-125">RELATED LINKS</span></span>

