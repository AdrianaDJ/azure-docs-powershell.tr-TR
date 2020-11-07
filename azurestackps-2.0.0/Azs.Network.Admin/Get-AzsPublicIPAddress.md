---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935986"
---
# <span data-ttu-id="1cbad-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="1cbad-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="1cbad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cbad-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbad-103">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-103">List of public ip addresses.</span></span>

## <span data-ttu-id="1cbad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cbad-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1cbad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cbad-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbad-106">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-106">List of public ip addresses.</span></span>

## <span data-ttu-id="1cbad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cbad-107">EXAMPLES</span></span>

### <span data-ttu-id="1cbad-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1cbad-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="1cbad-109">Tahsis edilmiş veya ayrılmamış genel IP adreslerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1cbad-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="1cbad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cbad-110">PARAMETERS</span></span>

### <span data-ttu-id="1cbad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbad-111">-DefaultProfile</span></span>
<span data-ttu-id="1cbad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cbad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cbad-113">-Filtre</span><span class="sxs-lookup"><span data-stu-id="1cbad-113">-Filter</span></span>
<span data-ttu-id="1cbad-114">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="1cbad-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="1cbad-115">-InlineCount</span></span>
<span data-ttu-id="1cbad-116">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="1cbad-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="1cbad-117">-OrderBy</span></span>
<span data-ttu-id="1cbad-118">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="1cbad-119">-Atla</span><span class="sxs-lookup"><span data-stu-id="1cbad-119">-Skip</span></span>
<span data-ttu-id="1cbad-120">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="1cbad-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1cbad-121">-SubscriptionId</span></span>
<span data-ttu-id="1cbad-122">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1cbad-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cbad-123">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cbad-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cbad-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="1cbad-124">-Top</span></span>
<span data-ttu-id="1cbad-125">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="1cbad-125">OData top parameter.</span></span>

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

### <span data-ttu-id="1cbad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbad-126">CommonParameters</span></span>
<span data-ttu-id="1cbad-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cbad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbad-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1cbad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbad-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cbad-129">INPUTS</span></span>

## <span data-ttu-id="1cbad-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cbad-130">OUTPUTS</span></span>

### <span data-ttu-id="1cbad-131">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. modeller. Api20150615. ıpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="1cbad-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="1cbad-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cbad-132">NOTES</span></span>

## <span data-ttu-id="1cbad-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cbad-133">RELATED LINKS</span></span>

