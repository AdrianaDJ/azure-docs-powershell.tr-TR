---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587163"
---
# <span data-ttu-id="a07ae-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a07ae-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="a07ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a07ae-103">Belirli bir aboneliğin Azure Güvenlik Merkezi tarafından otomatik olarak kaydedileceği konumu alır</span><span class="sxs-lookup"><span data-stu-id="a07ae-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a07ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a07ae-104">SYNTAX</span></span>

### <span data-ttu-id="a07ae-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a07ae-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07ae-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a07ae-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07ae-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a07ae-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a07ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a07ae-108">DESCRIPTION</span></span>
<span data-ttu-id="a07ae-109">Azure Güvenlik Merkezi, bazı verilerinizi kaydetmek için otomatik olarak bir konuma karar versin.</span><span class="sxs-lookup"><span data-stu-id="a07ae-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="a07ae-110">Bu yeri bulmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="a07ae-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="a07ae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a07ae-111">EXAMPLES</span></span>

### <span data-ttu-id="a07ae-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a07ae-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="a07ae-113">Azure Güvenlik Merkezi 'nin hesaplanan güvenlik verilerini kaydettiği konumu alır.</span><span class="sxs-lookup"><span data-stu-id="a07ae-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="a07ae-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a07ae-114">PARAMETERS</span></span>

### <span data-ttu-id="a07ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07ae-115">-DefaultProfile</span></span>
<span data-ttu-id="a07ae-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a07ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07ae-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a07ae-117">-Name</span></span>
<span data-ttu-id="a07ae-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a07ae-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07ae-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a07ae-119">-ResourceId</span></span>
<span data-ttu-id="a07ae-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a07ae-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07ae-121">CommonParameters</span></span>
<span data-ttu-id="a07ae-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a07ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07ae-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07ae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07ae-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a07ae-124">INPUTS</span></span>

### <span data-ttu-id="a07ae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a07ae-125">System.String</span></span>

## <span data-ttu-id="a07ae-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a07ae-126">OUTPUTS</span></span>

### <span data-ttu-id="a07ae-127">Microsoft. Azure. Commands. Security. modeller. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a07ae-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="a07ae-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a07ae-128">NOTES</span></span>

## <span data-ttu-id="a07ae-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a07ae-129">RELATED LINKS</span></span>
