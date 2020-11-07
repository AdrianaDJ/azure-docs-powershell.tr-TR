---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935565"
---
# <span data-ttu-id="10c71-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10c71-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="10c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c71-102">SYNOPSIS</span></span>
<span data-ttu-id="10c71-103">Uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="10c71-103">Gets an application security group.</span></span>

## <span data-ttu-id="10c71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10c71-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10c71-105">DESCRIPTION</span></span>
<span data-ttu-id="10c71-106">**Get-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="10c71-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="10c71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10c71-107">EXAMPLES</span></span>

### <span data-ttu-id="10c71-108">Örnek 1: tüm uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="10c71-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="10c71-109">Yukarıdaki komut, abonelikteki tüm uygulama güvenlik gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="10c71-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="10c71-110">Örnek 2: kaynak grubundaki uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="10c71-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="10c71-111">Yukarıdaki komut MyResourceGroup kaynak grubuna ait tüm uygulama güvenlik gruplarını getirir.</span><span class="sxs-lookup"><span data-stu-id="10c71-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="10c71-112">Örnek 3: belirli bir uygulama güvenlik grubunu alma.</span><span class="sxs-lookup"><span data-stu-id="10c71-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="10c71-113">Yukarıdaki komut MyApplicationSecurityGroup kaynak grubunun altındaki uygulama güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="10c71-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="10c71-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10c71-114">PARAMETERS</span></span>

### <span data-ttu-id="10c71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c71-115">-DefaultProfile</span></span>
<span data-ttu-id="10c71-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10c71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c71-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="10c71-117">-Name</span></span>
<span data-ttu-id="10c71-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="10c71-118">The resource name.</span></span>

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

### <span data-ttu-id="10c71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c71-119">-ResourceGroupName</span></span>
<span data-ttu-id="10c71-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="10c71-120">The resource group name.</span></span>

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

### <span data-ttu-id="10c71-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c71-121">CommonParameters</span></span>
<span data-ttu-id="10c71-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10c71-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c71-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c71-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c71-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10c71-124">INPUTS</span></span>

### <span data-ttu-id="10c71-125">System. String</span><span class="sxs-lookup"><span data-stu-id="10c71-125">System.String</span></span>

## <span data-ttu-id="10c71-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10c71-126">OUTPUTS</span></span>

### <span data-ttu-id="10c71-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10c71-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="10c71-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10c71-128">NOTES</span></span>

## <span data-ttu-id="10c71-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10c71-129">RELATED LINKS</span></span>

[<span data-ttu-id="10c71-130">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10c71-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="10c71-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10c71-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="10c71-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10c71-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="10c71-133">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="10c71-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
