---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 704c4c2a11cc83136481573190e745d7a4b2c83f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594633"
---
# <span data-ttu-id="4d81e-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d81e-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="4d81e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d81e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d81e-103">Uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="4d81e-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d81e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d81e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d81e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d81e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d81e-106">**Get-AzureRmApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="4d81e-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="4d81e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d81e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d81e-108">Örnek 1: tüm uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="4d81e-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="4d81e-109">Yukarıdaki komut, abonelikteki tüm uygulama güvenlik gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="4d81e-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="4d81e-110">Örnek 2: kaynak grubundaki uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="4d81e-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="4d81e-111">Yukarıdaki komut MyResourceGroup kaynak grubuna ait tüm uygulama güvenlik gruplarını getirir.</span><span class="sxs-lookup"><span data-stu-id="4d81e-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4d81e-112">Örnek 3: belirli bir uygulama güvenlik grubunu alma.</span><span class="sxs-lookup"><span data-stu-id="4d81e-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="4d81e-113">Yukarıdaki komut MyApplicationSecurityGroup kaynak grubunun altındaki uygulama güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="4d81e-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="4d81e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d81e-114">PARAMETERS</span></span>

### <span data-ttu-id="4d81e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d81e-115">-DefaultProfile</span></span>
<span data-ttu-id="4d81e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d81e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d81e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d81e-117">-Name</span></span>
<span data-ttu-id="4d81e-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4d81e-118">The resource name.</span></span>

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

### <span data-ttu-id="4d81e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d81e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d81e-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4d81e-120">The resource group name.</span></span>

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

### <span data-ttu-id="4d81e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d81e-121">CommonParameters</span></span>
<span data-ttu-id="4d81e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d81e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d81e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d81e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d81e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d81e-124">INPUTS</span></span>

### <span data-ttu-id="4d81e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d81e-125">System.String</span></span>

## <span data-ttu-id="4d81e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d81e-126">OUTPUTS</span></span>

### <span data-ttu-id="4d81e-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d81e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4d81e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d81e-128">NOTES</span></span>

## <span data-ttu-id="4d81e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d81e-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d81e-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d81e-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="4d81e-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d81e-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="4d81e-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d81e-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4d81e-133">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d81e-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
