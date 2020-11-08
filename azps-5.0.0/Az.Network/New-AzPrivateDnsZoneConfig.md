---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278835"
---
# <span data-ttu-id="a5ffe-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="a5ffe-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="a5ffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ffe-103">Özel DNS bölgesi grubunun DNS bölgesi yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="a5ffe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5ffe-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ffe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ffe-106">**New-AzPrivateDnsZoneConfig** CMDLET 'i DNS bölge grubunda ayarlanacak yenı bir DNS bölgesi yapılandırma nesnesi oluşturmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="a5ffe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ffe-108">DNS bölgesi yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="a5ffe-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="a5ffe-109">Yukarıdaki örnek DNS bölgesi oluşturur ve DNS bölge yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="a5ffe-110">`New-AzPrivateDnsZone` cmdlet, az. PrivateDns modülünden sağlanır.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="a5ffe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5ffe-111">PARAMETERS</span></span>

### <span data-ttu-id="a5ffe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ffe-112">-DefaultProfile</span></span>
<span data-ttu-id="a5ffe-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ffe-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5ffe-114">-Name</span></span>
<span data-ttu-id="a5ffe-115">Kaynak grubunda benzersiz olan kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="a5ffe-116">Bu ad kaynağa erişmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="a5ffe-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="a5ffe-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="a5ffe-118">Özel DNS bölgesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ffe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ffe-119">CommonParameters</span></span>
<span data-ttu-id="a5ffe-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ffe-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ffe-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5ffe-122">INPUTS</span></span>

### <span data-ttu-id="a5ffe-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a5ffe-123">None</span></span>

## <span data-ttu-id="a5ffe-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5ffe-124">OUTPUTS</span></span>

### <span data-ttu-id="a5ffe-125">Microsoft. Azure. Commands. Network. model. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="a5ffe-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="a5ffe-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5ffe-126">NOTES</span></span>

## <span data-ttu-id="a5ffe-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5ffe-127">RELATED LINKS</span></span>
