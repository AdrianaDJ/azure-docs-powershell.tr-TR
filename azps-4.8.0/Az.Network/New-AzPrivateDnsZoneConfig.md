---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109469"
---
# <span data-ttu-id="f974a-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f974a-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="f974a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f974a-102">SYNOPSIS</span></span>
<span data-ttu-id="f974a-103">Özel DNS bölgesi grubunun DNS bölgesi yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f974a-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="f974a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f974a-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f974a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f974a-105">DESCRIPTION</span></span>
<span data-ttu-id="f974a-106">**New-AzPrivateDnsZoneConfig** CMDLET 'i DNS bölge grubunda ayarlanacak yenı bir DNS bölgesi yapılandırma nesnesi oluşturmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="f974a-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="f974a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f974a-107">EXAMPLES</span></span>

### <span data-ttu-id="f974a-108">DNS bölgesi yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="f974a-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="f974a-109">Yukarıdaki örnek DNS bölgesi oluşturur ve DNS bölge yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f974a-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="f974a-110">`New-AzPrivateDnsZone` cmdlet, az. PrivateDns modülünden sağlanır.</span><span class="sxs-lookup"><span data-stu-id="f974a-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="f974a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f974a-111">PARAMETERS</span></span>

### <span data-ttu-id="f974a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f974a-112">-DefaultProfile</span></span>
<span data-ttu-id="f974a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f974a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f974a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="f974a-114">-Name</span></span>
<span data-ttu-id="f974a-115">Kaynak grubunda benzersiz olan kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="f974a-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="f974a-116">Bu ad kaynağa erişmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f974a-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="f974a-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="f974a-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="f974a-118">Özel DNS bölgesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f974a-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="f974a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f974a-119">CommonParameters</span></span>
<span data-ttu-id="f974a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f974a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f974a-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f974a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f974a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f974a-122">INPUTS</span></span>

### <span data-ttu-id="f974a-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f974a-123">None</span></span>

## <span data-ttu-id="f974a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f974a-124">OUTPUTS</span></span>

### <span data-ttu-id="f974a-125">Microsoft. Azure. Commands. Network. model. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f974a-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="f974a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f974a-126">NOTES</span></span>

## <span data-ttu-id="f974a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f974a-127">RELATED LINKS</span></span>
