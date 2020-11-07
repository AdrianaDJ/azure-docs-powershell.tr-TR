---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753861"
---
# <span data-ttu-id="1f8de-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f8de-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1f8de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f8de-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8de-103">Traffic Manager uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="1f8de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f8de-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f8de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f8de-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8de-106">**Set-AzTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'da uç noktayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="1f8de-107">Bu cmdlet, yerel son nokta nesnesinden ayarları güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="1f8de-108">*TrafficManagerEndpoint* parametresini kullanarak veya ardışık düzeni kullanarak uç nokta nesnesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8de-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="1f8de-109">Get-AzTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktayı temsil eden yerel bir nesne edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8de-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="1f8de-110">Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzTrafficManagerEndpoint** kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f8de-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="1f8de-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f8de-111">EXAMPLES</span></span>

### <span data-ttu-id="1f8de-112">Örnek 1: uç noktayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1f8de-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="1f8de-113">İlk komut **Get-AzTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="1f8de-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="1f8de-114">Komut, uç noktayı $TrafficManagerEndpoint değişkeninde yerel olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="1f8de-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="1f8de-115">İkinci komut, bu uç noktayı yerel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="1f8de-116">Bu komut son nokta kalınlığını 20 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="1f8de-117">Üçüncü komut, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="1f8de-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f8de-118">PARAMETERS</span></span>

### <span data-ttu-id="1f8de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8de-119">-DefaultProfile</span></span>
<span data-ttu-id="1f8de-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f8de-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f8de-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f8de-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1f8de-122">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="1f8de-123">Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f8de-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8de-124">CommonParameters</span></span>
<span data-ttu-id="1f8de-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f8de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8de-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f8de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8de-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f8de-127">INPUTS</span></span>

### <span data-ttu-id="1f8de-128">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f8de-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1f8de-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f8de-129">OUTPUTS</span></span>

### <span data-ttu-id="1f8de-130">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f8de-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1f8de-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f8de-131">NOTES</span></span>

## <span data-ttu-id="1f8de-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f8de-132">RELATED LINKS</span></span>
