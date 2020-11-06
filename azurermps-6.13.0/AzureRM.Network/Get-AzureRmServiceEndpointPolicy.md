---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588476"
---
# <span data-ttu-id="afa40-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afa40-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="afa40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa40-102">SYNOPSIS</span></span>
<span data-ttu-id="afa40-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="afa40-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afa40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afa40-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afa40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afa40-105">DESCRIPTION</span></span>
<span data-ttu-id="afa40-106">**Get-AzureRmServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="afa40-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="afa40-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afa40-107">EXAMPLES</span></span>

### <span data-ttu-id="afa40-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="afa40-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="afa40-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ServiceEndpointPolicy1 adlı hizmet uç noktası ilkesini alır ve $policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="afa40-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="afa40-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="afa40-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="afa40-111">Bu komut, ResourceGroup01 adındaki kaynak grubundaki tüm hizmet uç noktası ilkelerinin listesini alır ve $policyList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="afa40-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="afa40-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afa40-112">PARAMETERS</span></span>

### <span data-ttu-id="afa40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa40-113">-DefaultProfile</span></span>
<span data-ttu-id="afa40-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afa40-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afa40-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="afa40-115">-Name</span></span>
<span data-ttu-id="afa40-116">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="afa40-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa40-117">-ResourceGroupName</span></span>
<span data-ttu-id="afa40-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="afa40-118">The resource group name.</span></span>

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

### <span data-ttu-id="afa40-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa40-119">CommonParameters</span></span>
<span data-ttu-id="afa40-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afa40-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="afa40-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa40-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa40-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afa40-122">INPUTS</span></span>

### <span data-ttu-id="afa40-123">System. String</span><span class="sxs-lookup"><span data-stu-id="afa40-123">System.String</span></span>


## <span data-ttu-id="afa40-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afa40-124">OUTPUTS</span></span>

### <span data-ttu-id="afa40-125">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afa40-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="afa40-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afa40-126">NOTES</span></span>

## <span data-ttu-id="afa40-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afa40-127">RELATED LINKS</span></span>
