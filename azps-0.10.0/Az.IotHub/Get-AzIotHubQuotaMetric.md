---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 7da36f401647a4e020097eb2cfe6690aa1327755
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935832"
---
# <span data-ttu-id="0423c-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="0423c-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="0423c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0423c-102">SYNOPSIS</span></span>
<span data-ttu-id="0423c-103">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0423c-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="0423c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0423c-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0423c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0423c-105">DESCRIPTION</span></span>
<span data-ttu-id="0423c-106">Bir IotHub için kota ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0423c-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="0423c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0423c-107">EXAMPLES</span></span>

### <span data-ttu-id="0423c-108">Örnek 1 kota ölçülerini alın</span><span class="sxs-lookup"><span data-stu-id="0423c-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0423c-109">"Myiothub" adındaki IotHub için kota ölçümü bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="0423c-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0423c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0423c-110">PARAMETERS</span></span>

### <span data-ttu-id="0423c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0423c-111">-DefaultProfile</span></span>
<span data-ttu-id="0423c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0423c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0423c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0423c-113">-Name</span></span>
<span data-ttu-id="0423c-114">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="0423c-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="0423c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0423c-115">-ResourceGroupName</span></span>
<span data-ttu-id="0423c-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0423c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0423c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0423c-117">CommonParameters</span></span>
<span data-ttu-id="0423c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0423c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0423c-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0423c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0423c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0423c-120">INPUTS</span></span>

### <span data-ttu-id="0423c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0423c-121">System.String</span></span>

## <span data-ttu-id="0423c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0423c-122">OUTPUTS</span></span>

### <span data-ttu-id="0423c-123">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubquotametric</span><span class="sxs-lookup"><span data-stu-id="0423c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="0423c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0423c-124">NOTES</span></span>

## <span data-ttu-id="0423c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0423c-125">RELATED LINKS</span></span>
