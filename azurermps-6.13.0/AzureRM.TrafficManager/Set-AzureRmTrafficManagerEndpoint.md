---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587098"
---
# <span data-ttu-id="eaa54-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaa54-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="eaa54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa54-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa54-103">Traffic Manager uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaa54-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaa54-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa54-106">**Set-AzureRmTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'da uç noktayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="eaa54-107">Bu cmdlet, yerel son nokta nesnesinden ayarları güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="eaa54-108">*TrafficManagerEndpoint* parametresini kullanarak veya ardışık düzeni kullanarak uç nokta nesnesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaa54-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="eaa54-109">Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktayı temsil eden yerel bir nesne edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaa54-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="eaa54-110">Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzureRmTrafficManagerEndpoint** kullanın.</span><span class="sxs-lookup"><span data-stu-id="eaa54-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="eaa54-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaa54-111">EXAMPLES</span></span>

### <span data-ttu-id="eaa54-112">Örnek 1: uç noktayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="eaa54-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="eaa54-113">İlk komut **Get-AzureRmTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="eaa54-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="eaa54-114">Komut, uç noktayı $TrafficManagerEndpoint değişkeninde yerel olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="eaa54-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="eaa54-115">İkinci komut, bu uç noktayı yerel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="eaa54-116">Bu komut son nokta kalınlığını 20 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="eaa54-117">Üçüncü komut, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="eaa54-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaa54-118">PARAMETERS</span></span>

### <span data-ttu-id="eaa54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa54-119">-DefaultProfile</span></span>
<span data-ttu-id="eaa54-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eaa54-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa54-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaa54-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="eaa54-122">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="eaa54-123">Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaa54-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="eaa54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa54-124">CommonParameters</span></span>
<span data-ttu-id="eaa54-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaa54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa54-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa54-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaa54-127">INPUTS</span></span>

### <span data-ttu-id="eaa54-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaa54-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="eaa54-129">Bu cmdlet bir **TrafficManagerEndpoint** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="eaa54-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="eaa54-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaa54-130">OUTPUTS</span></span>

### <span data-ttu-id="eaa54-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaa54-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="eaa54-132">Bu cmdlet bir **TrafficManagerEndpoint** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="eaa54-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="eaa54-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaa54-133">NOTES</span></span>

## <span data-ttu-id="eaa54-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaa54-134">RELATED LINKS</span></span>
