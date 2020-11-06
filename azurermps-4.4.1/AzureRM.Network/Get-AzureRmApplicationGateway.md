---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c15f0dce8102acb609b2e7dcfb9ca4c17626906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587882"
---
# <span data-ttu-id="71c4a-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71c4a-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="71c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="71c4a-103">Uygulama ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="71c4a-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71c4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71c4a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="71c4a-106">**Get-AzureRmApplicationGateway** cmdlet 'i bir uygulama ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="71c4a-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="71c4a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="71c4a-108">Örnek 1: belirtilen uygulama ağ geçidini alma</span><span class="sxs-lookup"><span data-stu-id="71c4a-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71c4a-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="71c4a-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="71c4a-110">Örnek 2: kaynak grubundaki uygulama ağ geçitlerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="71c4a-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71c4a-111">Bu komut, ResourceGroup01 adındaki kaynak grubundaki tüm uygulama ağ geçitlerinin listesini alır ve $AppGwList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="71c4a-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="71c4a-112">Örnek 3: abonelikteki uygulama ağ geçitlerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="71c4a-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="71c4a-113">Bu komut, abonelikteki tüm uygulama ağ geçitlerinin bir listesini alır ve $AppGwList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="71c4a-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="71c4a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71c4a-114">PARAMETERS</span></span>

### <span data-ttu-id="71c4a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="71c4a-115">-Name</span></span>
<span data-ttu-id="71c4a-116">Bu cmdlet 'in aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71c4a-116">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="71c4a-118">Uygulama ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71c4a-118">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="71c4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c4a-119">-DefaultProfile</span></span>
<span data-ttu-id="71c4a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71c4a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c4a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c4a-121">CommonParameters</span></span>
<span data-ttu-id="71c4a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71c4a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c4a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c4a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c4a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71c4a-124">INPUTS</span></span>

### <span data-ttu-id="71c4a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="71c4a-125">System.String</span></span>

## <span data-ttu-id="71c4a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71c4a-126">OUTPUTS</span></span>

### <span data-ttu-id="71c4a-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71c4a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="71c4a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71c4a-128">NOTES</span></span>

## <span data-ttu-id="71c4a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71c4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="71c4a-130">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71c4a-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


