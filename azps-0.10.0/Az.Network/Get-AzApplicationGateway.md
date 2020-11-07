---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935609"
---
# <span data-ttu-id="d4942-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4942-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="d4942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4942-102">SYNOPSIS</span></span>
<span data-ttu-id="d4942-103">Uygulama ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="d4942-103">Gets an application gateway.</span></span>

## <span data-ttu-id="d4942-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4942-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4942-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4942-105">DESCRIPTION</span></span>
<span data-ttu-id="d4942-106">**Get-AzApplicationGateway** cmdlet 'i bir uygulama ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="d4942-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="d4942-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4942-107">EXAMPLES</span></span>

### <span data-ttu-id="d4942-108">Örnek 1: belirtilen uygulama ağ geçidini alma</span><span class="sxs-lookup"><span data-stu-id="d4942-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4942-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d4942-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="d4942-110">Örnek 2: kaynak grubundaki uygulama ağ geçitlerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="d4942-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4942-111">Bu komut, ResourceGroup01 adındaki kaynak grubundaki tüm uygulama ağ geçitlerinin listesini alır ve $AppGwList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d4942-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="d4942-112">Örnek 3: abonelikteki uygulama ağ geçitlerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="d4942-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="d4942-113">Bu komut, abonelikteki tüm uygulama ağ geçitlerinin bir listesini alır ve $AppGwList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d4942-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="d4942-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4942-114">PARAMETERS</span></span>

### <span data-ttu-id="d4942-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4942-115">-DefaultProfile</span></span>
<span data-ttu-id="d4942-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4942-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4942-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4942-117">-Name</span></span>
<span data-ttu-id="d4942-118">Bu cmdlet 'in aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4942-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4942-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4942-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4942-120">Uygulama ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4942-120">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="d4942-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4942-121">CommonParameters</span></span>
<span data-ttu-id="d4942-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4942-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4942-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4942-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4942-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4942-124">INPUTS</span></span>

### <span data-ttu-id="d4942-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d4942-125">System.String</span></span>

## <span data-ttu-id="d4942-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4942-126">OUTPUTS</span></span>

### <span data-ttu-id="d4942-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4942-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d4942-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4942-128">NOTES</span></span>

## <span data-ttu-id="d4942-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4942-129">RELATED LINKS</span></span>

[<span data-ttu-id="d4942-130">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4942-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


