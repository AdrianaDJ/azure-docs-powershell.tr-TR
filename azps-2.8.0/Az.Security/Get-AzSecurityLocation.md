---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 2de4a80f2770624bb520aa4236a5d92bea97fdf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933267"
---
# <span data-ttu-id="b448f-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b448f-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="b448f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b448f-102">SYNOPSIS</span></span>
<span data-ttu-id="b448f-103">Belirli bir aboneliğin Azure Güvenlik Merkezi tarafından otomatik olarak kaydedileceği konumu alır</span><span class="sxs-lookup"><span data-stu-id="b448f-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="b448f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b448f-104">SYNTAX</span></span>

### <span data-ttu-id="b448f-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b448f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b448f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b448f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b448f-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b448f-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b448f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b448f-108">DESCRIPTION</span></span>
<span data-ttu-id="b448f-109">Azure Güvenlik Merkezi, bazı verilerinizi kaydetmek için otomatik olarak bir konuma karar versin.</span><span class="sxs-lookup"><span data-stu-id="b448f-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="b448f-110">Bu yeri bulmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="b448f-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="b448f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b448f-111">EXAMPLES</span></span>

### <span data-ttu-id="b448f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b448f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="b448f-113">Azure Güvenlik Merkezi 'nin hesaplanan güvenlik verilerini kaydettiği konumu alır.</span><span class="sxs-lookup"><span data-stu-id="b448f-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="b448f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b448f-114">PARAMETERS</span></span>

### <span data-ttu-id="b448f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b448f-115">-DefaultProfile</span></span>
<span data-ttu-id="b448f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b448f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b448f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b448f-117">-Name</span></span>
<span data-ttu-id="b448f-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b448f-118">Resource name.</span></span>

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

### <span data-ttu-id="b448f-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b448f-119">-ResourceId</span></span>
<span data-ttu-id="b448f-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b448f-120">Resource ID.</span></span>

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

### <span data-ttu-id="b448f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b448f-121">CommonParameters</span></span>
<span data-ttu-id="b448f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b448f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b448f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b448f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b448f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b448f-124">INPUTS</span></span>

### <span data-ttu-id="b448f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b448f-125">System.String</span></span>

## <span data-ttu-id="b448f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b448f-126">OUTPUTS</span></span>

### <span data-ttu-id="b448f-127">Microsoft. Azure. Commands. Security. modeller. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b448f-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="b448f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b448f-128">NOTES</span></span>

## <span data-ttu-id="b448f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b448f-129">RELATED LINKS</span></span>
