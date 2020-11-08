---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266381"
---
# <span data-ttu-id="b9c53-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b9c53-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="b9c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c53-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c53-103">Belirli bir aboneliğin Azure Güvenlik Merkezi tarafından otomatik olarak kaydedileceği konumu alır</span><span class="sxs-lookup"><span data-stu-id="b9c53-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="b9c53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c53-104">SYNTAX</span></span>

### <span data-ttu-id="b9c53-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9c53-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c53-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b9c53-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c53-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b9c53-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c53-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c53-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c53-109">Azure Güvenlik Merkezi, bazı verilerinizi kaydetmek için otomatik olarak bir konuma karar versin.</span><span class="sxs-lookup"><span data-stu-id="b9c53-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="b9c53-110">Bu yeri bulmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9c53-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="b9c53-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c53-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c53-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9c53-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="b9c53-113">Azure Güvenlik Merkezi 'nin hesaplanan güvenlik verilerini kaydettiği konumu alır.</span><span class="sxs-lookup"><span data-stu-id="b9c53-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="b9c53-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c53-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c53-115">-DefaultProfile</span></span>
<span data-ttu-id="b9c53-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c53-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c53-117">-Name</span></span>
<span data-ttu-id="b9c53-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b9c53-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c53-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b9c53-119">-ResourceId</span></span>
<span data-ttu-id="b9c53-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b9c53-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c53-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c53-121">CommonParameters</span></span>
<span data-ttu-id="b9c53-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c53-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c53-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b9c53-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c53-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c53-124">INPUTS</span></span>

### <span data-ttu-id="b9c53-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c53-125">System.String</span></span>

## <span data-ttu-id="b9c53-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c53-126">OUTPUTS</span></span>

### <span data-ttu-id="b9c53-127">Microsoft. Azure. Commands. Security. modeller. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b9c53-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="b9c53-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c53-128">NOTES</span></span>

## <span data-ttu-id="b9c53-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c53-129">RELATED LINKS</span></span>
