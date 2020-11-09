---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325285"
---
# <span data-ttu-id="7de91-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7de91-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="7de91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de91-102">SYNOPSIS</span></span>
<span data-ttu-id="7de91-103">Azure Güvenlik Duvarı Ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="7de91-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="7de91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7de91-104">SYNTAX</span></span>

### <span data-ttu-id="7de91-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7de91-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7de91-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7de91-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de91-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7de91-107">DESCRIPTION</span></span>
<span data-ttu-id="7de91-108">**Get-AzFirewallPolicy** cmdlet 'i kaynak grubunda bir veya daha fazla güvenlik duvarı alır</span><span class="sxs-lookup"><span data-stu-id="7de91-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="7de91-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7de91-109">EXAMPLES</span></span>

### <span data-ttu-id="7de91-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7de91-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="7de91-111">Bu örnek, "TestRg" kaynak grubunda "firewallPolicy" adlı bir güvenlik duvarı ilkesi alır</span><span class="sxs-lookup"><span data-stu-id="7de91-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="7de91-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7de91-112">PARAMETERS</span></span>

### <span data-ttu-id="7de91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de91-113">-DefaultProfile</span></span>
<span data-ttu-id="7de91-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7de91-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de91-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7de91-115">-Name</span></span>
<span data-ttu-id="7de91-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7de91-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de91-117">-ResourceGroupName</span></span>
<span data-ttu-id="7de91-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7de91-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de91-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7de91-119">-ResourceId</span></span>
<span data-ttu-id="7de91-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7de91-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de91-121">CommonParameters</span></span>
<span data-ttu-id="7de91-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7de91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de91-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7de91-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de91-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7de91-124">INPUTS</span></span>

### <span data-ttu-id="7de91-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7de91-125">System.String</span></span>

## <span data-ttu-id="7de91-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7de91-126">OUTPUTS</span></span>

### <span data-ttu-id="7de91-127">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7de91-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="7de91-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7de91-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7de91-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7de91-129">NOTES</span></span>

## <span data-ttu-id="7de91-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7de91-130">RELATED LINKS</span></span>
